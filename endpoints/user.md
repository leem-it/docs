



# **User**

The endpoint contains functions to change user settings

## <span class="get method">get</span> **Verify**

Sends a verification email if the user's email has not yet been verified

`https://api.leem.it/v1/user/verify`

<details>
<summary>Response</summary>

<span class="get round"></span> **200: OK**

```json
{
    "status": "ok or verified"
}
```
<span class="delete round"></span> **400: Bad Request**

```json
{
    "error": "unable to send email"
}
```
<span class="delete round"></span> **401: Unauthorized**

```json
{
    "error": "Google Oauth exception"
}
```


</details>

## <span class="post method">post</span> **Verify**

Verifies the email

`https://api.leem.it/v1/user/verify/[device]`

<details>
<summary>Response</summary>

<span class="get round"></span> **200: OK**

```json
"html page"
```
<span class="delete round"></span> **400: Bad Request**

```json
{
    "error": "invalid URL"
}
```
<span class="delete round"></span> **401: Unauthorized**

```json
{
    "error": "Unauthenticated"
}
```


</details>
