---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby
  - python
  - javascript

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

```ruby
require 'Givvor'

api = Givvor::APIClient.authorize!('donatedonatedonate')
```

```python
import Givvor

api = Givvor.authorize('donatedonatedonate')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: donatedonatedonate"
```

```javascript
const Givvor = require('Givvor');

let api = Givvor.authorize('donatedonatedonate');
```

> Make sure to replace `donatedonatedonate` with your API key.

Givvor uses API keys to allow access to the API. You can register a new Givvor API key at our [developer portal](http://example.com/developers).

Givvor expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: donatedonatedonate`

<aside class="notice">
You must replace <code>donatedonatedonate</code> with your personal API key.
</aside>

# Givvor

## Get All Givvor

```ruby
require 'Givvor'

api = Givvor::APIClient.authorize!('donatedonatedonate')
api.Givvor.get
```

```python
import Givvor

api = Givvor.authorize('donatedonatedonate')
api.Givvor.get()
```

```shell
curl "http://example.com/api/Givvor"
  -H "Authorization: donatedonatedonate"
```

```javascript
const Givvor = require('Givvor');

let api = Givvor.authorize('donatedonatedonate');
let Givvor = api.Givvor.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all Givvor.

### HTTP Request

`GET http://example.com/api/Givvor`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include Givvor that have already been adopted.

<aside class="success">
Remember — a happy Givvor is an authenticated Givvor!
</aside>

## Get a Specific Givvor

```ruby
require 'Givvor'

api = Givvor::APIClient.authorize!('donatedonatedonate')
api.Givvor.get(2)
```

```python
import Givvor

api = Givvor.authorize('donatedonatedonate')
api.Givvor.get(2)
```

```shell
curl "http://example.com/api/Givvor/2"
  -H "Authorization: donatedonatedonate"
```

```javascript
const Givvor = require('Givvor');

let api = Givvor.authorize('donatedonatedonate');
let max = api.Givvor.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific Givvor.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/Givvor/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Givvor to retrieve

## Delete a Specific Givvor

```ruby
require 'Givvor'

api = Givvor::APIClient.authorize!('donatedonatedonate')
api.Givvor.delete(2)
```

```python
import Givvor

api = Givvor.authorize('donatedonatedonate')
api.Givvor.delete(2)
```

```shell
curl "http://example.com/api/Givvor/2"
  -X DELETE
  -H "Authorization: donatedonatedonate"
```

```javascript
const Givvor = require('Givvor');

let api = Givvor.authorize('donatedonatedonate');
let max = api.Givvor.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific Givvor.

### HTTP Request

`DELETE http://example.com/Givvor/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Givvor to delete

