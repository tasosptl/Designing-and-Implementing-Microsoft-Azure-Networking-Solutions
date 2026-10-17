# Azure Network Engineer Book - Chapter 8

The web VM public IP uses static allocation so that its address is assigned when
the public IP resource is created and is available to the `PublicWebVM` deployment
output. Dynamic allocation can leave `ipAddress` absent when that output is
evaluated, causing `DeploymentOutputEvaluationFailed`.

This template retains the Basic public IP SKU for the existing lab. Basic SKU
public IPs were retired on September 30, 2025; this change does not migrate the
lab to Standard SKU or restore support for new Basic SKU deployments.

[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fdavidokeyode%2FAZ-700%2Fmain%2Fchapter-8%2Ftemplate%2Fazuredeploy.json)
[![Visualize](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true)](http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fdavidokeyode%2FAZ-700%2Fmain%2Fchapter-8%2Ftemplate%2Fazuredeploy.json)


## CoreServicesVNet (10.10.0.0/16)
* **PublicWebServiceSubnet (10.10.3.0/24)**
  * WebVM (10.10.3.4)
 
## EngineeringVNet (10.20.0.0/16)
* **EngSubnet1 (10.20.1.0/24)**
* **EngSubnet2 (10.20.2.0/24)**
