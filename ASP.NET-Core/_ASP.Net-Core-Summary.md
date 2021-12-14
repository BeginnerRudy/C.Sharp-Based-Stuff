# Overview

If we want to build a simple CRUD website, we could use ASP.NET Core for achieving it.

Firstly, we learn about ==ASP.Net Core== which provide a simple HTTP server for building the web app.

Then, we look at the ==ASP.NET Core MVC== which provides a MVC pattern for building our web app in layers, this provides nice abstractions which means good maintainance ability. This is the main part for CRUD.

Thirdly, we have to save our data to disk. So, we learn about the ==Entity Framework Core==, so we can save our data.

Finally, we could add a user management system to our web app by utilizing the ==ASP.NET Core Identity== for authentication and authorization. 

So, the learning goal is able to use ASP.NET Core for CRUD web app.

- [x] Follow the video, and made a CRUD web app
- [x] Document the process of CRUD
  - [x] Make them into Anki Cards
- [ ] Build a simple CRUD with myself

# ASP.NET CORE

## Overview

ASP.NET Core helps developer to build web applications. The fundamental contains 

- the basic configuration files
- how the main method start ASP.NET Core application
- middleware pipeline to handle the request from client
- IoC with dependency injection
- Logging
- Error and Exception Handling

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

## Overview

MVC pattern is a way to architect our web app, ASP.NET Core MVC helps developers to build MVC-based web app. The concepts of ASP.NET Core MVC can be orgnaized by the process of it processing a HTTP request. 

Step 0: We ==add the MVC to the request pipeline== to enable MVC pattern on our server. 

Step 1: The request comes in, so the ==routing system== needs to find a matched controller to deal with it.

Step 2: The controller is found, then we need to do ==model binding== to convert the request data to parameters and pass it to the controller.

Step 3: After the model is binded, we need to perform ==model validation== as well for checking constraints. 

Step 4: Then, the controller get called, it find appropriate model and select view and ==pass data to View== to render.

Step 5: ==Some View related knowledge==

Step 6: The browser get View and render it to show the user.

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

## Overview

This is an ORM framework and the key takeaway are 

- DbContext == a database 
- DbSet == a table

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

## Overview

The key class in this API are 

- Data manager class
  - UserManager
  - SignInManager
- Data model class
  - `IdentityRole`
  - `IdentityRoleClaim`
  - `IdentityUser`
  - `IdentityUserClaim`
  - `IdentityUserLogin`
  - `IdentityUserRole`
  - `IdentityUserToken`

Authentication

- Register & signing & logout with UserManager + SignInManager

Authorization

- Simple/Role-based/Claim-based/Policy-based
- Authorization attributes
  - [Authorize]
  - [AollowAnonymous]

## Authetication and Authorization with ASP.NET Core Identity 

[ASP.NET Core Identity](./ASP.NET-Core-Identity.md)

- How to use ASP.NET Core Identity?

  - IdentityDbContext
  - Add Identity Service
  - Add Authetication Middleware
  - Generate Identity tables in the database

- Register new user

- UserManager

  - CreateAsync
  - DeleteAsync
  - UpdateAsync
  - Etc...

- SignInManager

  - SignInAsync
  - SignOutAsync
  - IsSignedIn
  - Etc...

- Password complexity configuration

- Login a user

- Redirect user to original url after login and prevent open redirect attacks

- Authorization

  - Role based Authorization
    - CRUD roles -> IdentityRole class
    - Add/Remove IdentityUser to Identity Role
    - How to do role based authentication?
      - [Authorize(Role = "Role1,Role2")] -> Role1 or Role2 can have access

  

  ```c#
  [Authorize(Role = "Role1")]
  [Authorize(Role = "Role2")]
  public void actionMethod();
  
  Need to be both Role1 and Role2 to have access
  ```

  

  - Claim based Authorization
    - Definition of User Claim -> user claims == (name, value) pair used for access control.
    - Manage User Claim
    - How to perform Claim based Authorization
      - Create Claim Policy in startup.cs
      - Use the policy for authorization checks -> [Authorize(Policy = "PolicyName")]
      - Claim type and claim value
  - Policy based Authorization
  - [Authorize] or [AllowAnonymous]

- Extend IdentityUser for additional property

- Authorizatioin in views via dependency injection

- External identity providers

- Email Confirmation

- Forget password and reset password
