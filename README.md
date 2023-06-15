---
page_type: sample
languages:
- java
products:
- azure-functions
- azure
description: "This repository contains sample for Azure Functions in Java"
urlFragment: "azure-functions-java"
---

# Azure Functions samples in Java

This repository contains samples which show the basis usage of [Azure Functions](https://docs.microsoft.com/en-us/azure/azure-functions/) in Java.

## Contents


## Prerequisites

- Gradle 4.10+
- Latest [Function Core Tools](https://aka.ms/azfunc-install)
- Azure CLI. This plugin use Azure CLI for authentication, please make sure you have Azure CLI installed and logged in.

## Setup

- ```cmd
    az login
    az account set -s <your subscription id>
    ```
- Update the Application settings in Azure portal with the required parameters as below
  - AzureWebJobsStorage: Connection string to your storage account
  - CosmosDBDatabaseName: Cosmos database name. Example: ItemCollectionIn
  - CosmosDBCollectionName:Cosmos database collection name. Example: ItemDb
  - AzureWebJobsCosmosDBConnectionString: Connection string to your Cosmos database
  - AzureWebJobsEventGridOutputBindingTopicUriString: Event Grid URI
  - AzureWebJobsEventGridOutputBindingTopicKeyString: Event Grid string
  - AzureWebJobsEventHubSender, AzureWebJobsEventHubSender_2 : Event hub connection string
  - AzureWebJobsServiceBus: Service bus connection string
  - SBQueueName: Service bus queue name. Example: test-input-java
  - SBTopicName: Service bus topic name. Example: javaworkercitopic2
  - SBTopicSubName: Service bus topic name. Example: javaworkercisub
- Update `host.json` with the right extension bundle version. `V3 - [1.*, 2.0.0) and V4 - [2.*, 3.0.0)`

## Running the sample

```cmd
./mvnw clean package azure-functions:run
```

```cmd
./gradlew clean azureFunctionsRun
```

## Deploy the sample on Azure


```cmd
./mvnw clean package azure-functions:deploy
```

```cmd
./gradlew clean azureFunctionsDeploy
```

> NOTE: please replace '/' with '\\' when you are running on windows.


