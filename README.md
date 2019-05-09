# MVCMovie (A dotnet core 2.2 mvc project)

## To Use This project basically you need these 3 things below:
1. Visual Studio Code
2. .NET Core SDK 2.2 or later
3. C# for Visual Studio Code version 1.17.1 or later

## Some useful dotnet cli commands below that is using to create this project:
1. dotnet new mvc -o MvcMovie 
(creates a new ASP.NET Core MVC project in the MvcMovie folder.)
2. code -r MvcMovie 
(Loads the MvcMovie.csproj project file in Visual Studio Code)

A dialog box appears with Required assets to build and debug are missing from 'MvcMovie'. Add them? Select Yes

Trust the HTTPS development certificate by running the following command:
3. dotnet dev-certs https --trust
Select Yes if you agree to trust the development certificate

These two commands required to add packages  for sqlite and  scaffolding.
4. dotnet add package Microsoft.EntityFrameworkCore.SQLite
5. dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design

Install the scaffolding tool:
6. dotnet tool install --global dotnet-aspnet-codegenerator

Run the following command:
7. dotnet aspnet-codegenerator controller -name MoviesController -m Movie -dc MvcMovieContext --relativeFolderPath Controllers --useDefaultLayout --referenceScriptLibraries

The following table details the ASP.NET Core code generator parameters:

Parameter	Description
-m	The name of the model.
-dc	The data context.
-udl	Use the default layout.
--relativeFolderPath	The relative output folder path to create the views.
--useDefaultLayout	The default layout should be used for the views.
--referenceScriptLibraries	Adds _ValidationScriptsPartial to Edit and Create pages

Use the h switch to get help on the aspnet-codegenerator controller command:
8. dotnet aspnet-codegenerator controller -h

Run the following .NET Core CLI commands:
9. dotnet ef migrations add InitialCreate  
(MigrationName:sample as InitialCreate, The ef migrations add InitialCreate command generates code to create the initial database schema)
10. dotnet ef database update

For remove a migration you can use also:
11. dotnet ef migrations remove

## For checking Sqlite you can use  (DB Browser for SQLite) or SQLite VS Code extension.
