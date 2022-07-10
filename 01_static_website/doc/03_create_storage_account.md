# Reference

<https://itnext.io/the-only-guide-you-need-for-a-static-website-in-azure-part-2-host-your-static-site-in-azure-9114b7069db2>

# Work
 
## Create resource group

<https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/overview#resource-groups>

``` az group create \--name gatsby-azuredevops-rg \--location southeastasia ```

![Text Description automatically generated](./images/03/media/image1.png)

### Check the group in the Azure Portal

![Graphical user interface, text, application, email Description automatically generated](./images/03/media/image2.png) 

![Graphical user interface, text, application, email Description automatically generated](./images/03/media/image3.png) 

## Create Storage Account

``` az storage account create \--name gatsbyazuredevopssa \--resource-group gatsby-azuredevops-rg \--location southeastasia \--sku Standard_LRS ```

![Text Description automatically generated](./images/03/media/image4.png) 

![Text Description automatically generated](./images/03/media/image5.png) 

### Check in the Azure Portal

![Graphical user interface, text, application, email Description automatically generated](./images/03/media/image6.png) 

## Enabling Static Website Feature

### Now you have a storage account, you need to enable the static website feature. You can do that by executing the following command

``` az storage blob service-properties update \--account-name gatsbyazuredevopssa \--static-website \--404-document 404.html \--index-document index.html```

![Text Description automatically generated](./images/03/media/image7.png) 

![Text Description automatically generated](./images/03/media/image8.png) 

### Check in the Azure Portal

![Graphical user interface, application Description automatically generated](./images/03/media/image9.png) 

## Details configuration

![Graphical user interface, text, application, email Description automatically generated](./images/03/media/image10.png) 
