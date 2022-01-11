# Managed Sentinel SOC Script & Documentation Repository
## Repository to feed the Sentinel as a code Solution (in combination with Azure Devops)

Repository with all scripts related to the Managed SOC environment (Azure Lighthouse - Sentinel)
This repo contains all scripts to run either in the customer tenant to create the required resources / solutions or to use in the master tenant to manage an existing setup.


# Azure Sentinel as Code

The purpose of this project is to provide tools to enable automatic deployment of Azure Sentinel environments through Azure DevOps.

A blog post explaining more about this project is available at [Deploying and Managing Azure Sentinel as code](https://techcommunity.microsoft.com/t5/azure-sentinel/deploying-and-managing-azure-sentinel-as-code/ba-p/1131928)

The project has several folders for each of the different Sentinel components that can be configured (Onboard, Connectors, Workbooks, Analytics Rules, Hunting Rules, Playbooks) plus folders for script helpers and Az DevOps YAML pipelines. In this README we explain some of the basics for each of them but we encourage you to visit each of the folders for more details on how to use the tools.

## Scripts

Scripts that are used inside the Azure DevOps pipelines to automate the deployment of the different Sentinel components

## Pipelines

YAML files that define the CI/CD pipelines that can be used to automated the deployment of Sentinel components

## Onboard

Automating the installation of Azure Sentinel on one or more workspaces as defined in config file under Onboard

## Connectors

Automatically connect data sources to start sending data into Sentinel. This can only be done for Microsoft first party services that don't require additional configuration on the data source side

## Workbooks

Collection of custom workbooks in JSON format that can be leveraged to add additional visibility into environments

## Analytics Rules

Definition files containing all the analytics rule alerts to be created in an environment

## Hunting Rules

Definition files containing all the hunting rules to be created in an environment

## Playbooks

Collection of custom playbooks to be added to your Sentinel environment
