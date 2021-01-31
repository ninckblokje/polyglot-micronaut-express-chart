# poyglot-micronaut-express-chart

A Helm chart for [polyglot-micronaut-express](https://github.com/ninckblokje/polyglot-micronaut-express), container images can be foud in [Docker hub](https://hub.docker.com/repository/docker/ninckblokje/polyglot-micronaut-express).

Possible variables:

````yaml
pme:
  jdbc:
    driver: "org.postgresql.Driver"
    password: ""
    url: "jdbc:postgresql://localhost:5432/postgres"
    username: ""
````

This chart will deploy the following:
- Configmap
- Secret
- Deployment
- Service

Handy commands:
````
helm install [RELEASE_NAME] . -f myvalues.yaml
helm install --dry-run [RELEASE_NAME] . -f myvalues.yaml
helm upgrade [RELEASE_NAME] . -f myvalues.yaml
helm uninstall [RELEASE_NAME]
helm get manifest [RELEASE_NAME]
````

Packaging:
````
helm lint .
helm package .
helm repo index --url https://ninckblokje.github.io/polyglot-micronaut-express-chart/ .
````
