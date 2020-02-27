---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - python

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Givvor is free, safe and secure. No ads, third-party access to data or spam. All you need to support you philanthropic efforts in one place.

Join others making a difference

Safely support your favorite nonprofits
- One place to contribute to all the causes you care about
- Be in the drivers seat for change

Discover additional worthy causes
- Live stream of who is giving to which nonprofits
- Insights into other nonprofits based on like-minded Givvors

Build communities of supporters
- Connect with other Givvors
- Each nonprofit has its own dedicated community
Don’t just be a donor, be a GIVVOR!


# Authentication

> To authorize, use this code:


```shell
# With shell, you can just pass the correct header with each request
curl "http://givvor-dev.herokuapp.com/api/user/login"
  -H "username: donatedonatedonate password:donatedonatedonate"
```

```python
import requests 
  
URL = "http://givvor-dev.herokuapp.com/api/user/login"
 
PARAMS = {'username':donatedonatedonate , 'password':donatedonatedonate } 

r = requests.get(url = URL, params = PARAMS) 

data = r.json() 

```

> Make sure to replace `donatedonatedonate` with your username and password.
> The above command returns JSON structured like this:

```json
{
  "token": "donatedonatedonate",
}
```

Givvor uses API keys to allow access to the API. You can register a new Givvor API key at our [developer portal](http://givvor-dev.herokuapp.com/login).

Givvor expects for the API key to be included in all API requests to the server in a header that looks like the following:

`username: donatedonatedonate`
`password: donatedonatedonate`

<aside class="notice">
You must replace <code>donatedonatedonate</code> with your personal username and password.
</aside>

# Givvor

## Get All Givvor

```shell
curl "http://givvor-dev.herokuapp.com/api/users/"
  -H "Authorization: donatedonatedonate"
```

```python
import requests 
  
URL = "http://givvor-dev.herokuapp.com/api/users/"
 
PARAMS = {'Authorization':donatedonatedonate } 

r = requests.get(url = URL, params = PARAMS) 

data = r.json() 
  
```


> The above command returns JSON structured like this:

```json
{
    "count": "{int}",
    "next": "http://givvor-dev.herokuapp.com/api/users/?limit={int}&offset={int}",
    "previous": null,
    "results": [
        {
            "username": "givvor",
            "first_name": "givvor",
            "last_name": "givvor",
            "profile": {
                "bg_img": "https://www.givvor.com/static/at_user-icon.png",
                "profile_img": "https://www.givvor.com/static/at_user-icon.png",
            }
        },
        {
            "username": "givvor",
            "first_name": "givvor",
            "last_name": "givvor",
            "profile": {
                "bg_img": "https://www.givvor.com/static/at_user-icon.png",
                "profile_img": "https://www.givvor.com/static/at_user-icon.png",
            }
        }
    ]
}
```

This endpoint retrieves all Givvor.

### HTTP Request

`GET http://givvor-dev.herokuapp.com/api/users/`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
limit | 10 | To change the limit of result returned.
offset | 10 | To change the starting point of result returned.

<aside class="success">
Remember — a happy Givvor is an authenticated Givvor!
</aside>

## Get a Specific Givvor

```shell
curl "http://givvor-dev.herokuapp.com/api/users/2/"
  -H "Authorization: donatedonatedonate"
```

```python

import requests 
  
URL = "http://givvor-dev.herokuapp.com/api/users/2/"
 
PARAMS = {'Authorization':donatedonatedonate } 

r = requests.get(url = URL, params = PARAMS) 

data = r.json() 

```


> The above command returns JSON structured like this:

```json
{
  "username": "givvor",
  "first_name": "givvor",
  "last_name": "givvor",
  "profile": {
      "bg_img": "https://www.givvor.com/static/at_user-icon.png",
      "profile_img": "https://www.givvor.com/static/at_user-icon.png",
  }
}
```

This endpoint retrieves a specific Givvor.

### HTTP Request

`GET http://givvor-dev.herokuapp.com/api/users/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Givvor to retrieve


<aside class="warning">Do not expose your API token with any other person.</aside>


## Delete a Specific Givvor



```shell
curl "http://example.com/api/Givvor/2"
  -X DELETE
  -H "Authorization: donatedonatedonate"
```

```python
import requests 
  
URL = "http://givvor-dev.herokuapp.com/api/users/2/delete/"
 
PARAMS = {'Authorization':donatedonatedonate } 

r = requests.get(url = URL, params = PARAMS) 

data = r.json() 
```


> The above command returns JSON structured like this:

```json
{
  "msg" : "user succesfully deleted :("
}
```

This endpoint deletes a specific Givvor.

### HTTP Request

`DELETE http://givvor-dev.herokuapp.com/api/users/<ID>/delete/`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Givvor to delete

