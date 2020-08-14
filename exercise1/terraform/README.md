
Create an environment with 2 machines.

This repository which is mainly for creating the vitural machine in Azure platform. This code will create 2 private VM and 1 public connected VM (For login purpose)

Before you starting this you need to learn basic thing for Azure and create one new account in Azure platform by using following link https://azure.microsoft.com/en-us/free/ for leaning purpose.

Once you created the Azure account, We need to do some basic setup for connecting Azure api by using terraform script. Please follow the link https://www.terraform.io/docs/providers/azurerm/guides/azure_cli.html for basic setup.

Also Please install the terraform on your local or where you are going to execute the terraform script. You can use the following link to install terraform https://www.terraform.io/downloads.html

Now every thing is done. Let me explain about the code.

Well.. In oder to create VM, we need to create some basic resources to full fill the infrasturacture.

1. Resouce Group.
2. Virtual Network.
3. Subnet's.
4. Network Interface.
5. Public ip's
6. In this code all the resources created as module. So the main idea is to reuse the code for multiple infrasturacture.

experiment/exercise1/terraform/main.tf & experiment/exercise1/terraform/variables.tf These files will change the each infrasturacture, other will be the same.

How to run the terraform code?

1. First clone this repo into your local
2. Navigate intoexperiment/exercise1/terraform folder.
3. First you need to initialized the terraform module by using the following command 
    "terraform init"
4. If you what to view the outcome of this code, you need to run the following commmand 
    "terraform plan"
5. Creating the VM, Please run the below command. 
    "terraform apply auto-approve "
    
** This will ask to user to provide the subscription_id and tenant_id. Since it's secure one that's why i'm getting from user. May be we have multiple motthod for apply the terraform. But i'm using this method.
