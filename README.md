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