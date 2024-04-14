# Configuring Security Certificates in Azure App Service

## Introduction

Securing information transmitted between your company's app and the customer is crucial for maintaining data privacy and integrity. Azure App Service provides tools to create, upload, or import private and public certificates, ensuring secure communication. This document outlines various options available for adding certificates in App Service and requirements for private certificates.

## Options for Adding Certificates

### 1. Create a Free App Service Managed Certificate

- **Description**: Private certificate provided free of charge for securing custom domains in App Service.
- **Features**: Easy to use and managed by Azure.

### 2. Purchase an App Service Certificate

- **Description**: Private certificate managed by Azure, combining automated management with flexibility for renewal and export options.

### 3. Import a Certificate from Key Vault

- **Description**: Suitable if you manage certificates using Azure Key Vault.

### 4. Upload a Private Certificate

- **Description**: Option for uploading private certificates from third-party providers.

### 5. Upload a Public Certificate

- **Description**: Suitable for loading public certificates into code for accessing remote resources.

## Private Certificate Requirements

- Exported as a password-protected PFX file, encrypted using triple DES.
- Private key at least 2048 bits long.
- Contains all intermediate certificates in the certificate chain.
- Must meet TLS binding requirements:
  - Contains Extended Key Usage for server authentication.
  - Signed by a trusted certificate authority.

## Creating a Free Managed Certificate

- **Prerequisites**: App Service plan must be in Basic, Standard, Premium, or Isolated tier.
- **Features**: Fully managed TLS/SSL server certificate, automatically renewed by App Service.

## Importing an App Service Certificate

- **Description**: App Service Certificate purchased from Azure.
- **Features**: Azure manages purchase process, domain verification, certificate maintenance, renewal, and synchronization with App Service apps.

## Limitations of Free Managed Certificate

- Does not support wildcard certificates or private DNS.
- Not exportable.
- Not supported in an App Service Environment (ASE).
- Supports only alphanumeric characters, dashes (-), and periods (.).

## Conclusion

Configuring security certificates in Azure App Service is essential for ensuring secure communication between your app and users. By understanding the options available and meeting the requirements for private certificates, you can effectively implement certificate-based security measures to protect sensitive information transmitted over the network.
