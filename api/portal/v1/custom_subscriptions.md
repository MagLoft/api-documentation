# Custom Subscriptions

API for managing Custom Subscription

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/custom_subscriptions/:app_id" %}

{% api-method-summary %}
List Custom Subscriptions
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a list of all `custom subscriptions` that belong to the magazine
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "order_id": "sub-12345",
  "source": "custom",
  "user_id": "FF063C1C-C5F3-4749-A7FC-7DCF91B3278F",
  "active": true,
  "start_date": "2018-01-24",
  "end_date": "2018-01-24",
  "created_at": "2018-01-24 10:55:35",
  "reader": {
    "id": 12345,
    "email": "user@magloft.com",
    "custom_data": {
      "gender": "male"
    },
    "confirmed": true
  },
  "status": "updated",
  "password": "pass1234"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/custom_subscriptions/:app_id/page/:page" %}

{% api-method-summary %}
List Custom Subscriptions Page
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a page list of all `custom subscriptions` that belong to the magazine
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="string" %}
The page number to list
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}


{% api-method-query-parameters %}

{% api-method-parameter name="per_page" type="string" %}
Number of items to show per page
{% endapi-method-parameter %}

{% api-method-parameter name="order_by" type="string" %}
Field to sort results by
{% endapi-method-parameter %}

{% api-method-parameter name="order_dir" type="string" %}
Direction (asc, desc) to sort results by
{% endapi-method-parameter %}

{% api-method-parameter name="filter" type="string" %}
Text filter to search results by
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
      "order_id": "sub-12345",
      "source": "custom",
      "user_id": "FF063C1C-C5F3-4749-A7FC-7DCF91B3278F",
      "active": true,
      "start_date": "2018-01-24",
      "end_date": "2018-01-24",
      "created_at": "2018-01-24 10:55:35",
      "reader": {
        "id": 12345,
        "email": "user@magloft.com",
        "custom_data": {
          "gender": "male"
        },
        "confirmed": true
      },
      "status": "updated",
      "password": "pass1234"
    }
  ]
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/custom_subscriptions/:app_id/(:email)(:id)" %}

{% api-method-summary %}
Get Custom Subscription
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a specific `custom subscription` by `id`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" %}
Email address of the reader account
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" %}
Subscription ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "order_id": "sub-12345",
  "source": "custom",
  "user_id": "FF063C1C-C5F3-4749-A7FC-7DCF91B3278F",
  "active": true,
  "start_date": "2018-01-24",
  "end_date": "2018-01-24",
  "created_at": "2018-01-24 10:55:35",
  "reader": {
    "id": 12345,
    "email": "user@magloft.com",
    "custom_data": {
      "gender": "male"
    },
    "confirmed": true
  },
  "status": "updated",
  "password": "pass1234"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="post" host="https://www.magloft.com" path="/api/portal/v1/custom_subscriptions/:app_id" %}

{% api-method-summary %}
Create Custom Subscription
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **creates** a new `custom subscription` and **returns** the saved `custom subscription`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="email" type="string" required=true %}
Email address of the reader account
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" %}
Plain-text password of Reader account shown only when creating a new subscription without specifying a password
{% endapi-method-parameter %}

{% api-method-parameter name="start_date" type="string" %}
Date from which the subscription should be valid (inclusive)
{% endapi-method-parameter %}

{% api-method-parameter name="end_date" type="string" %}
Date until which the subscription should be valid (inclusive)
{% endapi-method-parameter %}

{% api-method-parameter name="active" type="string" %}
Boolean indicating whether the subscription is currently active
{% endapi-method-parameter %}

{% api-method-parameter name="custom_data" type="string" %}
Hash containing custom data (string key, string value) of a reader
{% endapi-method-parameter %}

{% api-method-parameter name="firstname" type="string" %}
First name of the Custom Subscription's reader
{% endapi-method-parameter %}

{% api-method-parameter name="lastname" type="string" %}
Last name of the Custom Subscription's reader
{% endapi-method-parameter %}

{% api-method-parameter name="confirmation" type="string" %}
Boolean to indicate whether to send a confirmation email
{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "order_id": "sub-12345",
  "source": "custom",
  "user_id": "FF063C1C-C5F3-4749-A7FC-7DCF91B3278F",
  "active": true,
  "start_date": "2018-01-24",
  "end_date": "2018-01-24",
  "created_at": "2018-01-24 10:55:35",
  "reader": {
    "id": 12345,
    "email": "user@magloft.com",
    "custom_data": {
      "gender": "male"
    },
    "confirmed": true
  },
  "status": "updated",
  "password": "pass1234"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/custom_subscriptions/:app_id/:id" %}

{% api-method-summary %}
Update Custom Subscription
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **updates** a specific `custom subscription` by `id` and **returns** the updated `custom subscription`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=true %}
Subscription ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="start_date" type="string" %}
Date from which the subscription should be valid (inclusive)
{% endapi-method-parameter %}

{% api-method-parameter name="end_date" type="string" %}
Date until which the subscription should be valid (inclusive)
{% endapi-method-parameter %}

{% api-method-parameter name="active" type="string" %}
Boolean indicating whether the subscription is currently active
{% endapi-method-parameter %}

{% api-method-parameter name="custom_data" type="string" %}
Hash containing custom data (string key, string value) of a reader
{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "order_id": "sub-12345",
  "source": "custom",
  "user_id": "FF063C1C-C5F3-4749-A7FC-7DCF91B3278F",
  "active": true,
  "start_date": "2018-01-24",
  "end_date": "2018-01-24",
  "created_at": "2018-01-24 10:55:35",
  "reader": {
    "id": 12345,
    "email": "user@magloft.com",
    "custom_data": {
      "gender": "male"
    },
    "confirmed": true
  },
  "status": "updated",
  "password": "pass1234"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="delete" host="https://www.magloft.com" path="/api/portal/v1/custom_subscriptions/:app_id/:id" %}

{% api-method-summary %}
Delete Custom Subscription
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **deletes** a specific `custom subscription` by `id` and **returns** an `empty response` with status `204`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=true %}
Subscription ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
null
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/custom_subscriptions/:app_id/export.csv" %}

{% api-method-summary %}
Export Custom Subscriptions
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a csv document that contains a spreadsheet of all `custom subscriptions`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
null
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

