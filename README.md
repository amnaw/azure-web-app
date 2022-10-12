Creating an App Service

steps to create an App Service Web App using the Azure Portal

On the homepage, click "Create a resource"
Search for "Web App"
Click "Create"
Select your subscription
Select your resource group "resource-group-west"
Enter a name for your web app—This needs to be a unique name and is unique to Azure as a whole and not just your Azure account. I used "hello-world1234" as my unique name.
For Publish, select "Code"
For the "Runtime Stack", select "Python 3.7" or greater.
For the "Operating System" select "Linux"
Select a region for your app service
Create a new App Service Plan. You can keep the default name Azure gives you or you can create your own name.
For SKU and size, select "F1" (Free).
Click "Review + Create"
Click "Create"

To deploy an App Service from a GitHub repository, I did the following:

Go to Deployment Center
Choose GitHub
Choose org and repo
Go through the prompts; deployment takes a few minutes
Go to URL of web app and should see the app deployed

-------------------------------

Troubleshooting:

If your app shows "Application Error"
- make sure it runs locally fine
- cd web
- run "pip freeze > requirements.txt"
- pull & push to Github repo to trigger the re-deployment pipeline
- if build fail, read the build error message in Github action
- in case of dependencies issue in requirements, update the correct package versions (ex. python-dateutil==2.6.0 TO python-dateutil==2.7.3)
