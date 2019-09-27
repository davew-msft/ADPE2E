# Deploy Azure Data Platform End2End to your subscription

In this section you will automatically provision all Azure resources required to complete labs 1 though to 5. We will use a pre-defined ARM template with the definition of all Azure services used to ingest, store, process and visualise data. 

The estimated time to complete this lab is: 30 minutes.

## Prepare your Azure subscription

1. [Login to Azure](https://portal.azure.com)
2. Create a Resource Group called `MDW-Lab` or similar.  The remainder of the instructions assume `MDW-Lab`.  
3. When you choose a region try to pick one of the below recommended regions.  To avoid deployment error when services are not available in the region selected, please use one of the recommended regions.  **Remember which region you choose**.  

    Recommended Regions|
    -------------------|
    US East |
    US East 2| 
    US Central| 
    US West 2 |
    Europe West| 
    Asia Southeast| 
    Europe North |
    US South Central| 
    US West |
    UK South |
    Australia East| 
    Canada Central |
    Japan East |
    Germany Central |
    France Central |
    India Central |
    Brazil South |
    Korea Central |
    Korea South |


--------------------------------------
## Deploy Azure Services
In this section you will use automated deployment and ARM templates to automate the deployment of all Azure Data Services used in labs 1 through to 5.

1. You can deploy all Azure services required in each lab by clicking the **Deploy to Azure** button below. 

    [![Deploy to Azure](https://azuredeploy.net/deploybutton.png)](https://azuredeploy.net/)

2. On the **Deploy to Azure - Setup** page provide:
    <br>- Your organisation directory
    <br>- The subscription you want to use
    <br>- The resource group you created in the previous section

    ![](./Media/Lab0-Image06.png)

3. Click **Next**

4. On the **Deploy to Azure - Preview** just click **Deploy**

    ![](./Media/Lab0-Image07.png)

5. On the Azure Portal, navigate to your resource group.

6. On the **Overview** panel, click on the **Deployments** link to follow the progress of your deployment. A successful deployment should last less than 10 minutes.

    ![](./Media/Lab0-Image08.png)

7. Once your deployment is complete you are ready to start your labs. Enjoy!

    ![](./Media/Lab0-Image09.png)