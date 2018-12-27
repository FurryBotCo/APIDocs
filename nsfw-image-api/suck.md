---
description: Get a random suck image!
---

# Suck

{% api-method method="get" host="https://api.furrybot.me/nsfw" path="/suck/:responseType/:imageType" %}
{% api-method-summary %}
Get a bulge.
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get random fur images.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="imageType" type="string" required=false %}
This can be one or more of: **png**,**jpg**,**gif**,**webp** separated by commas \(no spaces\)
{% endapi-method-parameter %}

{% api-method-parameter name="responseType" type="string" required=false %}
This can be json or image, if not specified json will be used.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="cdn" type="string" required=false %}
Which cdn should be used for this request? The possible values for this are hidden internally.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
An image was found
{% endapi-method-response-example-description %}

```javascript
{
    "success": true,
    "response": {
        "image": "https://furrybot.furcdn.net/nsfw/suck/1A2FO.jpg",
        "filetype": "jpeg",
        "name": "1A2FO.jpg",
        "returntype": "json"
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Something was wrong with the request.
{% endapi-method-response-example-description %}

```javascript
{
    "success": false,
    "error": {
        "code": 400
        "description": "{varies}"
    }]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
An image was not found.
{% endapi-method-response-example-description %}

```javascript
{
    "success": false,
    "error": {
        "code": 404,
        "description": "no images found with given type."
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}
