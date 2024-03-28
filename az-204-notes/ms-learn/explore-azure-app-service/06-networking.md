# Understanding App Service Networking Features

**Overview:**
Azure App Service offers default internet accessibility for hosted applications, with options to manage inbound and outbound network traffic. This summary delves into the networking features provided by Azure App Service, addressing different deployment types and traffic control requirements.

**Multi-tenant App Service Networking:**

- Azure App Service functions as a distributed system, with front ends handling incoming requests and workers hosting customer workloads.
- Due to the multi-tenant nature, direct connection between App Service network and user networks isn't feasible.
- Instead, specialized features are utilized to manage application communication, offering distinct inbound and outbound functionalities.

**Inbound Features:**

- Inbound traffic control mechanisms include:
  - App-assigned address: Supports IP-based SSL needs and provides unshared dedicated inbound addresses.
  - Access restrictions: Allows restricting access to apps from specific addresses.
  - Service endpoints and private endpoints: Facilitate secure communication within Azure Virtual Networks.

**Outbound Features:**

- Outbound traffic from worker VMs is managed based on the App Service plan, with varying VM types for different plans.
- Outbound addresses used by apps for making calls are shared among apps on the same worker VM family.
- Outbound IP addresses can be found in app properties in the Azure portal or through Azure CLI commands.

**Finding Outbound IPs:**

- Outbound IP addresses utilized by the app can be accessed through app properties in the Azure portal or Azure CLI commands.
- Azure CLI commands enable retrieval of all possible outbound IP addresses, irrespective of pricing tiers.

These networking features empower users to efficiently control inbound and outbound traffic, ensuring secure and seamless communication for Azure App Service-hosted applications.
