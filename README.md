# ripple-energy-openapi

## Background

This repository was created to simplify the integration with the API endpoints provided by Ripple Energy.  Documenting the APIs using OpenAPI spec provides the ability to use the Swagger UI to visually document and interact with the API using the try it now functionality.

## Viewing the ripple-energy-openapi spec on github.io

You can view the ripple-energy-openapi spec here: https://vls29.github.io/ripple-energy-openapi

## Generating a client using openapi-generator-cli

From [their GitHub documentation](https://github.com/OpenAPITools/openapi-generator/) "OpenAPI Generator allows generation of API client libraries (SDK generation), server stubs, documentation and configuration automatically given an OpenAPI Spec".

Below is an example of using the openapi-generator-cli to generate a bash client from the ripple-energy-api.yaml file:

```
docker run \
    --rm \
    -v "${PWD}:/files" \
    openapitools/openapi-generator-cli \
    generate \
    -i /files/ripple-energy-api.yaml \
    -g bash \
    -o /files/client/
```

See https://github.com/OpenAPITools/openapi-generator/ for full documentation on the openapi-generator.

## Contributing

If you find an endpoint you need is not documented, or incorrectly documented, please consider submitting a PR with the amendments.

### How to run up the Swagger UI viewer in Codespaces

To run up the Swagger UI viewer in your Codespaces container, you can use the docker compose file by running the following from the terminal: `docker compose up`