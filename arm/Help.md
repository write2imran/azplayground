# Run following command

az deployment group create --resource-group aztemplate --parameters language=".net" helloWorld="true" webAppName="armquickstartapp"
--template-file "./arm/quickstart-template.json"

- Browse the application
- Home > Resoure Group -> aztemplate -> AppServicePlan-armquickstartapp -> armquickstartapp -> Browse
