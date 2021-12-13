##  ASP NET Core Identity tutorial from scratch

![Screen Shot 2021-12-02 at 2.25.11 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-02 at 2.25.11 pm.png)

IdentityDbContext inherits from DbContext

![Screen Shot 2021-12-02 at 3.08.13 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-02 at 3.08.13 pm.png)

![Screen Shot 2021-12-02 at 2.36.28 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-02 at 2.36.28 pm.png)

![Screen Shot 2021-12-02 at 2.37.05 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-02 at 2.37.05 pm.png)

![Screen Shot 2021-12-02 at 3.07.38 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-02 at 3.07.38 pm.png)

### Register new user 

This section create the View for user registration.



Step 1: Create RegisterViewModel -> apply model validation 

Step 2: Create AccountController 

Step 3: Create Account folder, then create Register.cshtml 

Step 4: Add a login nav link in the shared _Layout.cshtml

### User Manager and Signin Manager

![Screen Shot 2021-12-03 at 8.54.52 am](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-03 at 8.54.52 am.png)

![Screen Shot 2021-12-03 at 9.17.32 am](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-03 at 9.17.32 am.png)

### Password Complexity

password complexity can be configured in startup.cs

### Show or hide login and logout links based on login status in asp net core

Change the Razor view page, _Layout.cshtml file

### Implementing login functionality in asp net core

![Screen Shot 2021-12-03 at 9.58.03 am](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-03 at 9.58.03 am.png)

Step 1: create login view model

Step 2: create login view file -> login.cshtml

Step 3: create login action in account controller

![Screen Shot 2021-12-03 at 12.13.20 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-03 at 12.13.20 pm.png)

### Authorization in ASP NET Core

Limit edit and create employee actions to logged-in users.

Step 1: add [Authorize] to the actions which are needed to be protected. 

Step 2: add         [AllowAnonymous]

![Screen Shot 2021-12-03 at 12.38.25 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-03 at 12.38.25 pm.png)

![Screen Shot 2021-12-03 at 12.38.09 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-03 at 12.38.09 pm.png)

### Redirect user to original url after login in asp net core

![Screen Shot 2021-12-03 at 12.41.41 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-03 at 12.41.41 pm.png)

open redirect attack 

### Open redirect vulnerability example

![Screen Shot 2021-12-03 at 12.45.46 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-03 at 12.45.46 pm.png)

![Screen Shot 2021-12-03 at 12.49.30 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-03 at 12.49.30 pm.png)

![Screen Shot 2021-12-03 at 12.56.29 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-03 at 12.56.29 pm.png)

### Extend IdentityUser in ASP NET Core

If we want to store additional user data  like Gender, City, Country etc. 

![Screen Shot 2021-12-03 at 2.48.21 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-03 at 2.48.21 pm.png)

![Screen Shot 2021-12-03 at 3.25.20 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-03 at 3.25.20 pm.png)

### Creating roles in asp net core

#### Introduction

Step 1: create CreateRoleViewModel

Step 2: create AdministrationController and CreateRole action method

Step 3: create CreateRole.cshtml



![Screen Shot 2021-12-03 at 4.07.35 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-03 at 4.07.35 pm.png)

#### Get list of roles

![Screen Shot 2021-12-03 at 4.30.07 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-03 at 4.30.07 pm.png)

#### Edit role in asp net core



#### Add or remove users from role



![Screen Shot 2021-12-03 at 7.40.27 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-03 at 7.40.27 pm.png)

![Screen Shot 2021-12-03 at 7.40.58 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-03 at 7.40.58 pm.png)



EditUsersInRole action in administrationController

EditUsersInRole.cshtml

#### role based authorization

![Screen Shot 2021-12-04 at 12.56.35 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-04 at 12.56.35 pm.png)

![Screen Shot 2021-12-04 at 12.59.56 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-04 at 12.59.56 pm.png)

#### Show or hide navigation menu based on user role

