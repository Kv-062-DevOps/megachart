# megachart
Megachart to deploy all our not megacharts

To install this, you first need to install the registry-creds chart. You can find it in file ecr.md. Then, when installing
you need to override several env variables in back service. Your command will look like this:
```
helm install --set db-service.access_key="dynamodb-user-access-key" \
--set db-service.secret_key="dynamodb-user-secret-access-key" --set db-service.region="dynamodb-region" release-name
chart-location

```
