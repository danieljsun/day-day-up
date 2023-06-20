## visibility timeout and maximum receives

```
Given SQS default visibility timeout 3 minutes
And dead-letter queue maximum receives 5 count
And the lambda trigger would fail always
Then the metric `aws.lambda.errors` would have 5 counts of 1 error with 3 minutes interval
And the msg would be put to DLQ after 15 minutes
```

