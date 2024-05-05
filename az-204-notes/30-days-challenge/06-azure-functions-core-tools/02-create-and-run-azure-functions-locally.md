# Create and Run Azure Functions Locally by Using the Core Tools

## Introduction

The Azure Functions Core Tools allow you to develop and run functions on your local computer from the command line. In this unit, you will learn how to use these tools to create and run your first function, a simple interest calculator, locally on your computer without relying on the Azure portal's functions editor. This unit will provide an overview of the Core Tools before delving into practical exercises in the subsequent unit, where you will use the Azure Cloud Shell.

## What is Azure Functions Core Tools?

Azure Functions Core Tools consist of a standalone runtime and a set of command-line tools that facilitate the development, testing, and deployment of function code from your local computer. These tools offer various capabilities, including:

- Generating the necessary files and folders for local function development.
- Providing a local runtime for testing and debugging functions.
- Publishing functions to Azure.

You can accomplish these tasks directly from the command line, using any text editor of your choice for code writing and configuration. Additionally, signing in to Azure, creating Azure resources, and deploying project files require the Azure CLI or Azure PowerShell.

## Core Tools Versions

The major version of Core Tools must match the major version of the Functions runtime in Azure. Currently, version 4.x is recommended, supporting all languages. While this tutorial discusses version 4.x, you will utilize Core Tools within an Azure Cloud Shell environment in your browser, where necessary versions of Core Tools, Azure CLI, and Node.js are already installed.

## Local Development vs. Azure Portal Development

While the Azure portal offers a built-in editor for function code, it's limited to specific language stacks and cannot edit locally developed functions deployed to Azure. Core Tools support local development for all language stacks supported by Azure Functions.

## Create Functions Locally

You'll now explore how to create functions with Core Tools and run them locally. The process involves:

1. **Creating a new functions project with `func init`**: Initializes a new functions project.
2. **Creating a new function with `func new`**: Generates a new function within the project.
3. **Running functions locally with `func start`**: Hosts the Azure Functions runtime locally for testing.

Let's proceed with a closer look at these steps in the upcoming exercises.
