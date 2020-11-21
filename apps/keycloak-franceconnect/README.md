# Keycloak-FranceConnect Demo app

This chart needs an existing secret in the namespace containing the clientSecret provided by FranceConnect. To create it, you can use the following command:

```sh
echo -n '<clientsecret>' > test-fc_clientsecret && \
kubectl create secret generic clientsecret --from-file=./test-fc_clientsecret
```

This chart create a configmap `test-fc-realm` with a test-fc.json file pointing to the content of `/realm/test-fc.json` .
