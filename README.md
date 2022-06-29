# Title: Highly Available Web Layer and DB architecture
This template could be useful in quickly deploy the resources where you need VNet with predefined Subnets(Web, Management, Database & Bastion),Web VMs in HA(AvSet) with IIS Roles installed,Load Balancer for Web VMs with default Inbound IIS application configurations & Outbound configuration for internet access and Bastion Service for securely accessing Virtual Machines



# Solution overview and deployed resources. 
Layers are a way to separate responsibilities and manage dependencies. Each layer has a specific responsibility. A higher layer can use services in a lower layer, but not the other way around.

Tiers are physically separated, running on separate machines. A tier can call to another tier directly, or use asynchronous messaging (message queue). Although each layer might be hosted in its own tier, that's not required. Several layers might be hosted on the same tier. Physically separating the tiers improves scalability and resiliency, but also adds latency from the additional network communication.

A traditional three-tier application has a presentation tier, a middle tier, and a database tier.


## Target audience
Infrastructure Architect

Application Developer

IT Professional

Cloud Solution Architect

# Architecture

The [Template.json](https://github.com/nikhil7891/Highly-Available-Web-Layer-and-DB-architecture/blob/master/template.json) Azure Resource Manager template will help you automatically deploy the diagram below, which includes:

- Resource Group in preferred location.
- VNet with predefined Subnets(Web, Management, Database & Bastion)
- Web VMs in HA(AvSet) with IIS Roles installed.
- SQL VM  with 1 TB Data & 1 TB Log Disks.
- Load Balancer for Web VMs with default Inbound IIS application configurations & Outbound configuration for internet access.
- Bastion Service for securely accessing Virtual Machines.
- NSG for Web VM(with Port 80 rule) & Database VM.


![alt image](https://github.com/nikhil7891/Highly-Available-Web-Layer-and-DB-architecture/blob/master/Architecturedeployment.png)



[Template.json](https://github.com/nikhil7891/Highly-Available-Web-Layer-and-DB-architecture/blob/master/template.json) can be modified to match your current infrastructure needs.

## One Click Deploying Template
<!-- Powershell command for Translating Git URL for template.json
    $url = "https://raw.githubusercontent.com/nikhil7891/Highly-Available-Web-Layer-and-DB-architecture/master/template.json"
    [uri]::EscapeDataString($url)
>> uri = https%3A%2F%2Fraw.githubusercontent.com%2Fnikhil7891%2FHighly-Available-Web-Layer-and-DB-architecture%2Fmaster%2Ftemplate.json

Base URL: https://portal.azure.com/#create/Microsoft.Template/uri
Final URL: <Base URL>/<uri>
-->
[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fnikhil7891%2FHighly-Available-Web-Layer-and-DB-architecture%2Fmaster%2Ftemplate.json)



## Deploying an ARM Template using the Azure portal

- Visit https://portal.azure.com

- Allow 30 minutes for the deployment to complete

## Azure services and related products

The template will create following resources as per the standard naming conventions:-
1. Resource Group in preferred location.
2. VNet with predefined Subnets(Web, Management, Database & Bastion)
3. Web VMs in HA(AvSet) with IIS Roles installed.
4. SQL VM  with 1 TB Data & 1 TB Log Disks.
5. Load Balancer for Web VMs with default Inbound IIS application configurations & Outbound configuration for internet access.
6. Bastion Service for securely accessing Virtual Machines.
7. NSG for Web VM(with Port 80 rule) & Database VM.

## Deployment steps



## Related references
https://docs.microsoft.com/en-us/azure/architecture/guide/architecture-styles/n-tier

https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/n-tier/n-tier-sql-server

https://docs.microsoft.com/en-us/azure/architecture/high-availability/ref-arch-iaas-web-and-db




## License & Contribute

You are responsible for the performance, the necessary testing, and if needed any regulatory clearance for any of the models produced by this toolbox.
Please refer [LICENSE](LICENSE) &  [Contribute](https://github.com/Ganapathivarma07/LRS-Migration-AzureSQLMI/blob/master/Contribute.md) for more details


