#collector-backend

## deploy:

```
aws cloudformation package --template-file template.yaml --output-template-file output.yaml --s3-bucket desole-upload-1
aws cloudformation deploy --template-file output.yaml --stack-name desole-test2 --capabilities CAPABILITY_IAM
```

## todo:

* repackage so linting doesn't confuse cloudformation
* add output to template.yaml so we have the endpoint
* CORS handling
* memory/timeout for lambda

#

```
curl -X POST https://pt8uhzwsci.execute-api.us-east-1.amazonaws.com/Prod/hello-world -H "Content-Type: application/json" -i --data @event.json
```

