# Issues

API for managing issues

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app\_id" %}
{% api-method-summary %}
List Issues
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a list of all `issues` that belong to the magazine
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="app\_id" type="String" required=true %}
App ID \(Publication\) to scope this request for.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="url\_scheme" type="string" required=false %}
URL scheme for the issue assets.  
The value can be one of the following:  
`path` **\(default\)**: `/path/to/asset`  
`shorthand`: `//cdn_host/path/to/asset`  
`https`: `https://cdn_host/path/to/asset`  
`http`: `http://cdn_host/path/to/asset`
{% endapi-method-parameter %}

{% api-method-parameter name="source" type="String" %}
Source type of issue
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "categories": null,
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app\_id" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="url\_scheme" type="string" required=false %}
\`https\`: https://host/path/to/asset
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app\_id" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="url\_scheme" type="string" required=false %}
//host/path/to/asset
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app\_id/page/:page" %}
{% api-method-summary %}
Retrieve paginated list of issues
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a page list of all `issues` that belong to the magazine
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="app\_id" type="String" required=true %}
App ID \(Publication\) to scope this request for.
{% endapi-method-parameter %}

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
      "title": "Welcome to MagLoft",
      "info": null,
      "hpub": null,
      "source_file": null,
      "source": "typeloft",
      "unlock_type": "free",
      "categories": null,
      "product_id": "purchase.issue_123456789",
      "product_id_apple": null,
      "product_id_google": null,
      "publication_id": null,
      "coupon_code": null,
      "dirty": false,
      "user_id": null,
      "custom_stylesheet": null,
      "custom_data": null,
      "price_tier": null,
      "cover": null
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app\_id/:id" %}
{% api-method-summary %}
Get Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a specific `issue` by `id`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="app\_id" type="String" required=true %}
App ID \(Publication\) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
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
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "categories": null,
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app\_id/:id/download" %}
{% api-method-summary %}
Download Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **redirects** to a specific `issue` HPUB url
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="app\_id" type="String" required=true %}
App ID \(Publication\) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
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

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app\_id/:id/source" %}
{% api-method-summary %}
Download a specific issue source
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **redirects** to a specific `issue` source file url
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="app\_id" type="String" required=true %}
App ID \(Publication\) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
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

{% api-method method="post" host="https://www.magloft.com" path="/api/portal/v1/issues/:app\_id" %}
{% api-method-summary %}
Create an Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **creates** a new `issue` and **returns** the saved `issue`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="app\_id" type="String" required=true %}
App ID \(Publication\) to scope this request for.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="user\_id" type="Integer" %}
Issue User ID
{% endapi-method-parameter %}

{% api-method-parameter name="title" type="String" %}
Issue Title
{% endapi-method-parameter %}

{% api-method-parameter name="info" type="String" %}
Issue information
{% endapi-method-parameter %}

{% api-method-parameter name="date" type="String" %}
Issue publish date
{% endapi-method-parameter %}

{% api-method-parameter name="product\_id" type="String" %}
Issue product id
{% endapi-method-parameter %}

{% api-method-parameter name="product\_id\_apple" type="String" %}
Issue product id \(Apple\)
{% endapi-method-parameter %}

{% api-method-parameter name="product\_id\_google" type="String" %}
Issue product id \(Google\)
{% endapi-method-parameter %}

{% api-method-parameter name="unlock\_type" type="String" %}
Unlock Type
{% endapi-method-parameter %}

{% api-method-parameter name="price\_tier" type="Integer" %}
Issue price tier
{% endapi-method-parameter %}

{% api-method-parameter name="design\_id" type="Integer" %}
Issue typeloft theme id
{% endapi-method-parameter %}

{% api-method-parameter name="cover" type="String" %}
Issue Cover
{% endapi-method-parameter %}

{% api-method-parameter name="hpub" type="String" %}
Issue HPUB Path
{% endapi-method-parameter %}

{% api-method-parameter name="source\_file" type="String" %}
Issue Source File
{% endapi-method-parameter %}

{% api-method-parameter name="source" type="String" %}
Source type of issue
{% endapi-method-parameter %}

{% api-method-parameter name="categories" type="Array" %}
Issue categories
{% endapi-method-parameter %}

{% api-method-parameter name="properties" type="Hash" %}
Issue properties
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="Symbol" %}

{% endapi-method-parameter %}

{% api-method-parameter name="create\_pages" type="boolean" %}

{% endapi-method-parameter %}

{% api-method-parameter name="publish" type="boolean" %}

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
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "categories": null,
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/issues/:app\_id/:id" %}
{% api-method-summary %}
Update an Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **updates** a specific `issue` by `id` and **returns** the updated `issue`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="app\_id" type="String" required=true %}
App ID \(Publication\) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="title" type="String" %}
Issue Title
{% endapi-method-parameter %}

{% api-method-parameter name="info" type="String" %}
Issue information
{% endapi-method-parameter %}

{% api-method-parameter name="date" type="String" %}
Issue publish date
{% endapi-method-parameter %}

{% api-method-parameter name="product\_id" type="String" %}
Issue product id
{% endapi-method-parameter %}

{% api-method-parameter name="product\_id\_apple" type="String" %}
Issue product id \(Apple\)
{% endapi-method-parameter %}

{% api-method-parameter name="product\_id\_google" type="String" %}
Issue product id \(Google\)
{% endapi-method-parameter %}

{% api-method-parameter name="unlock\_type" type="String" %}
Unlock Type
{% endapi-method-parameter %}

{% api-method-parameter name="price\_tier" type="Integer" %}
Issue price tier
{% endapi-method-parameter %}

{% api-method-parameter name="cover" type="String" %}
Issue Cover
{% endapi-method-parameter %}

{% api-method-parameter name="hpub" type="String" %}
Issue HPUB Path
{% endapi-method-parameter %}

{% api-method-parameter name="source\_file" type="String" %}
Issue Source File
{% endapi-method-parameter %}

{% api-method-parameter name="source" type="String" %}
Source type of issue
{% endapi-method-parameter %}

{% api-method-parameter name="categories" type="Array" %}
Issue categories
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="Symbol" %}

{% endapi-method-parameter %}

{% api-method-parameter name="custom\_data" type="Hash" %}
Custom Data Hash
{% endapi-method-parameter %}

{% api-method-parameter name="properties" type="Hash" %}
Issue properties
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
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "categories": null,
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://www.magloft.com" path="/api/portal/v1/issues/:app\_id/:id/clone/:magazine\_id" %}
{% api-method-summary %}
Clone an Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **creates** a new `issue` by cloning an existing `issue` and **returns** the saved `issue`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="app\_id" type="String" required=true %}
App ID \(Publication\) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
{% endapi-method-parameter %}

{% api-method-parameter name="magazine\_id" type="Integer" %}
Cloned Issue target magazine ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="user\_id" type="Integer" required=true %}
Issue User ID
{% endapi-method-parameter %}

{% api-method-parameter name="cloneTitle" type="String" required=true %}
Cloned Issue title
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
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "categories": null,
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/issues/:app\_id/:id/convert" %}
{% api-method-summary %}
Convert Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint converts an `issue` from PDF, EPUB or Folio
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="app\_id" type="String" required=true %}
App ID \(Publication\) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
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
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "categories": null,
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/issues/:app\_id/:id/pack" %}
{% api-method-summary %}
Pack an issue to HPUB
{% endapi-method-summary %}

{% api-method-description %}
This endpoint pack an `issue` to HPUB and **returns** the `issue`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="app\_id" type="String" required=true %}
App ID \(Publication\) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
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
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "categories": null,
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/issues/:app\_id/:id/process\_links" %}
{% api-method-summary %}
Process Filename
{% endapi-method-summary %}

{% api-method-description %}
This endpoint process an `issue` filename links in TypeLoft Pages and **returns** an `empty response` with status `204`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="app\_id" type="String" required=true %}
App ID \(Publication\) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
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

{% api-method method="delete" host="https://www.magloft.com" path="/api/portal/v1/issues/:app\_id/:id" %}
{% api-method-summary %}
Delete Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **deletes** a specific `issue` by `id` and **returns** an `empty response` with status `204`
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="app\_id" type="String" required=true %}
App ID \(Publication\) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
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

