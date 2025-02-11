# Crossmint Fern Configuration

This repository contains your Fern configuration: 
  - [OpenAPI Spec](./fern/openapi/openapi.yaml)
  - [OpenAPI Overrides](./fern/openapi/openapi-overrides.yml)
  - [SDK generator config](./fern/generators.yml)

View the documentation [here](https://crossmint.docs.buildwithfern.com).

## Updating your Docs

### Local Development server

To run a local development server with hot-reloading you can run the following command

```sh
fern docs dev
```

### Hosted URL 

Documentation is automatically updated when you push to main via the `fern generate` command. 

```sh
npm install -g fern-api # only required once
fern generate --docs
```

## Validating your OpenAPI spec

To validate your API, run: 
```sh
npm install -g fern-api # only required once
fern check
```

## Updating your SDKs

To update your SDKs, simply run the `Release TypeScript SDK` GitHub Action with the desired version for the release. Under the hood, this leverages the Fern CLI: 

```sh
npm install -g fern-api # only required once
fern generate --group ts-sdk
```