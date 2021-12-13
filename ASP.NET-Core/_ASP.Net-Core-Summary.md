# Overview

If we want to build a simple CRUD website, we could use ASP.NET Core for achieving it.

Firstly, we learn about ==ASP.Net Core== which provide a simple HTTP server for building the web app.

Then, we look at the ==ASP.NET Core MVC== which provides a MVC pattern for building our web app in layers, this provides nice abstractions which means good maintainance ability. This is the main part for CRUD.

Thirdly, we have to save our data to disk. So, we learn about the ==Entity Framework Core==, so we can save our data.

Finally, we could add a user management system to our web app by utilizing the ==ASP.NET Core Identity== for authentication and authorization. 

So, the learning goal is able to use ASP.NET Core for CRUD web app.

- [x] Follow the video, and made a CRUD web app
- [x] Document the process of CRUD
  - [ ] Make them into Anki Cards
- [ ] Build a simple CRUD with myself

# ASP.NET CORE

## Environment Setup

[Environment setup](./Environment-Setup.md)

## Know the project files

[Project files](./Project-Files.md)

Explain all the files usage in the application folders

- .csproj project file
- lauchsettings.json
- appsettings.json
- How does the ASP.NET Core Application got initialized -> The main method -> Program.cs + Startup.cs (two files)
- ASPNETCORE_ENVIRONMENT used for choosing environment

Summary

- After knowing these stuff, I could inspect the configurations of an ASP.NET Core app from appsettings.json and .csproj file.

## Middleware Pipeline

[Middleware](./Middleware.md)

There is still more to be learnt in middleware.

1. What is middleware?
2. The order of middleware
3. Configure ASP.NET Core request processing pipeline

## Service Configuration with Dependency Injection

[Dependency Injection](./Dependency-Injection.md)

- Constructor injection
- Register service 
- dependency lifetime

## Publishing and deploying the application ??

## Monitoring and troubleshooting errors with logging

[Logging](./Logging.md)

- Built-in Logging Provider
- 3rd Party Logging Providers
- Log exceptions from a controller
  - ILogger
- Configure log level
- Log to file
- Log filtering
- ==Log Scope [还没学过]==
- ==Need to learn how the Logging API + Logging Provider works==

## Sercurity

## Error and Exception handling

[Error and Exception handling](./Error-and-Exception-Handling.md)

These are all about how to show the error and exception to the browser, that is let the user understand what is happening. 

- Developer Exception Page ==(Development only!==)
- Global Exception handling 
- Handle 404 Error
  - UseStatusCodePages
  - UseStatusCodePagesWithRedirects
  - UseStatusCodePagesWithReExecute

## Buliding Custom Components

## Testing the application

- xUnit
- Unit test

# ASP.NET CORE MVC

## Serve Web pages with MVC controller

[ASP,NET-Core-MVC](./ASP,NET-Core-MVC.md)

- What is MVC pattern?
- What is ASP.NET Core MVC?
- How to setup MVC in ASP.NET Core?
- AddMvc() VS AddMvcCore()
- Controller in ASP.NET Core MVC
- Model in ASP.NET Core MVC

## Routing

[Routing](./Routing.md)

- Conventional Routing
  - route template
  - MapControllerRoute()
  - MapControllerDefaultRoute()
- Attribute Routing
  - token replacement
  - HTTP verb templates
  - Combination of attribute routing
- Configure the routing of AccessDenied page

## Model Binding and Validation

[Model Binding and Validation](./Model-Binding-and-Validation.md)

- Definition of model binding
- Model binding target and source
- Model binding with for loop and foreach loop
- Definition of model validation
- How to do model validation in ASP.NET Core?
- How to do model validation for ==select list== in ASP.NET Core?
- How to move model validation from sever side to client side for perfromance concerns?
- What are the built-in validation attributes?
- How to build a custom validation attributes?
- What is **remote validation**? 

## Depedency Injection

 In ASP.NET Core MVC, [controllers](https://docs.microsoft.com/en-us/aspnet/core/mvc/controllers/dependency-injection?view=aspnetcore-6.0) can request needed services through their constructors, allowing them to follow the [Explicit Dependencies Principle](https://docs.microsoft.com/en-us/dotnet/standard/modern-web-apps-azure-architecture/architectural-principles#explicit-dependencies).

Your app can also use [dependency injection in view files](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/dependency-injection?view=aspnetcore-6.0), using the `@inject` directive:

```
@inject SomeService ServiceName

<!DOCTYPE html>
<html lang="en">
<head>
    <title>@ServiceName.GetTitle</title>
</head>
<body>
    <h1>@ServiceName.GetTitle</h1>
</body>
</html>
```

## Razor View for Frontend

[Views in ASP.NET Core](./Views.md)

- Definition of View
- How to create a view? 
- How does a controller specify a view?
- What is View discovery?
- Three ways to pass data to View
  - Strongly typed data
    - view model
  - Weakly typed data
    - ViewData
    - ViewBag
- What is Layout and how to use it?
- What is _ViewStart.cshtml?
- What is _ViewImport.cshtml?
- Hot to use loops in view?

- [Tag helpers](./Tag-Helper.md)
  - Definition of tag helper
  - How to use tag helper
  - Built-in tag helpers
    - ==redirect== + image referencing + environment variable + ==form creation==

## The MVC filter pipeline ??

# Entity Framework Core

## Saving data with Entity Framework Core

[Entity Framework Core](./Entity-Framework-Core.md)

- install driver for database
- configure database connection string
- Use EF Core in ASP.NET Core
  - DbContext
  - DbSet
- data seeding 
- migration

# ASP.NET CORE Identity

## Authetication and Authorization with ASP.NET Core Identity 

[ASP.NET Core Identity](./ASP.NET-Core-Identity.md)

