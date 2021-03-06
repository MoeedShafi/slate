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

# Givvor Groups

## Get All Givvor Groups

```shell
curl "http://givvor-dev.herokuapp.com/api/groups/"
  -H "Authorization: donatedonatedonate"
```

```python
import requests 
  
URL = "http://givvor-dev.herokuapp.com/api/groups/"
 
PARAMS = {'Authorization':donatedonatedonate } 

r = requests.get(url = URL, params = PARAMS) 

data = r.json() 
  
```


> The above command returns JSON structured like this:

```json
{
    "result": [
        
        {
            "title": "GIVVOR GROUP TITLE",
            "get_entity_display_image": "https://www.givvor.com/static/group.png",
            "slug": "givvor-group-slug"
        },
        {
            "title":  "GIVVOR GROUP TITLE",
            "get_entity_display_image": "https://www.givvor.com/static/group.png",
            "slug": "givvor-group-slug"
        }
    ]
}
```

This endpoint retrieves all Givvor Groups.

### HTTP Request

`GET http://givvor-dev.herokuapp.com/api/groups/`

### Query Parameters


<aside class="success">
Remember — a happy Givvor Groups is an Verified Givvor Group!
</aside>


# Givvor Feed

## Get User Givvor Feed

```shell
curl "http://givvor-dev.herokuapp.com/feed/api/stream/"
  -H "Authorization: donatedonatedonate"
```

```python
import requests 
  
URL = "http://givvor-dev.herokuapp.com/feed/api/stream/"
 
PARAMS = {'Authorization':donatedonatedonate } 

r = requests.get(url = URL, params = PARAMS) 

data = r.json() 
  
```


> The above command returns JSON structured like this:

```json
[
    {
        "action_object_content_type": "givvor group",
        "feed_type": "donation",
        "liner": "/GROUP donated $12.0 to GIVVOR GROUP",
        "author": "/GROUP",
        "author_img_url": "https://www.givvor.com/static/group.png",
        "time_since": "1 day, 1 hour"
    },
    {
        "action_object_content_type": "givvor group",
        "feed_type": "donation",
        "liner": "@GIVVOR donated $14 to GIVVOR GROUP",
        "author": "@GIVVOR",
        "author_img_url":  "https://www.givvor.com/static/group.png",
        "time_since": "1 day, 1 hour"
    },
]
```

This endpoint retrieves all Givvor Groups.

### HTTP Request

`GET http://givvor-dev.herokuapp.com/feed/api/stream/`

### Query Parameters



# Givvor Donations

## Get User Givvor Donation

```shell
curl "http://givvor-dev.herokuapp.com/accounts/api/donations/"
  -H "Authorization: donatedonatedonate"
```

```python
import requests 
  
URL = "http://givvor-dev.herokuapp.com/accounts/api/donations/"
 
PARAMS = {'Authorization':donatedonatedonate } 

r = requests.get(url = URL, params = PARAMS) 

data = r.json() 
  
```


> The above command returns JSON structured like this:

```json
[
    {
        "group": "givvor group",
        "amount": "12",
        "description": "/GROUP donated $12.0 to GIVVOR GROUP",
        "user": "/GROUP",
        "user_img_url": "https://www.givvor.com/static/group.png",
        "date": "11/12/2019"
    },
    {
        "group": "givvor group",
        "amount": "14",
        "description": "@GIVVOR donated $14 to GIVVOR GROUP",
        "user": "@GIVVOR",
        "user_img_url":  "https://www.givvor.com/static/group.png",
        "date": "11/12/2019"
    },
]
```

This endpoint retrieves all Givvor Groups.

### HTTP Request

`GET http://givvor-dev.herokuapp.com/accounts/api/donations/`

### Query Parameters


## Donate

```shell

curl --data "api_key=api_key,......" 
"http://givvor-dev.herokuapp.com/tapi/donate/"

```

```python
import requests 
  
URL = "http://givvor-dev.herokuapp.com/tapi/donate/"

data = {'api_key':api_key, 
        .....................,
        .....................,
        .....................,
        } 

r = requests.post(url = URL, data = data) 

data = r.json() 
  
```


> The above command returns JSON structured like this:

```json
{
  'response': 'Donation Successful'
}
```

