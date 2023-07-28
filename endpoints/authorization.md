



# **Authorization**

The api allows for authentication with both email/password and the google Oauth2.

The api then uses jwt tokens for authorization.

Note that when a user signups with email/password they can then use an oauth proviter to login to their accounts

## <span class="get method">get</span> **Google Oauth2**

Starts the google oauth2 login process, this will redirect to a page that is handled by google.
At the end the auth returns either a jwt token or an exception.

`https://api.leem.it/v1/auth/google`

<details>
<summary>Response</summary>

<span class="get round"></span> **200: OK**

```json
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIn0.dozjgNryP4J3jVmNHl0w5N_XgL0n3I9PlFUP0THsR8U"
}
```
<span class="delete round"></span> **401: Unauthorized**

```json
{
    "error": "Google Oauth exception"
}
```


</details>

## <span class="post method">post</span> **SignUp**

Simple email/password signup

`https://api.leem.it/v1/auth/signup`

|name|type|in|required|
| :---: | :---: | :---: | :---: |
|name|`string`|body|True|
|email|`string`|body|True|
|password|`string`|body|True|

<details>
<summary>Response</summary>

<span class="get round"></span> **200: OK**

```json
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIn0.dozjgNryP4J3jVmNHl0w5N_XgL0n3I9PlFUP0THsR8U"
}
```
<span class="delete round"></span> **401: Unauthorized**

```json
{
    "error": "user is not authenticated"
}
```


</details>

## <span class="post method">post</span> **LogIn**

Simple email/password login

`https://api.leem.it/v1/auth/login`

|name|type|in|required|
| :---: | :---: | :---: | :---: |
|email|`string`|body|True|
|password|`string`|body|True|

<details>
<summary>Response</summary>

<span class="get round"></span> **200: OK**

```json
{
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIn0.dozjgNryP4J3jVmNHl0w5N_XgL0n3I9PlFUP0THsR8U"
}
```
<span class="delete round"></span> **401: Unauthorized**

```json
{
    "error": "user is not authenticated"
}
```


</details>
