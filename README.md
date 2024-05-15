# Docker image for running Azure CLI commands in an Azure Pipelines container job

<!-- markdownlint-disable MD013 -->
[![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://github.com/swissgrc/docker-azure-pipelines-azurecli-net7/blob/main/LICENSE) [![Build](https://img.shields.io/github/actions/workflow/status/swissgrc/docker-azure-pipelines-azurecli-net7/publish.yml?branch=develop&style=flat-square)](https://github.com/swissgrc/docker-azure-pipelines-azurecli-net7/actions/workflows/publish.yml) [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=swissgrc_docker-azure-pipelines-azurecli-net7&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=swissgrc_docker-azure-pipelines-azurecli-net7) [![Pulls](https://img.shields.io/docker/pulls/swissgrc/azure-pipelines-azurecli.svg?style=flat-square)](https://hub.docker.com/r/swissgrc/azure-pipelines-azurecli) [![Stars](https://img.shields.io/docker/stars/swissgrc/azure-pipelines-azurecli.svg?style=flat-square)](https://hub.docker.com/r/swissgrc/azure-pipelines-azurecli)
<!-- markdownlint-restore -->

Docker image to run Azure CLI commands in [Azure Pipelines container jobs].

## Usage

This image can be used to run Azure CLI commands in [Azure Pipelines container jobs].

### Azure Pipelines Container Job

To use the image in an Azure Pipelines Container Job, add one of the following example tasks and use it with the `container` property.

The following example shows the container used for a deployment step with a Azure CLI command:

```yaml
  - stage: deploy
    jobs:
      - deployment: runAzureCLI
        container: swissgrc/azure-pipelines-azurecli:latest-net7
        environment: smarthotel-dev
        strategy:
          runOnce:
            deploy:
              steps:
                - bash: |
                    az version
```

### Tags

| Tag           | Description                                                                                               | Base Image                                | Azure CLI | Size                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------|-----------|--------------------------------------------------------------------------------------------------------------------------------------|
| latest-net7   | Identical to `latest` tag                                                                                 | swissgrc/azure-pipelines-dotnet:7.0.409   | 2.60.0    | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-azurecli/latest?style=flat-square)      |
| unstable-net7 | Identical to `unstable` tag                                                                               | swissgrc/azure-pipelines-dotnet:7.0.409   | 2.60.0    | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-azurecli/unstable?style=flat-square)    |
| 2.49.0-net7   | [Azure CLI 2.49.0](https://learn.microsoft.com/en-us/cli/azure/release-notes-azure-cli#may-23-2023)       | swissgrc/azure-pipelines-dotnet:7.0.304   | 2.49.0    | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-azurecli/2.49.0-net7?style=flat-square) |
| 2.50.0-net7   | [Azure CLI 2.50.0](https://learn.microsoft.com/en-us/cli/azure/release-notes-azure-cli#july-04-2023)      | swissgrc/azure-pipelines-dotnet:7.0.305   | 2.50.0    | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-azurecli/2.50.0-net7?style=flat-square) |
| 2.51.0-net7   | [Azure CLI 2.51.0](https://learn.microsoft.com/en-us/cli/azure/release-notes-azure-cli#august-01-2023)    | swissgrc/azure-pipelines-dotnet:7.0.306   | 2.51.0    | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-azurecli/2.51.0-net7?style=flat-square) |
| 2.52.0-net7   | [Azure CLI 2.52.0](https://learn.microsoft.com/en-us/cli/azure/release-notes-azure-cli#september-05-2023) | swissgrc/azure-pipelines-dotnet:7.0.400   | 2.52.0    | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-azurecli/2.52.0-net7?style=flat-square) |
| 2.53.0-net7   | [Azure CLI 2.53.0](https://learn.microsoft.com/en-us/cli/azure/release-notes-azure-cli#september-26-2023) | swissgrc/azure-pipelines-dotnet:7.0.401   | 2.53.0    | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-azurecli/2.53.0-net7?style=flat-square) |
| 2.53.1-net7   | [Azure CLI 2.53.1](https://learn.microsoft.com/en-us/cli/azure/release-notes-azure-cli#october-24-2023)   | swissgrc/azure-pipelines-dotnet:7.0.402   | 2.53.1    | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-azurecli/2.53.1-net7?style=flat-square) |
| 2.54.0-net7   | [Azure CLI 2.54.0](https://learn.microsoft.com/en-us/cli/azure/release-notes-azure-cli#november-14-2023)  | swissgrc/azure-pipelines-dotnet:7.0.403   | 2.54.0    | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-azurecli/2.54.0-net7?style=flat-square) |
| 2.55.0-net7   | [Azure CLI 2.55.0](https://learn.microsoft.com/en-us/cli/azure/release-notes-azure-cli#december-05-2023)  | swissgrc/azure-pipelines-dotnet:7.0.404   | 2.55.0    | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-azurecli/2.55.0-net7?style=flat-square) |
| 2.56.0-net7   | [Azure CLI 2.56.0](https://learn.microsoft.com/en-us/cli/azure/release-notes-azure-cli#january-09-2024)   | swissgrc/azure-pipelines-dotnet:7.0.405   | 2.56.0    | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-azurecli/2.56.0-net7?style=flat-square) |
| 2.57.0-net7   | [Azure CLI 2.57.0](https://learn.microsoft.com/en-us/cli/azure/release-notes-azure-cli#february-06-2024)  | swissgrc/azure-pipelines-dotnet:7.0.406   | 2.57.0    | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-azurecli/2.57.0-net7?style=flat-square) |
| 2.58.0-net7   | [Azure CLI 2.58.0](https://learn.microsoft.com/en-us/cli/azure/release-notes-azure-cli#march-05-2024)     | swissgrc/azure-pipelines-dotnet:7.0.407   | 2.58.0    | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-azurecli/2.58.0-net7?style=flat-square) |
| 2.59.0-net7   | [Azure CLI 2.59.0](https://learn.microsoft.com/en-us/cli/azure/release-notes-azure-cli#april-02-2024)     | swissgrc/azure-pipelines-dotnet:7.0.408   | 2.59.0    | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-azurecli/2.59.0-net7?style=flat-square) |
| 2.60.0-net7   | [Azure CLI 2.60.0](https://learn.microsoft.com/en-us/cli/azure/release-notes-azure-cli#april-30-2024)     | swissgrc/azure-pipelines-dotnet:7.0.409   | 2.60.0    | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-azurecli/2.60.0-net7?style=flat-square) |

[Azure Pipelines container jobs]: https://docs.microsoft.com/en-us/azure/devops/pipelines/process/container-phases
