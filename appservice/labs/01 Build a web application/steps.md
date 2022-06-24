# Steps to create Web Application

This sample consists of three main component

1. Stroge Account that holds images in a publicaly accessible blob container
2. Web App as a REST API, it returns path of the image stored in the container and also has rest point which allows to upload the image
3. Web App as a client, it is a client app which talks with REST API

### Create Group and storage account

- Create a resource group (not necessary web app should be in the same resource group)
- Create a storage account
- Create a Container and upload the image (grilledcheese.jpg)

### Create Web App for API that returns the image url from container

- Create a Web App ASP .Net Core 3.1 with S1 Plan
- Access the Web App https://<webappname>.azurewebsites.net
- Create new application setting, provide key as "StorageConnectinoString" and value from one of storage account connection setting
- Open the Sample application folder /labs/01/starter/api
- Deploy api.zip file to web app ( az webapp deployment source config-zip --resource-group ManagedPlatform --src api.zip --name imgapiimranrauf01)
- Browse the newly deployed app (it returns the path of the image (from container images) at root '/' url )

### Create Web App for accessing the API and display the image

- Create a Web App ASP .Net Core 3.1 with S1 Plan
- Open the sample application folder /labs/01/starter/web
- Configure the Web app "ApiUrl" settings, provide url of the above api application
- Deploy web.zip file to web app ( az webapp deployment source config-zip --resource-group ManagedPlatform --src web.zip --name imgwebimranrauf01)
