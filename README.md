# tap-dynamodb

[![CircleCI](https://circleci.com/gh/singer-io/tap-dynamodb.svg?style=svg)](https://circleci.com/gh/singer-io/tap-dynamodb)

This is a [Singer](https://singer.io) tap that produces JSON-formatted data
following the [Singer
spec](https://github.com/singer-io/getting-started/blob/master/SPEC.md).

## Configuration

**Required Settings:**

The config file requires `region_name`.

**Authentication:**

This tap can get it's credentials in a variety of ways, including [environment variables](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/configuration.html#environment-variables), [shared credentials file](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/configuration.html#shared-credentials-file), [AWS config file](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/configuration.html#aws-config-file), [assume role provider](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/configuration.html#assume-role-provider), and [IAM roles](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/configuration.html#iam-roles).

You can optionally add ond of the following sets of configurations:

**Option A: Assume role through external ID:**

_To use an external ID, specify the following config options:_

- `account_id`
- `external_id`
- `role_name`

**Option B: Use explicit AWS credentials:**

_To use a specific AWS user, specify at minimum the user's access key and secret key:_

- `aws_access_key_id`
- `aws_secret_access_key`
- `aws_session_token` _(if applicable)_

## Testing

For testing you can specify `use_local_dynamo` to run against a local instance of [DynamoDB Local](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.html).

Copyright &copy; 2019 Stitch
