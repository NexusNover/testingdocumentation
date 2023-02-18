---
title: API Reference

language_tabs:
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='https://tokens.blaze.rest'>Generate a Token</a>

includes:
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: This documentation website contains information on how to interact with blaze.rest API Endpoints
---

# Introduction

Welcome to the documentation website for blaze.rest, a powerful API designed to help you create scalable and efficient RESTful web services. This website serves as a comprehensive guide to using the blaze.rest API, providing everything you need to get started and build complex web applications.

# blaze.rest

## Random Joke

```ruby
require 'uri'
require 'net/http'

url = URI("https://blaze.rest/api/v1/blaze/joke")

http = Net::HTTP.new(url.host, url.port)
http.use_ssl = true

request = Net::HTTP::Get.new(url)
response = http.request(request)

puts response.read_body
```

```python
import requests
url = f"https://blaze.rest/api/v1/blaze/joke"

response = requests.get(url)

print(response.text)
```

```shell
curl "https://blaze.rest/api/v1/blaze/joke"
```

```javascript
const fetch = (...args) => import('node-fetch').then(({default: fetch}) => fetch(...args));

const url = `https://blaze.rest/api/v1/blaze/joke`;

fetch(url)
  .then(response => response.text())
  .then(data => console.log(data))
  .catch(error => console.error(error));
```

> This endpoint will respond with the following JSON response

```json
{
   "status":200,
   "data":{
      "joke":"A boat builder is showing his son one of his forests. He turns to him and says, \"Son, one day this will all be oars\""
   }
}
```

This endpoint generates a random joke

### HTTP Request

`GET https://blaze.rest/api/v1/blaze/joke`

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
token | true | Your blaze.rest API Token


# Discord

## Application Information

```ruby
require 'uri'
require 'net/http'

id = 'DISCORD_APPLICATION_ID'
url = URI("https://blaze.rest/api/v1/discord/application/#{id}")

http = Net::HTTP.new(url.host, url.port)
http.use_ssl = true

request = Net::HTTP::Get.new(url)
response = http.request(request)

puts response.read_body
```

```python
import requests

id = "DISCORD_APPLICATION_ID"
url = f"https://blaze.rest/api/v1/discord/application/{id}"

response = requests.get(url)

print(response.text)
```

```shell
curl "https://blaze.rest/api/v1/discord/application/DISCORD_APPLICATION_ID"
```

```javascript
const fetch = (...args) => import('node-fetch').then(({default: fetch}) => fetch(...args));

const id = "DISCORD_APPLICATION_ID";
const url = `https://blaze.rest/api/v1/discord/application/${id}`;

fetch(url)
  .then(response => response.text())
  .then(data => console.log(data))
  .catch(error => console.error(error));
```

> This endpoint will respond with the following JSON response

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

`GET https://blaze.rest/api/v1/discord/application/:id`

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
id | true | The ID of a Discord Application

## User Information

```ruby
require 'uri'
require 'net/http'

id = 'DISCORD_USER_ID'
url = URI("https://blaze.rest/api/v1/discord/user/#{id}")

http = Net::HTTP.new(url.host, url.port)
http.use_ssl = true

request = Net::HTTP::Get.new(url)
response = http.request(request)

puts response.read_body
```

```python
import requests

id = "DISCORD_USER_ID"
url = f"https://blaze.rest/api/v1/discord/user/{id}"

response = requests.get(url)

print(response.text)
```

```shell
curl "https://blaze.rest/api/v1/discord/user/DISCORD_USER_ID"
```

```javascript
const fetch = (...args) => import('node-fetch').then(({default: fetch}) => fetch(...args));

const id = "DISCORD_USER_ID";
const url = `https://blaze.rest/api/v1/discord/user/${id}`;

fetch(url)
  .then(response => response.text())
  .then(data => console.log(data))
  .catch(error => console.error(error));
```

> This endpoint will respond with the following JSON response

```json
{
   "status":200,
   "data":{
      "id":"1065368179494359071",
      "username":"blaze.rest",
      "discriminator":"9232",
      "avatar_code":"b012035185190963be7a49a51e732ddb",
      "banner_code":null,
      "avatar_decoration":null,
      "public_flags":0,
      "banner_color":null,
      "accent_color":null
   }
}
```

This endpoint fetches information about a Discord User

### HTTP Request

`GET https://blaze.rest/api/v1/discord/user/:id`

### Query Parameters

Parameter | Required | Description
--------- | ------- | -----------
id | true | The ID of a Discord User
