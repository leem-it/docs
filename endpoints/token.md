



# **Token**

This endpoint allows to manage tokens

## <span class="get method">get</span> **Refresh**

Allows to refresh a token (this function is currently disabled)

`https://api.leem.it/v1/token/refresh`

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
"Unauthorized"
```


</details>

## <span class="get method">get</span> **Lifetime**

Allows to create lifetime tokens

`https://api.leem.it/v1/token/lifetime/[device]`

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
"Unauthorized"
```


</details>

## <span class="get method">get</span> **LogOut**

Logs out all the temporary tokens from a user. Please note that this method won't logout lifetime tokens.

`https://api.leem.it/v1/token/logout`

<details>
<summary>Response</summary>

<span class="get round"></span> **200: OK**

```json
{
    "status": "ok"
}
```
<span class="delete round"></span> **401: Unauthorized**

```json
"Unauthorized"
```


</details>

## <span class="get method">get</span> **LogOut a device**

Allows to invalidate lifetime tokens

`https://api.leem.it/v1/token/login/[device]`

<details>
<summary>Response</summary>

<span class="get round"></span> **200: OK**

```json
{
    "status": "ok"
}
```
<span class="delete round"></span> **401: Unauthorized**

```json
"Unauthorized"
```


</details>
