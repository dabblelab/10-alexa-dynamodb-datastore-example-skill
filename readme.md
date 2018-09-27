# DynamoDB Starter Alexa Template

This is a simple template that shows use of DynamoDB with Alexa. This template uses the [Alexa Skills Kit for Node.js](https://github.com/alexa/alexa-skills-kit-sdk-for-nodejs) version 2.0 and is designed to be used with the [Alexa Skills Kit CLI](https://developer.amazon.com/docs/smapi/ask-cli-intro.html).


## Instructions to execute this template 
- Provide DynamoDB execution permission to the Lambda.
- Create a DynamoDB table with name dynamodb-starter and schema, userId as a Partition Key and movieTitle as a sort key. 

```
{
    AttributeDefinitions: [
        {
            AttributeName: 'userId',
            AttributeType: 'S'
        },
        {
            AttributeName: 'movieTitle',
            AttributeType: 'S'
        }
    ],
    KeySchema: [
        {
            AttributeName: 'userId',
            KeyType: 'HASH'
        },
        {
            AttributeName: 'movieTitle',
            KeyType: 'RANGE'
        }
    ]
}
```