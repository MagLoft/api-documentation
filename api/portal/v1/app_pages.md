# App Pages

API for managing In-App Pages

{% api-method method="get" host="https://api.example.com/" path="/api/portal/v1/app_pages/:app_id" %}

{% api-method-summary %}
List App Pages
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a list of all `app pages` that belong to the magazine
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
  "name": "Welcome Letter",
  "title": "Welcome to MagLoft",
  "icon": "trophy",
  "trigger": "on_launch",
  "action": "subscribe",
  "visibility": [
    "web",
    "ios",
    "android"
  ],
  "created_at": "2018-01-24 10:55:35",
  "updated_at": "2018-01-24 10:55:35",
  "published": true,
  "html": "<p>Hello World</p>"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://api.example.com/" path="/api/portal/v1/app_pages/:app_id/page/:page" %}

{% api-method-summary %}
Retrieve paginated list of readers
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a page list of `app pages` that belong to the magazine
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="Integer" %}
The page number to list
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}


{% api-method-query-parameters %}

{% api-method-parameter name="per_page" type="Integer" %}
Number of items to show per page
{% endapi-method-parameter %}

{% api-method-parameter name="order_by" type="Symbol" %}
Field to sort results by
{% endapi-method-parameter %}

{% api-method-parameter name="order_dir" type="Symbol" %}
Direction (asc, desc) to sort results by
{% endapi-method-parameter %}

{% api-method-parameter name="filter" type="JSON" %}

{% endapi-method-parameter %}

{% endapi-method-query-parameters %}



{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "total": 1,
  "page": 1,
  "records": [
    {
      "id": 1234,
      "name": "Welcome Letter",
      "title": "Welcome to MagLoft",
      "icon": "trophy",
      "trigger": "on_launch",
      "action": "subscribe",
      "visibility": [
        "web",
        "ios",
        "android"
      ],
      "created_at": "2018-01-24 10:55:35",
      "updated_at": "2018-01-24 10:55:35",
      "published": true,
      "html": "<p>Hello World</p>"
    }
  ]
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://api.example.com/" path="/api/portal/v1/app_pages/:app_id/:id" %}

{% api-method-summary %}
Get App Page
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a specific `app page` by `id`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
App Page ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "name": "Welcome Letter",
  "title": "Welcome to MagLoft",
  "icon": "trophy",
  "trigger": "on_launch",
  "action": "subscribe",
  "visibility": [
    "web",
    "ios",
    "android"
  ],
  "created_at": "2018-01-24 10:55:35",
  "updated_at": "2018-01-24 10:55:35",
  "published": true,
  "html": "<p>Hello World</p>"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="post" host="https://api.example.com/" path="/api/portal/v1/app_pages/:app_id" %}

{% api-method-summary %}
Create App Page
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **creates** a new `app page` and **returns** the saved `app page`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="name" type="String" required=true %}
Internal name of a page
{% endapi-method-parameter %}

{% api-method-parameter name="title" type="String" %}
Visible title of a page
{% endapi-method-parameter %}

{% api-method-parameter name="icon" type="String" %}
Optional icon to show in the modal window or side menu
{% endapi-method-parameter %}

{% api-method-parameter name="trigger" type="String" %}
Trigger Event to specify when the page should show up
{% endapi-method-parameter %}

{% api-method-parameter name="action" type="String" %}
Call to action to perform when accepting the offer
{% endapi-method-parameter %}

{% api-method-parameter name="html" type="String" %}
The html contents of a page
{% endapi-method-parameter %}

{% api-method-parameter name="visibility" type="Array" %}
An array specifying on which devices the page should be shown (web, ios, android)
{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "name": "Welcome Letter",
  "title": "Welcome to MagLoft",
  "icon": "trophy",
  "trigger": "on_launch",
  "action": "subscribe",
  "visibility": [
    "web",
    "ios",
    "android"
  ],
  "created_at": "2018-01-24 10:55:35",
  "updated_at": "2018-01-24 10:55:35",
  "published": true,
  "html": "<p>Hello World</p>"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="put" host="https://api.example.com/" path="/api/portal/v1/app_pages/:app_id/:id" %}

{% api-method-summary %}
Update App Page
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **updates** a specific `app page` by `id` and **returns** the updated `app page`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
App Page ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="name" type="String" %}
Internal name of a page
{% endapi-method-parameter %}

{% api-method-parameter name="title" type="String" %}
Visible title of a page
{% endapi-method-parameter %}

{% api-method-parameter name="icon" type="String" %}
Optional icon to show in the modal window or side menu
{% endapi-method-parameter %}

{% api-method-parameter name="trigger" type="String" %}
Trigger Event to specify when the page should show up
{% endapi-method-parameter %}

{% api-method-parameter name="action" type="String" %}
Call to action to perform when accepting the offer
{% endapi-method-parameter %}

{% api-method-parameter name="html" type="String" %}
The html contents of a page
{% endapi-method-parameter %}

{% api-method-parameter name="visibility" type="Array" %}
An array specifying on which devices the page should be shown (web, ios, android)
{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "name": "Welcome Letter",
  "title": "Welcome to MagLoft",
  "icon": "trophy",
  "trigger": "on_launch",
  "action": "subscribe",
  "visibility": [
    "web",
    "ios",
    "android"
  ],
  "created_at": "2018-01-24 10:55:35",
  "updated_at": "2018-01-24 10:55:35",
  "published": true,
  "html": "<p>Hello World</p>"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="delete" host="https://api.example.com/" path="/api/portal/v1/app_pages/:app_id/:id" %}

{% api-method-summary %}
Delete App Page
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **deletes** a specific `app page` by `id` and **returns** an `empty response`  with status `204`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
App Page ID
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


