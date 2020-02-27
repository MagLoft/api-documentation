# RSS Import

API for managing rss import

{% api-method method="post" host="https://api.example.com/" path="/api/portal/v1/rss_imports/:app_id" %}

{% api-method-summary %}
Create an RSS Import
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **creates** a new `RSS Import` and **returns** the saved `RSS Import`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="url" type="String" required=true %}
External Blog URL to import articles from
{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "message_id": "123412341234",
  "url": "https://blog.magloft.com/feed/",
  "status": "pending",
  "created_at": "2018-01-24 10:55:35",
  "updated_at": "2018-01-24 10:55:35",
  "total": 14,
  "imported": 3
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://api.example.com/" path="/api/portal/v1/rss_imports/:app_id/:id" %}

{% api-method-summary %}
Get RSS Import
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a specific `rss import` by `id`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
RSS Import ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "message_id": "123412341234",
  "url": "https://blog.magloft.com/feed/",
  "status": "pending",
  "created_at": "2018-01-24 10:55:35",
  "updated_at": "2018-01-24 10:55:35",
  "total": 14,
  "imported": 3
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}


