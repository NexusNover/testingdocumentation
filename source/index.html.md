---
title: API Reference

language_tabs:
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='https://tokens.logic.rest'>Generate a Token</a>

includes:
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: This documentation website contains information on how to interact with logic.rest API Endpoints
---

# Introduction

Welcome to the documentation website for Logic.rest, a powerful API designed to help you create scalable and efficient RESTful web services. This website serves as a comprehensive guide to using the Logic.rest API, providing everything you need to get started and build complex web applications.

# Discord

## GET Application Information

```ruby
require 'uri'
require 'net/http'

id = 'DISCORD_APPLICATION_ID'
url = URI("https://logic.rest/api/v1/discord/application/#{id}")

http = Net::HTTP.new(url.host, url.port)
http.use_ssl = true

request = Net::HTTP::Get.new(url)
response = http.request(request)

puts response.read_body
```

```python
import requests

id = "DISCORD_APPLICATION_ID"
url = f"https://logic.rest/api/v1/discord/application/{id}"

response = requests.get(url)

print(response.text)
```

```shell
curl "https://logic.rest/api/v1/discord/application/DISCORD_APPLICATION_ID"
```

```javascript
const fetch = (...args) => import('node-fetch').then(({default: fetch}) => fetch(...args));

const id = "DISCORD_APPLICATION_ID";
const url = `https://logic.rest/api/v1/discord/application/${id}`;

fetch(url)
  .then(response => response.text())
  .then(data => console.log(data))
  .catch(error => console.error(error));
```

> This endpoint will respond with the following response

```json
{
   "status":200,
   "data":{
      "id":"282859044593598464",
      "name":"ProBot ✨",
      "description":"Make a Professional Server! Welcome images, voice/text levels, reaction roles, logs,  moderation, and many many more!",
      "icon_code":"156a0d2872579f1ffcaa5d2127239bfd",
      "type":null,
      "hook":true,
      "terms_of_service_url":"https://probot.io/terms-of-use",
      "privacy_policy_url":"https://probot.io/privacy-policy",
      "tags":[
         "Leveling",
         "Moderation",
         "Reaction Roles",
         "Soical",
         "Welcome"
      ],
      "verify_key":"72afa4f075f512b48b3916961f5fb9e357ba68f943ce8f9facaca3390987a383",
      "flags":10797056,
      "bot":{
         "id":"282859044593598464",
         "username":"ProBot ✨",
         "discriminator":"5803",
         "avatar_code":"156a0d2872579f1ffcaa5d2127239bfd",
         "is_public?":true,
         "requires_code_grant?":false,
         "support_guild_id":"224308865427046402",
         "approximate_guild_count":8580000
      }
   }
}
```

This endpoint fetches information about a Discord Application

### HTTP Request

`GET https://logic.rest/api/v1/discord/application/:id`

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
id | true | The ID of a Discord Application

## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2" \
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.get(2);
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

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Delete a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.delete(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.delete(2)
```

```shell
curl "http://example.com/api/kittens/2" \
  -X DELETE \
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete

