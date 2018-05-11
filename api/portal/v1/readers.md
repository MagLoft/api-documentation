# Readers

API for managing app readers

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/readers/:app_id" %}

{% api-method-summary %}
List Readers
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a list of all `readers` that belong to the magazine
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
  "email": "john.doe@magloft.com",
  "name": "John Doe",
  "last_sign_in_at": "2018-01-24 10:55:35",
  "created_at": "2018-01-24 10:55:35",
  "devices": [
    "android",
    "apple"
  ],
  "confirmed": true,
  "authentication_token": "aabbccddeeff00112233445566778899",
  "custom_data": {
  }
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/readers/:app_id/page/:page" %}

{% api-method-summary %}
Retrieve paginated list of readers
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a page list of all `readers` that belong to the magazine
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="Integer" required=true %}
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

{% api-method-parameter name="filter" type="String" %}
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
      "email": "john.doe@magloft.com",
      "name": "John Doe",
      "last_sign_in_at": "2018-01-24 10:55:35",
      "created_at": "2018-01-24 10:55:35",
      "devices": [
        "android",
        "apple"
      ],
      "confirmed": true,
      "authentication_token": "aabbccddeeff00112233445566778899",
      "custom_data": {
      }
    }
  ]
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/readers/:app_id/(:email)(:id)" %}

{% api-method-summary %}
Get Reader
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a specific `reader` by `id`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="String" %}
Reader Email Address
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" %}
Reader ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "email": "john.doe@magloft.com",
  "name": "John Doe",
  "last_sign_in_at": "2018-01-24 10:55:35",
  "created_at": "2018-01-24 10:55:35",
  "devices": [
    "android",
    "apple"
  ],
  "confirmed": true,
  "authentication_token": "aabbccddeeff00112233445566778899",
  "custom_data": {
  }
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="post" host="https://www.magloft.com" path="/api/portal/v1/readers/:app_id" %}

{% api-method-summary %}
Create a Reader
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **creates** a new `reader` and **returns** the saved `reader`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="email" type="String" required=true %}
Reader Email Address
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="String" %}
Reader Password
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="String" %}
Reader Full Name (first name and last name)
{% endapi-method-parameter %}

{% api-method-parameter name="custom_data" type="Hash" %}
Custom key-value data stored for this reader
{% endapi-method-parameter %}

{% api-method-parameter name="confirmation" type="Virtus::Attribute::Boolean" %}
Send Confirmation Email
{% endapi-method-parameter %}

{% api-method-parameter name="confirmed" type="Virtus::Attribute::Boolean" %}
Whether this readers' Email was confirmed
{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "email": "john.doe@magloft.com",
  "name": "John Doe",
  "last_sign_in_at": "2018-01-24 10:55:35",
  "created_at": "2018-01-24 10:55:35",
  "devices": [
    "android",
    "apple"
  ],
  "confirmed": true,
  "authentication_token": "aabbccddeeff00112233445566778899",
  "custom_data": {
  }
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/readers/:app_id/:id" %}

{% api-method-summary %}
Update a Reader
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **updates** a specific `reader` by `id` and **returns** the updated `reader`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Reader ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="name" type="String" %}
Reader Full Name (first name and last name)
{% endapi-method-parameter %}

{% api-method-parameter name="custom_data" type="Hash" %}
Custom key-value data stored for this reader
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="String" %}
Reader Password
{% endapi-method-parameter %}

{% api-method-parameter name="confirmed" type="Virtus::Attribute::Boolean" %}
Whether this readers' Email was confirmed
{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "email": "john.doe@magloft.com",
  "name": "John Doe",
  "last_sign_in_at": "2018-01-24 10:55:35",
  "created_at": "2018-01-24 10:55:35",
  "devices": [
    "android",
    "apple"
  ],
  "confirmed": true,
  "authentication_token": "aabbccddeeff00112233445566778899",
  "custom_data": {
  }
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="delete" host="https://www.magloft.com" path="/api/portal/v1/readers/:app_id/:id" %}

{% api-method-summary %}
Delete Reader
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **deletes** a specific `reader` by `id` and **returns** an `empty response` with status `204`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Reader ID
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

{% api-method method="post" host="https://www.magloft.com" path="/api/portal/v1/readers/:app_id/:id/unlock" %}

{% api-method-summary %}
Create Issue Purchases
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **creates** one or many `issue purchases` by `product_id` and **returns** a list of `issue purchases`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Reader ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="product_ids" type="Array" required=true %}
Array containing Issue Product IDs to unlock
{% endapi-method-parameter %}

{% api-method-parameter name="order_id" type="String" %}
Subscription Order ID
{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/readers/:app_id/export.csv" %}

{% api-method-summary %}
Export readers
{% endapi-method-summary %}

{% api-method-description %}

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
null
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}


