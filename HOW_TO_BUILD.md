# How to build

## Maven build

`./mvnw -Dmaven.test.skip clean package`

## Build Go API

```
java -jar -Dio.swagger.v3.parser.util.RemoteUrl.trustAll=true modules/openapi-generator-cli/target/openapi-generator-cli.jar generate \
   -i https://localhost:8443/api/v0/docs/openapi.json \
   -g go \
   -o /path/to/code/turbot/pipes-sdk-go \
   --package-name pipes --git-repo-id pipes-sdk-go --git-user-id turbot --remove-operation-id-prefix --additional-properties structPrefix=true
```

## Go Format the code

`gofmt -s -w .`