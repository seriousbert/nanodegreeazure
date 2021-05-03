Article CMS (FlaskWebProject)
This project is a Python web application built using Flask. The user can log in and out and create/edit articles. An article consists of a title, author, and body of text stored in an Azure SQL Server along with an image that is stored in Azure Blob Storage. You will also implement OAuth2 with Sign in with Microsoft using the msal library, along with app logging.

Log In Credentials for FlaskWebProject
Username: admin
Password: pass
Or, once the MS Login button is implemented, it will automatically log into the admin account.

Project Instructions (For Student)
You are expected to do the following to complete this project:

Create a Resource Group in Azure.
Create an SQL Database in Azure that contains a user table, an article table, and data in each table (populated with the scripts provided in the SQL Scripts folder).
Provide a screenshot of the populated tables as detailed further below.
Create a Storage Container in Azure for images to be stored in a container.
Provide a screenshot of the storage endpoint URL as detailed further below.
Add functionality to the Sign In With Microsoft button.
This will require completing TODOs in views.py with the msal library, along with appropriate registration in Azure Active Directory.
Choose to use either a VM or App Service to deploy the FlaskWebProject to Azure. Complete the analysis template in WRITEUP.md (or include in the README) to compare the two options, as well as detail your reasoning behind choosing one or the other. Once you have made your choice, go through with deployment.
Add logging for whether users successfully or unsuccessfully logged in.
This will require completing TODOs in __init__.py, as well as adding logging where desired in views.py.
To prove that the application in on Azure and working, go to the URL of your deployed app, log in using the credentials in this README, click the Create button, and create an article with the following data:
Title: "Hello World!"
Author: "Jane Doe"
Body: "My name is Jane Doe and this is my first article!"
Upload an image of your choice. Must be either a .png or .jpg. After saving, click back on the article you created and provide a screenshot proving that it was created successfully. Please also make sure the URL is present in the screenshot.
Log into the Azure Portal, go to your Resource Group, and provide a screenshot including all of the resources that were created to complete this project. (see sample screenshot in "example_images" folder)
Take a screenshot of the Redirect URIs entered for your registered app, related to the MS Login button.
Take a screenshot of your logs (can be from the Log stream in Azure) showing logging from an attempt to sign in with an invalid login, as well as a valid login.
example_images Folder
This folder contains sample screenshots that students are required to submit in order to prove they completed various tasks throughout the project.

article-cms-solution.png is a screenshot from running the FlaskWebProject on Azure and prove that the student was able to create a new entry. The Title, Author, and Body fields must be populated to prove that the data is being retrieved from the Azure SQL Database while the image on the right proves that an image was uploaded and pulled from Azure Blob Storage.
azure-portal-resource-group.png is a screenshot from the Azure Portal showing all of the contents of the Resource Group the student needs to create. The resource group must (at least) contain the following:
Storage Account
SQL Server
SQL Database
Resources related to deploying the app
sql-storage-solution.png is a screenshot showing the created tables and one query of data from the initial scripts.
blob-solution.png is a screenshot showing an example of blob endpoints for where images are sent for storage.
uri-redirects-solution.png is a screenshot of the redirect URIs related to Microsoft authentication.
log-solution.png is a screenshot showing one potential form of logging with an "Invalid login attempt" and "admin logged in successfully", taken from the app's Log stream. You can customize your log messages as you see fit for these situations.
Dependencies
A free Azure account
A GitHub account
Python 3.7 or later
Visual Studio 2019 Community Edition (Free)
The latest Azure CLI (helpful; not required - all actions can be done in the portal)
All Python dependencies are stored in the requirements.txt file. To install them, using Visual Studio 2019 Community Edition:

In the Solution Explorer, expand "Python Environments"
Right click on "Python 3.7 (64-bit) (global default)" and select "Install from requirements.txt"
