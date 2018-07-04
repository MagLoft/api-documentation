# Clients

API for managing Clients \(Sub-User Accounts\)

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/clients/" %}
{% api-method-summary %}
List Clients
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a list of `clients`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
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
{% api-method-parameter name="per\_page" type="Integer" %}
Number of items to show per page
{% endapi-method-parameter %}

{% api-method-parameter name="order\_by" type="Symbol" %}
Field to sort results by
{% endapi-method-parameter %}

{% api-method-parameter name="order\_dir" type="Symbol" %}
Direction \(asc, desc\) to sort results by
{% endapi-method-parameter %}

{% api-method-parameter name="filter" type="String" %}
Text filter to search results by
{% endapi-method-parameter %}

{% api-method-parameter name="publication\_id" type="Integer" %}
Filter by publications ID
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
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
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
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
{% api-method-parameter name="email" type="String" required=true %}
Client email address
{% endapi-method-parameter %}

{% api-method-parameter name="firstname" type="String" required=true %}
Client Firstname
{% endapi-method-parameter %}

{% api-method-parameter name="lastname" type="String" %}
Client Lastname
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="String" required=true %}
Client Password
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
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
{% api-method-parameter name="firstname" type="String" %}
Client Firstname
{% endapi-method-parameter %}

{% api-method-parameter name="lastname" type="String" %}
Client Lastname
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="String" %}
Client Password
{% endapi-method-parameter %}

{% api-method-parameter name="password\_confirmation" type="String" %}
Client Password Confirmation
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
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
This endpoint **deletes** a specific `client` by `id` and **returns** an `empty response` with status `204`
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
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
null
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

