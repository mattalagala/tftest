

<!-- ABOUT THE PROJECT -->
# Interac Landing Zone Deployment on Azure Stack Hub

<!-- [![Product Name Screen Shot][product-screenshot]](https://example.com) -->

## Summary 

Deploy Landing Zone foundational resources to the Azure Stack Hub environment.

## Folder Structure

The repo contains nested files in several folders. 

#### DATA Folder
* Contains the input *.csv files for this package. Each module receives its input parameters from these files and creates a map object to deploy resources based on the number of map elements. 

#### LZ_MODULES Folder
* Contains the invidual Azure Stack Hub components for the Landing Zone. This includes Resource Groups, NSG, NSG Rules, Virtual Networks, Virtual Network Peering, Subnets, Key Vault, RBAC Policies and Storage Account.

#### LZ_MODULES Sub Folders
* These are the Azure Stack Hub components which are called individually by the "main.tf" file in the root directory. These components can be used individually to deploy singular resoures, but the recommended method is to deploy everyting through the "main.tf" file. 

### Technologies

Majority of the repo is written in the HashiCorp Configuration Language (HCI) but it also contains a few Azure Resource Manager (ARM) templates to deploy reources not supported by the HashiCorp provider.  

* [HCL](https://www.terraform.io/docs/language/syntax/configuration.html)
* [ARM Templates](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/overview)

<!-- GETTING STARTED -->
## Getting Started

The script requires Terraform to be installed or referenced locally. 

### Download

* [Terraform Download](https://www.terraform.io/downloads.html)

### Installation
Choose the appropriate OS you are deploying from (ex: Windows or Linux VM)
* [Terraform Installation](https://learn.hashicorp.com/tutorials/terraform/install-cli?in=terraform/azure-get-started)


#### Windows

1. Download the Terraform binary for Windows from the above link:
2. Move the binary to a local folder ex. **C:/tools/terraform/**
3. Set **C:/tools/terraform/** in your **Environment Variables**. 
4. Validate your installation by running the following commands and verifying that the Terraform version you installed is displaying. 
```sh 
C:\Users\user> terraform -v
```

#### Linux

1. Download the Terraform binary for Linux from the above link:

2. List out the locations in your **PATH** directory.
```sh 
$ echo $PATH
```
3. Assuming you have downloaded to the "downloads" folder, move the binary to **/usr/local/bin**. 
```sh 
$ mv ~/Downloads/terraform /usr/local/bin/
```
4. Set your **PATH** variable: 
```sh 
$ export PATH=$PATH:/usr/local/bin/
```
5. Validate your installation by running the following commands and verifying that the Terraform version you installed is displaying. 
```sh 
$ terraform -v
```


<!-- USAGE EXAMPLES -->
## Usage

### Running Terraform
1. Clone the repo:
```sh 
$ git clone <path>
```
2. On your local machine run to initialize the local Terraform directory.
```sh 
$ terraform init
```
3. Run the terraform plan command to plan out the current deployment to a state file. 
```sh 
$ terraform plan -out state
```
_Since Terraform is a declaritive technology, "state" is where Terraform will hold the current script configuration so that we can later deploy that "state". The plan command runs a scenario of how the current automation will deploy as, but does not actually apply it._

4. Run the Terraform apply command to apply the current state. 
```sh 
$ terraform apply state
```
_This will take the same "state" file from the previous plan stage and deploy the resources to Azure Stack Hub._

### Destroying the current state
1. Run the terraform plan command again to create a separate file to store the planned destroy state. 
```sh 
$ terraform plan -destroy -out destroy
```
_Like the previous plan command, this plan will generate a state file called "destroy" which will store the planned destruction of resources from Azure Stack Hub._

2. Run the Terraform apply "destroy" command to apply the current destroy state. 
```sh 
$ terraform apply destroy
```
_This will cause the previously created resources to be destroyed._


Please visit the link below for basic commands in Terraform:
* [Terraform Basic CLI Commands](https://www.terraform.io/docs/cli/commands/index.html)



<!-- ACKNOWLEDGEMENTS -->
## Helpful Tools
* [Visual Studio Code](https://code.visualstudio.com/)

