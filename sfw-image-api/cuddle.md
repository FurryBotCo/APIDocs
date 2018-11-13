---
description: Get a random cuddle image!
---

# Cuddle

{% api-method method="get" host="https://api.furrybot.me/sfw" path="/boop/:responseType/:imageType" %}
{% api-method-summary %}
Get Boops.
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get random fur images.
{% endapi-method-description %}

{% api-method-parameter name="responseType" type="string" required=false %}
This can be json or image, if not specified json is used.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="imageType" type="string" required=false %}
This can be 1 or more of: png,jpg,gif,webp. Separate by commas. \(no spaces\)
{% endapi-method-parameter %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
An image was found.
{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "response": {
        "image": "https://furrybot.furcdn.net/sfw/cuddle/0000C.jpg",
        "filetype": "jpeg",
        "name": "00574.jpg",
        "returntype": "json"
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
    "success": false,
    "error": {
        "code": 400
        "description": "{varies}"
    }
}```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "success": false,
    "error": {
        "code": 404,
        "description": "no images found with given type."
    }
}```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}
