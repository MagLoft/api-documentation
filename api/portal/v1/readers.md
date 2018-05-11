# Readers

API for managing app readers

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/readers/:app_id" %}

{% api-method-summary %}
GET readers list
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID
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

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/readers/:app_id/page/:page" %}

{% api-method-summary %}
GET paginated readers list
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="string" %}

{% endapi-method-parameter %}

{% endapi-method-path-parameters %}


{% api-method-query-parameters %}

{% api-method-parameter name="per_page" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="order_by" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="order_dir" type="string" %}

{% endapi-method-parameter %}

{% api-method-parameter name="filter" type="string" %}

{% endapi-method-parameter %}

{% endapi-method-query-parameters %}



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

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/readers/:app_id/(:email)(:id)" %}

{% api-method-summary %}
GET a specific reader
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" %}
Reader Email
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" %}
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

{% api-method method="post" host="https://www.magloft.com" path="/api/portal/v1/readers/:app_id" %}

{% api-method-summary %}
Create reader
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="email" type="string" required=true %}
Reader Email
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" %}
Reader Password
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" %}
Reader Name
{% endapi-method-parameter %}

{% api-method-parameter name="custom_data" type="string" %}
Reader Custom Data
{% endapi-method-parameter %}

{% api-method-parameter name="confirmation" type="string" %}
Send Confirmation Email
{% endapi-method-parameter %}

{% api-method-parameter name="confirmed" type="string" %}
Set Reader to Confirmed
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

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/readers/:app_id/:id" %}

{% api-method-summary %}
Update reader
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=true %}
Reader ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="name" type="string" %}
Reader Name
{% endapi-method-parameter %}

{% api-method-parameter name="custom_data" type="string" %}
Reader Custom Data
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" %}
Reader Password
{% endapi-method-parameter %}

{% api-method-parameter name="confirmed" type="string" %}
Reader Email Confirmed
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

{% api-method method="delete" host="https://www.magloft.com" path="/api/portal/v1/readers/:app_id/:id" %}

{% api-method-summary %}
Delete reader
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=true %}
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
Unlock Product IDs
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="string" required=true %}
Reader ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="product_ids" type="string" required=true %}
Issue Product IDs
{% endapi-method-parameter %}

{% api-method-parameter name="order_id" type="string" %}

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

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/readers/:app_id/export.csv" %}

{% api-method-summary %}
Export readers
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="string" required=true %}
App ID
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


