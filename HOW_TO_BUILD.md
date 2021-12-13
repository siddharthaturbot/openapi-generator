# How to build

## Maven build

`./mvnw -Dmaven.test.skip clean "-Dio.swagger.parser.util.RemoteUrl.trustAll=true -Dio.swagger.v3.parser.util.RemoteUrl.trustAll=true -Dmaven.test.skip=true" package`

## Build Go API

```
java -jar modules/openapi-generator-cli/target/openapi-generator-cli.jar generate \
   -i /Users/mike/Downloads/steampipe_cloud_openapi.json \
   -g go \
   -o /Users/mike/Code/github.com/turbot/steampipe-cloud-sdk-go \
   --package-name steampipecloud  --git-repo-id steampipe-cloud-sdk-go --git-user-id turbot --remove-operation-id-prefix --additional-properties structPrefix=true
```

