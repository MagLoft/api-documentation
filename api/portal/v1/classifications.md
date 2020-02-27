# Classifications

API for managing Classifications

{% api-method method="get" host="https://api.example.com/" path="/api/portal/v1/classifications/:app_id" %}

{% api-method-summary %}
List Classifications
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a list of all `classifications` that belong to the publication
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Business",
  "color": "#444444",
  "position": 0
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://api.example.com/" path="/api/portal/v1/classifications/:app_id/:id" %}

{% api-method-summary %}
Get Classification
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a specific `classification` by `id`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Classification ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Business",
  "color": "#444444",
  "position": 0
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="post" host="https://api.example.com/" path="/api/portal/v1/classifications/:app_id/sort" %}

{% api-method-summary %}
Sort Classification
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **sorts** all `classification` by `position` and **returns** an `empty response` with status `204`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="positions" type="Array" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="positions[id]" type="Integer" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="positions[position]" type="Integer" required=true %}

{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=204 %}

```json
null
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="post" host="https://api.example.com/" path="/api/portal/v1/classifications/:app_id" %}

{% api-method-summary %}
Create Classification
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **creates** a new `classification` and **returns** the saved `classification`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="title" type="String" %}
Title of a classification
{% endapi-method-parameter %}

{% api-method-parameter name="color" type="String" %}
Hex color of a classification
{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Business",
  "color": "#444444",
  "position": 0
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="put" host="https://api.example.com/" path="/api/portal/v1/classifications/:app_id/:id" %}

{% api-method-summary %}
Update Classification
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **updates** a specific `classification` by `id` and **returns** the updated `classification`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Classification ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="title" type="String" %}
Title of a classification
{% endapi-method-parameter %}

{% api-method-parameter name="color" type="String" %}
Hex color of a classification
{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Business",
  "color": "#444444",
  "position": 0
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="delete" host="https://api.example.com/" path="/api/portal/v1/classifications/:app_id/:id" %}

{% api-method-summary %}
Delete Classification
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **deletes** a specific `classification` by `id` and **returns** an `empty response` with status `204`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Classification ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=204 %}

```json
null
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}


