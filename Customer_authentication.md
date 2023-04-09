# Customer Authentication API

The Customer Authentication API is a RESTful API that allows customers to securely authenticate themselves to access their accounts or perform specific actions within an application or website. The API provides several endpoints that allow customers to register for a new account, log in to an existing account, reset their password, and log out.

| Method | Function   |
|-------:|------------|
|   Post | register |
|    Get | login     |
|  Get | logout |


## Register

To use the platform's services, customers must create a new account by registering with their email address and creating a secure password . The registration process is simple and easy to follow.

Post :  https://trojena.oa.r.appspot.com/authentication/store/register

|   Parameter | Type         | Example           |
|------------:|--------------|-------------------|
|  email | String          | mohamed@gmail.com |
| password | String | Mo12345678        |
|  firstName | String       | mohamed           |
|  lastName | String         | khaled            |

Example request:
```
Post /authentication/store/register
```
Example response:

```
HTTP/1.1 200 OK
Content-Type: application/json

{
   message: successfully registered
}
```

## Login

To log in, users can navigate to the "login" page and enter their email address and password. The system may also require additional security measures such as two-factor authentication. Once the user submits the login form, the system will verify the credentials and grant access to the website services.

Get :  https://trojena.oa.r.appspot.com/authentication/store/login

|   Parameter | Type                  | Example |
|------------:|-----------------------|---------|
|  email | String              | mohamed@gmail.com       |
|  password | String              | Mo12345678       |

Example request:
```
Get /authentication/store/login
```
Example response:

```
HTTP/1.1 200 OK
Content-Type: application/json

{
   message: Logged in successfully
}
```

## Logout

To ensure the security of your account and personal information, it is recommended that you log out after using the website services.

Get :  https://trojena.oa.r.appspot.com/authentication/store/logout

|   Parameter | Type                   | Example |
|------------:|------------------------|---------|
|  No information required      |

Example request:
```
Get /authentication/store/logout
```
Example response:

```
HTTP/1.1 200 OK
Content-Type: application/json

{
   message: operation accomplished successfully
}
```
