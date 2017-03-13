# ProjectA
this template allows you to deploy a simple Windows or Linux VM for using the Infrastructure Pattern Template CVM1, CVM2, CVM3, CVM4 and CVM5.

The Infrastructure Pattern Template CVM1 can either deploy a new or attach to an existing Storage Account, create a new or attach to an existing Virtual Network with 1 subnet and one Standard_A0 size VM with OS and Data Disk.

The Infrastructure Pattern Template CVM2 can either deploy a new or attach to an existing Storage Account, create a new or attach to an existing Virtual Network with 1 subnet and one Standard_A1 size VM with OS and Data Disk.


The Infrastructure Pattern Template CVM3 can either deploy a new or attach to an existing Storage Account, create a new or attach to an existing Virtual Network with 1 subnet and one Standard_A2 size VM with OS and Data Disk.


The Infrastructure Pattern Template CVM4 can either deploy a new or attach to an existing Storage Account, create a new or attach to an existing Virtual Network with 1 subnet and one Standard_A3 size VM with OS and Data Disk.

The Infrastructure Pattern Template CVM5 can either deploy a new or attach to an existing Storage Account, create a new or attach to an existing Virtual Network with 1 subnet and one Standard_D1 size VM with OS and Data Disk.

## Usage

Click on the **Deploy to Azure** button below. This will open the Azure Portal (login if necessary) and start a Custom Deployment. The following Parameters will be shown and must be updated / selected accordingly. 

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fdrameshdba%2FProjectA%2Fmaster%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>

baseUrl

Select the appropriate Repository Base URL containing Pattern Templates and Resource Templates
Default is 'https://raw.githubusercontent.com/mrptsai/'.
patternName

Select the appropriate Infrastructure Pattern.
Default is 'CVM1'.
Valid patternName's are:
     1 -cvm1  (Creates a single VM with a new or existing Storage Account and a new or existing Virtual Network)
     2 -cvm2  (Creates a single VM with a new or existing Storage Account and a new or existing Virtual Network)
     3 -cvm3  (Creates a single VM with a new or existing Storage Account and a new or existing Virtual Network)
     4 -cvm4  (Creates a single VM with a new or existing Storage Account and a new or existing Virtual Network)
     5 -cvm5  (Creates a single VM with a new or existing Storage Account and a new or existing Virtual Network)

Enter a unique Name for a new Storage Account or specify the name of an existing Storage Account. Use PowerShell and the following command to generate a unique Storage Account Name:
  storage + (-join ((48..57) + (97..122) | Get-Random -Count 15 | % {[char]$_}))
storageNewOrExisting

Is the Storage Account New or Existing?
Allowed Values are:
     1 - new
     2 - existing
storageExistingResourceGroup

Specify the existing Storage Resource Group. Leave blank if creating a new Storage Account.
Default is '' unless overridden.
virtualNetworkName

Enter a Name for a Virtual Network or specify the name of an existing Virtual Network.
virtualNetworkNewOrExisting

Is the Virtual Network New or Existing?
Allowed Values are:
     1 - new
     2 - existing
virtualNetworkExistingResourceGroup

Specify the existing Virtual Network Resource Group. Leave blank if creating a new Virtual Network.
Default is '' unless overridden.
virtualNetworkPrefix

Specify the Virtual Network Prefix to create or to be used
Default is '10.0.0.0/24' unless overridden.
subnet0Prefix

Specify the Subnet Prefix for the Management Tier
Default is '10.0.0.0/26' unless overridden.
subnet0Name

Specify the Subnet name for the Management Tier to create or to be used
Default is 'vm-subnet' unless overridden.
vmAdminUserName

Specify the VM local Logon Account that will have Administration Privileges.
Default is 'testuser' unless overridden.
vmAdminPassword

Enter a Password for the local Administration Account.
Default is 'P@ssword1Password2' unless overridden.
vmCount

Select the number of Virtual Machine you want to deploy.
Default is 1 unless overridden.
Allowed Values are:
     1
     2
     3
     4
vmType

Select the Operating System to deploy on the Virtual Machine(s). 0 = Windows, 1 = Linux
Default is 0 (Windows) unless overridden.
Allowed Values are:
     0 (Windows)
     1 (Linux)

Prerequisites

Access to Azure

Versioning

We use http://github.com/ for version control.

Authors

Ramesh Babu, Donti - Initial work - Project