![Screen Shot 2021-12-04 at 1.00.52 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-04 at 1.00.52 pm.png)

![Screen Shot 2021-12-04 at 1.17.18 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-04 at 1.17.18 pm.png)

#### Delete identity role in asp net core

#### Manage user roles

#### Manage user claims in asp net core

user claims == (name, value) pair used for access control.

#### Claims based authorization 

![Screen Shot 2021-12-05 at 1.00.37 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-05 at 1.00.37 pm.png)

#### Role based authorization vs claims based authorization in asp net core

![Screen Shot 2021-12-05 at 1.22.38 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-05 at 1.22.38 pm.png)

![Screen Shot 2021-12-05 at 1.23.05 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-05 at 1.23.05 pm.png)

![Screen Shot 2021-12-05 at 1.29.27 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-05 at 1.29.27 pm.png)

#### Authorization in views in asp net core mvc

![Screen Shot 2021-12-05 at 2.17.19 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-05 at 2.17.19 pm.png)

#### Claim type and claim value in claims policy based authorization

set claim value to true/false

#### Create custom authorization policy using func 

![Screen Shot 2021-12-05 at 3.13.07 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-05 at 3.13.07 pm.png)

![Screen Shot 2021-12-05 at 3.39.16 pm](/Users/rudy/Library/Application Support/typora-user-images/Screen Shot 2021-12-05 at 3.39.16 pm.png)

#### Custom authorization requirements and handlers

![Screen Shot 2021-12-05 at 3.47.31 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-05%20at%203.47.31%20pm.png?lastModify=1639111245)

![Screen Shot 2021-12-05 at 3.52.36 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-05%20at%203.52.36%20pm.png?lastModify=1639111245)

#### Custom authorization requirement and handler example 

![Screen Shot 2021-12-05 at 3.56.40 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-05%20at%203.56.40%20pm.png?lastModify=1639111245)

![Screen Shot 2021-12-05 at 4.22.08 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-05%20at%204.22.08%20pm.png?lastModify=1639111245)

![Screen Shot 2021-12-05 at 4.22.23 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-05%20at%204.22.23%20pm.png?lastModify=1639111245)

![Screen Shot 2021-12-05 at 4.22.42 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-05%20at%204.22.42%20pm.png?lastModify=1639111245)

#### Multiple custom authorization handlers for a requirement ![Screen Shot 2021-12-05 at 7.54.06 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-05%20at%207.54.06%20pm.png?lastModify=1639111245)

![Screen Shot 2021-12-05 at 7.56.24 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-05%20at%207.56.24%20pm.png?lastModify=1639111245)

### External identity providers 

#### Create google oauth credentials Client Id and Client Secret

![Screen Shot 2021-12-06 at 9.57.14 am](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-06%20at%209.57.14%20am.png?lastModify=1639111245)

![Screen Shot 2021-12-06 at 9.57.33 am](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-06%20at%209.57.33%20am.png?lastModify=1639111245)

![Screen Shot 2021-12-06 at 9.57.47 am](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-06%20at%209.57.47%20am.png?lastModify=1639111245)

#### google authentication setting up the UI



#### ExternalLoginCallback action in asp net core

####  Register application with facebook

#### facebook authentication

### ASP NET Core secret manager

![Screen Shot 2021-12-06 at 1.19.42 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-06%20at%201.19.42%20pm.png?lastModify=1639111245)

![Screen Shot 2021-12-06 at 1.39.44 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-06%20at%201.39.44%20pm.png?lastModify=1639111245)

### Email Confirmation

#### Why email confirmation is important

### ![Screen Shot 2021-12-06 at 1.55.24 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-06%20at%201.55.24%20pm.png?lastModify=1639111245)

#### Block login if email is not confirmed in asp net core

![Screen Shot 2021-12-06 at 2.39.30 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-06%20at%202.39.30%20pm.png?lastModify=1639111245)

