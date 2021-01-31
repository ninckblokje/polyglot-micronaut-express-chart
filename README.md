# poyglot-micronaut-express-chart

A Helm chart for [polyglot-micronaut-express](https://github.com/ninckblokje/polyglot-micronaut-express), container images can be foud in [Docker hub](https://hub.docker.com/repository/docker/ninckblokje/polyglot-micronaut-express).

This chart will deploy the following:
- Configmap
- Secret
- Deployment
- Service

## Configuration

Provide the following as basic configuration:

````yaml
pme:
  jdbc:
    driver: "org.postgresql.Driver"
    password: ""
    url: "jdbc:postgresql://localhost:5432/postgres"
    username: ""
````

It is possible to use [Azure Key Vault Provider]() for Azure Keyvault integration, by specifying the following additional configuration:

````yaml
azure:
  secretFromKeyvault: true
  keyvaultName: ""
  resourceGroup: ""
  subscriptionId: ""
  tenantId: ""
````

## Commands

````
helm install [RELEASE_NAME] . -f myvalues.yaml
helm install --dry-run [RELEASE_NAME] . -f myvalues.yaml
helm upgrade [RELEASE_NAME] . -f myvalues.yaml
helm uninstall [RELEASE_NAME]
helm get manifest [RELEASE_NAME]
````

## Packaging

````
helm lint .
helm package .
helm repo index --url https://ninckblokje.github.io/polyglot-micronaut-express-chart/ .
````
