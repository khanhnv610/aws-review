# cloudwatch

- mặc định theo dõi dc các metric gì?
- có thêm theo dõi thêm các metric gì?
- cloudwatch logs làm dc gì ngoài thu thập logs?

# dynamoDB steam

- là gì?
- làm dc những gì?

When you enable DynamoDB Streams on a table, you can associate the stream ARN with a Lambda
function that you write. Immediately after an item in the table is modified, a new record appears in the
table's stream. AWS Lambda polls the stream and invokes your Lambda function synchronously when it
detects new stream records. Since our requirement is to have an immediate entry made to an
application in case an item in the DynamoDB table is modified, a lambda function is also required.
Let us try to analyze this with an example:
Consider a mobile gaming app that writes to a GamesScores table. Whenever the top score of the
GameScores table is updated, a corresponding stream record is written to the table's stream. This event
could then trigger a Lambda function that posts a Congratulatory message on a Social media network
handle.
DynamoDB streams can be used to monitor the changes to a DynamoDB table.
AWS Documentation mentions the following:
A DynamoDB stream is an ordered flow of information about changes to items in an Amazon DynamoDB
table. When you enable a stream on a table, DynamoDB captures information about every modification
to data items in the table.
For more information on DynamoDB streams, please refer to the URL below.
https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Streams.html

# IAM

- cognito identity và user pools là gì?
- federated identity providers là gì?

Reference:
https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pools-identityfederation.html

https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_oidc.html

https://aws.amazon.com/articles/web-identity-federation-with-mobile-applications/

https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-getting-started.html

# Elastic load balance