![Screen Shot 2021-12-06 at 2.39.49 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-06%20at%202.39.49%20pm.png?lastModify=1639111245) 

####  email confirmation

![Screen Shot 2021-12-06 at 2.45.25 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-06%20at%202.45.25%20pm.png?lastModify=1639111245)

#### External login email confirmation in asp net core

![Screen Shot 2021-12-07 at 9.48.36 am](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-07%20at%209.48.36%20am.png?lastModify=1639111245)

### Forgot password in asp net core

![Screen Shot 2021-12-07 at 10.14.43 am](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-07%20at%2010.14.43%20am.png?lastModify=1639111245)

### Reset password in asp net core

![Screen Shot 2021-12-07 at 10.26.23 am](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-07%20at%2010.26.23%20am.png?lastModify=1639111245)



### How tokens are generated and validated in asp net core

![Screen Shot 2021-12-07 at 10.27.29 am](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-07%20at%2010.27.29%20am.png?lastModify=1639111245)

   ![Screen Shot 2021-12-07 at 10.38.45 am](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-07%20at%2010.38.45%20am.png?lastModify=1639111245)

![Screen Shot 2021-12-07 at 10.39.24 am](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-07%20at%2010.39.24%20am.png?lastModify=1639111245)

###  ASP NET Core password reset token lifetime

![Screen Shot 2021-12-07 at 11.05.40 am](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-07%20at%2011.05.40%20am.png?lastModify=1639111245)

![Screen Shot 2021-12-07 at 11.06.19 am](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-07%20at%2011.06.19%20am.png?lastModify=1639111245)

### ASP NET Core custom token provider

![Screen Shot 2021-12-07 at 11.15.42 am](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-07%20at%2011.15.42%20am.png?lastModify=1639111245)

![Screen Shot 2021-12-07 at 11.16.06 am](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-07%20at%2011.16.06%20am.png?lastModify=1639111245)

### ASP NET Core encryption and decryption example

![Screen Shot 2021-12-07 at 12.19.47 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-07%20at%2012.19.47%20pm.png?lastModify=1639111245)

 ![Screen Shot 2021-12-07 at 12.54.11 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-07%20at%2012.54.11%20pm.png?lastModify=1639111245)

### Change password in asp net core

![Screen Shot 2021-12-07 at 1.03.28 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-07%20at%201.03.28%20pm.png?lastModify=1639111245)

### Add password to local account linked to external login

Those user who loggin with external account do not have password 

![Screen Shot 2021-12-07 at 1.27.41 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-07%20at%201.27.41%20pm.png?lastModify=1639111245)

### ASP NET Core account lockout

![Screen Shot 2021-12-07 at 1.37.39 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-07%20at%201.37.39%20pm.png?lastModify=1639111245)

![Screen Shot 2021-12-07 at 1.40.20 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-07%20at%201.40.20%20pm.png?lastModify=1639111245)



### aEnforce ON DELETE NO ACTION in entity framework core

![Screen Shot 2021-12-04 at 7.29.03 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-04%20at%207.29.03%20pm.png?lastModify=1639111245)

![Screen Shot 2021-12-04 at 7.38.58 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-04%20at%207.38.58%20pm.png?lastModify=1639111245)



### List all users from asp net core identity database

![Screen Shot 2021-12-04 at 2.14.08 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-04%20at%202.14.08%20pm.png?lastModify=1639111245)

### Edit identity user in asp net core

### Delete identity user in asp net core

![Screen Shot 2021-12-04 at 2.55.32 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-04%20at%202.55.32%20pm.png?lastModify=1639111245)

### delete confirmation

![Screen Shot 2021-12-04 at 3.13.58 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-04%20at%203.13.58%20pm.png?lastModify=1639111245)

![Screen Shot 2021-12-04 at 3.14.21 pm](file:///Users/rudy/Library/Application%20Support/typora-user-images/Screen%20Shot%202021-12-04%20at%203.14.21%20pm.png?lastModify=1639111245)