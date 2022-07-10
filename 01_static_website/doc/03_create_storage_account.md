# Reference

<https://itnext.io/the-only-guide-you-need-for-a-static-website-in-azure-part-2-host-your-static-site-in-azure-9114b7069db2>

# Create resource group

<https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/overview#resource-groups>

az group create \--name gatsby-azuredevops-rg \--location southeastasia

![Text Description automatically
generated](./images/03/media/image1.png){width="6.5in"
height="2.0972222222222223in"}

Check the group in the Azure Portal

![Graphical user interface, text, application, email Description
automatically generated](./images/03/media/image2.png){width="6.5in"
height="2.4229166666666666in"}

![Graphical user interface, text, application, email Description
automatically generated](./images/03/media/image3.png){width="6.5in"
height="3.3097222222222222in"}

# Create Storage Account

az storage account create \--name gatsbyazuredevopssa \--resource-group
gatsby-azuredevops-rg \--location southeastasia \--sku Standard_LRS

![Text Description automatically
generated](./images/03/media/image4.png){width="6.5in"
height="3.3291666666666666in"}

![Text Description automatically
generated](./images/03/media/image5.png){width="6.5in"
height="3.372916666666667in"}

Check in the Azure Portal

![Graphical user interface, text, application, email Description
automatically generated](./images/03/media/image6.png){width="6.5in"
height="3.810416666666667in"}

# Enabling Static Website Feature

Now you have a storage account, you need to enable the static website
feature. You can do that by executing the following command

az storage blob service-properties update \--account-name
gatsbyazuredevopssa \--static-website \--404-document 404.html
\--index-document index.html

![Text Description automatically
generated](./images/03/media/image7.png){width="6.5in"
height="3.277083333333333in"}

![Text Description automatically
generated](./images/03/media/image8.png){width="6.5in"
height="3.477777777777778in"}

Check in the Azure Portal

![Graphical user interface, application Description automatically
generated](./images/03/media/image9.png){width="6.5in"
height="4.116666666666666in"}

Details configuration

![Graphical user interface, text, application, email Description
automatically generated](./images/03/media/image10.png){width="6.5in"
height="3.622916666666667in"}
