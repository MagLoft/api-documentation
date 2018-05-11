# Clients

API for managing Clients (Sub-User Accounts)

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/clients/" %}

{% api-method-summary %}
List Clients
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a list of `clients`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}





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
      "firstname": "Amelia",
      "lastname": "Earhart",
      "email": "user@magloft.com",
      "created_at": "2018-01-24 10:55:35",
      "updated_at": "2018-01-24 10:55:35",
      "last_seen_at": "2018-01-24 10:55:35",
      "sign_in_count": 6,
      "gravatar_url": "//secure.gravatar.com/avatar/123456789987654321",
      "roles": [
        {
          "id": 1234,
          "user_id": 1211,
          "publication_id": 123,
          "access_level": "author",
          "created_at": "2018-01-24 10:55:35",
          "updated_at": "2018-01-24 10:55:35"
        }
      ]
    }
  ]
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/clients/page/:page" %}

{% api-method-summary %}
Retrieve paginated list of clients
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a page list of all `clients`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="page" type="Integer" required=true %}
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

{% api-method-parameter name="publication_id" type="string" %}
Filter by publications ID
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
      "firstname": "Amelia",
      "lastname": "Earhart",
      "email": "user@magloft.com",
      "created_at": "2018-01-24 10:55:35",
      "updated_at": "2018-01-24 10:55:35",
      "last_seen_at": "2018-01-24 10:55:35",
      "sign_in_count": 6,
      "gravatar_url": "//secure.gravatar.com/avatar/123456789987654321",
      "roles": [
        {
          "id": 1234,
          "user_id": 1211,
          "publication_id": 123,
          "access_level": "author",
          "created_at": "2018-01-24 10:55:35",
          "updated_at": "2018-01-24 10:55:35"
        }
      ]
    }
  ]
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/clients/:id" %}

{% api-method-summary %}
GET Client
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a specific `client` by `id`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="id" type="Integer" required=true %}
Client ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "firstname": "Amelia",
  "lastname": "Earhart",
  "email": "user@magloft.com",
  "created_at": "2018-01-24 10:55:35",
  "updated_at": "2018-01-24 10:55:35",
  "last_seen_at": "2018-01-24 10:55:35",
  "sign_in_count": 6,
  "gravatar_url": "//secure.gravatar.com/avatar/123456789987654321",
  "roles": [
    {
      "id": 1234,
      "user_id": 1211,
      "publication_id": 123,
      "access_level": "author",
      "created_at": "2018-01-24 10:55:35",
      "updated_at": "2018-01-24 10:55:35"
    }
  ]
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="post" host="https://www.magloft.com" path="/api/portal/v1/clients/" %}

{% api-method-summary %}
Create new client
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **creates** a new `client` and **returns** the saved `client`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}




{% api-method-body-parameters %}

{% api-method-parameter name="email" type="string" required=true %}
Client email address
{% endapi-method-parameter %}

{% api-method-parameter name="firstname" type="string" required=true %}
Client Firstname
{% endapi-method-parameter %}

{% api-method-parameter name="lastname" type="string" %}
Client Lastname
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}
Client Password
{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "firstname": "Amelia",
  "lastname": "Earhart",
  "email": "user@magloft.com",
  "created_at": "2018-01-24 10:55:35",
  "updated_at": "2018-01-24 10:55:35",
  "last_seen_at": "2018-01-24 10:55:35",
  "sign_in_count": 6,
  "gravatar_url": "//secure.gravatar.com/avatar/123456789987654321",
  "roles": [
    {
      "id": 1234,
      "user_id": 1211,
      "publication_id": 123,
      "access_level": "author",
      "created_at": "2018-01-24 10:55:35",
      "updated_at": "2018-01-24 10:55:35"
    }
  ]
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/clients/:id" %}

{% api-method-summary %}
Update Client
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **updates** a specific `client` by `id` and **returns** the updated `client`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="id" type="Integer" required=true %}
Client ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="firstname" type="string" %}
Client Firstname
{% endapi-method-parameter %}

{% api-method-parameter name="lastname" type="string" %}
Client Lastname
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" %}
Client Password
{% endapi-method-parameter %}

{% api-method-parameter name="password_confirmation" type="string" %}
Client Password Confirmation
{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

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

{% api-method method="delete" host="https://www.magloft.com" path="/api/portal/v1/clients/:id" %}

{% api-method-summary %}
Delete Client
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **deletes** a specific `client` by `id` and **returns** an `empty response`  with status `204`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="id" type="Integer" required=true %}
Client ID
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