This endpoint Donates a specific amount to Givvor Group.

### HTTP Request

`POST http://givvor-dev.herokuapp.com/tapi/donate/`

### Query Parameters


Parameter | Description
--------- | -----------
amount | The amount a Givvor wants to donate
message (optional) | The message a Givvor wants to give with this donations
event_id (optional) | The ID of campign related to Group
cc_number | Credit Card
exp_month | Credit Card Expiry Month
exp_year | Credit Card Expiry Year
first_name | First name of the Givvor
last_name | Last name of the Givvor
address | Address of the Givvor
city | City of the Givvor
state | State of the Givvor
zip | Zip of the Givvor
fec_email | Email of the Givvor
phone | Phone of the Givvor

# Givvor Registry

##Registry
```shell
curl "http://givvor-registry.herokuapp.com/api/registry/"
  -H "Authorization: donatedonatedonate"
```

```python
import requests 
  
URL = "http://givvor-registry.herokuapp.com/api/registry"
 
PARAMS = {'Authorization':donatedonatedonate } 

r = requests.get(url = URL, params = PARAMS) 

data = r.json() 
  
```


> The above command returns JSON structured like this:

```json
[
    {
        "need": "Masks",
        "needed": "12",
        "description": "need masks for patients",
        "group": "Howard hospital college",
        "date": "03/12/2020"
    },
    {
        "need": "Lunches",
        "needed": "150",
        "description": "need Lunches for medical staff",
        "group": "Howard hospital college",
        "date": "04/12/2020-05/17/2020"
    },
]
```

This endpoint retrieves all  needs of Givvor Groups.

### HTTP Request

`GET http://givvor-registry.herokuapp.com/api/registry/`

##Create Need

```shell

curl --data "api_key=api_key,......" 
"http://givvor-registry.herokuapp.com/api/create_need/"

```

```python
import requests 
  
URL = "http://givvor-registry.herokuapp.com/api/create_need/"

data = {'api_key':api_key, 
        .....................,
        .....................,
        .....................,
        } 

r = requests.post(url = URL, data = data) 

data = r.json() 
  
```


> The above command returns JSON structured like this:

```json
{
  'response': 'Created Successfully'
}
```

This endpoint creates a need to a specific Givvor Group.

### HTTP Request

`POST http://givvor-registry.herokuapp.com/api/create_need/`

### Query Parameters


Parameter | Description
--------- | -----------
quantity | quantity required per day
title |  name of need
descrption | description of need
date1 | start date
date2 | end date
frequncy | Once OR Daily
group_id | Givvor Group ID

##Need Details
```shell
curl "http://givvor-registry.herokuapp.com/api/need/<ID>/"
  -H "Authorization: donatedonatedonate"
```

```python
import requests 
  
URL = "http://givvor-registry.herokuapp.com/api/need/<ID>/"
 
PARAMS = {'Authorization':donatedonatedonate } 

r = requests.get(url = URL, params = PARAMS) 

data = r.json() 
  
```


> The above command returns JSON structured like this:

```json
{
    "need": "Masks",
    "needed": "12",
    "description": "need masks for patients",
    "group": "Howard hospital college",
    "date": "03/12/2020"
}
```

This endpoint retrieves  a specific need of Givvor Groups.

### HTTP Request

`GET http://givvor-registry.herokuapp.com/api/need/<ID>/`

##fulfill Need

```shell

curl --data "api_key=api_key,......" 
"http://givvor-registry.herokuapp.com/api/need/<ID>/fulfill_need/"

```

```python
import requests 
  
URL = "http://givvor-registry.herokuapp.com/api/need/<ID>/fulfill_need/"

data = {'api_key':api_key, 
        .....................,
        .....................,
        .....................,
        } 

r = requests.post(url = URL, data = data) 

data = r.json() 
  
```


> The above command returns JSON structured like this:

```json
{
  'response': 'Created Successfully'
}
```

This endpoint creates a fulfilment to a specific Need.

### HTTP Request

`POST http://givvor-registry.herokuapp.com/api/need/<ID>/fulfill_need/`

### Query Parameters


Parameter | Description
--------- | -----------
quantity | quantity providing per day
amount |  cost of product
date | date of delivery
type | Donation OR Reimburse
