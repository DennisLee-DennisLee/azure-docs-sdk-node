---
title: Azure Core AMQP client library for AMQP operations
keywords: Azure, js, SDK, API,  @azure/core-amqp
author: maggiepint
ms.author: magpint
ms.date: 06/10/2020
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: js
ms.service: core
---

# Azure Core HTTP client library for JavaScript - Version 1.1.3

This is the core HTTP pipeline for Azure SDK JavaScript libraries which work in the browser and Node.js. This library is primarily intended to be used in code generated by [AutoRest](https://github.com/Azure/Autorest) and [`autorest.typescript`](https://github.com/Azure/autorest.typescript).

## Getting started

### Requirements

- [Node.js](https://nodejs.org) version > 8.x
- Typescript compiler

```shell
npm install -g typescript
```

### Installation

This package is primarily used in generated code and not meant to be consumed directly by end users.

## Key concepts

You can find an explanation of how this repository's code works by going to our [architecture overview](https://github.com/Azure/azure-sdk-for-js/blob/master/sdk/core/core-http/docs/architectureOverview.md).

## Examples

Examples can be found in the `samples` folder.

## Next steps

- Build this library (`core-http`). For more information on how to build project in this repo, please refer to the [Contributing Guide](https://github.com/Azure/azure-sdk-for-js/blob/master/CONTRIBUTING.md).

- The code in `samples\node-sample.ts` shows how to create a `ServiceClient` instance with a test `TokenCredential` implementation and use the client instance to perform a `GET` operation from the Azure management service endpoint for subscriptions. To run the code, first obtain an access token to the Azure management service.

One easy way to get an access token is using [Azure CLI](https://docs.microsoft.com/cli/azure/?view=azure-cli-latest)

1. Sign in
```shell
az login
```
2. Select the subscription to use
```shell
az account set -s <subscription id>
```
3. Obtain an access token
```shell
az account get-access-token --resource=https://management.azure.com
```

### NodeJS

- Set values of `subscriptionId` and `token` variable in `samples/node-sample.ts`

- Change directory to samples folder, compile the TypeScript code, then run the sample

```
cd samples
tsc node-sample.ts
node node-sample.js
```

### Browser

- Set values of `subscriptionId` and `token` variable in `samples/index.js`
- Follow the instructions of [JavaScript Bundling Guide using Parcel](https://github.com/Azure/azure-sdk-for-js/blob/master/documentation/Bundling.md#using-parcel) to build and run the code in the browser.

## Troubleshooting

If you run into issues while using this library, please feel free to [file an issue](https://github.com/Azure/azure-sdk-for-js/issues/new).

## Contributing

If you'd like to contribute to this library, please read the [contributing guide](https://github.com/Azure/azure-sdk-for-js/blob/master/CONTRIBUTING.md) to learn more about how to build and test the code.

![Impressions](https://azure-sdk-impressions.azurewebsites.net/api/impressions/azure-sdk-for-js%2Fsdk%2Fcore%2Fcore-http%2FREADME.png)
