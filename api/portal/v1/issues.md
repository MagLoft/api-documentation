# Issues

API for managing issues

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id" %}

{% api-method-summary %}
List Issues
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a list of all `issues` that belong to the magazine
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}


{% api-method-query-parameters %}

{% api-method-parameter name="screen_type" type="String" %}
Screen Type
{% endapi-method-parameter %}

{% api-method-parameter name="source" type="String" %}
Source type of issue
{% endapi-method-parameter %}

{% api-method-parameter name="url_scheme" type="String" %}

{% endapi-method-parameter %}

{% api-method-parameter name="generator" type="String" %}
Generator
{% endapi-method-parameter %}

{% endapi-method-query-parameters %}



{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "hide_locked": false,
  "categories": [
    "Sports",
    "Business",
    "Politics"
  ],
  "category_ids": [
    1,
    2,
    3
  ],
  "classifications": [
    "Sports",
    "Business",
    "Politics"
  ],
  "classification_ids": [
    1,
    2,
    3
  ],
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "product_id_amazon": null,
  "screen_type": "issue",
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null,
  "generator": "pdfix"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/page/:page" %}

{% api-method-summary %}
Retrieve paginated list of issues
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a page list of all `issues` that belong to the magazine
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
      "title": "Welcome to MagLoft",
      "info": null,
      "hpub": null,
      "source_file": null,
      "source": "typeloft",
      "unlock_type": "free",
      "hide_locked": false,
      "categories": [
        "Sports",
        "Business",
        "Politics"
      ],
      "category_ids": [
        1,
        2,
        3
      ],
      "classifications": [
        "Sports",
        "Business",
        "Politics"
      ],
      "classification_ids": [
        1,
        2,
        3
      ],
      "product_id": "purchase.issue_123456789",
      "product_id_apple": null,
      "product_id_google": null,
      "product_id_amazon": null,
      "screen_type": "issue",
      "publication_id": null,
      "coupon_code": null,
      "dirty": false,
      "user_id": null,
      "custom_stylesheet": null,
      "custom_data": null,
      "price_tier": null,
      "cover": null,
      "generator": "pdfix"
    }
  ]
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id" %}

{% api-method-summary %}
Get Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a specific `issue` by `id`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "hide_locked": false,
  "categories": [
    "Sports",
    "Business",
    "Politics"
  ],
  "category_ids": [
    1,
    2,
    3
  ],
  "classifications": [
    "Sports",
    "Business",
    "Politics"
  ],
  "classification_ids": [
    1,
    2,
    3
  ],
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "product_id_amazon": null,
  "screen_type": "issue",
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null,
  "generator": "pdfix"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id/download" %}

{% api-method-summary %}
Download Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **redirects** to a specific `issue` HPUB url
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
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

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id/source" %}

{% api-method-summary %}
Download a specific issue source
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **redirects** to a specific `issue` source file url
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
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

{% api-method method="post" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id" %}

{% api-method-summary %}
Create an Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **creates** a new `issue` and **returns** the saved `issue`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="user_id" type="Integer" %}
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

{% api-method-parameter name="product_id" type="String" %}
Issue product id
{% endapi-method-parameter %}

{% api-method-parameter name="product_id_apple" type="String" %}
Issue product id (Apple)
{% endapi-method-parameter %}

{% api-method-parameter name="product_id_google" type="String" %}
Issue product id (Google)
{% endapi-method-parameter %}

{% api-method-parameter name="product_id_amazon" type="String" %}
Issue product id (Amazon)
{% endapi-method-parameter %}

{% api-method-parameter name="unlock_type" type="String" %}
Unlock Type
{% endapi-method-parameter %}

{% api-method-parameter name="hide_locked" type="Virtus::Attribute::Boolean" %}
Hide if Locked
{% endapi-method-parameter %}

{% api-method-parameter name="price_tier" type="Integer" %}
Issue price tier
{% endapi-method-parameter %}

{% api-method-parameter name="design_id" type="Integer" %}
Issue typeloft theme id
{% endapi-method-parameter %}

{% api-method-parameter name="cover" type="String" %}
Issue Cover
{% endapi-method-parameter %}

{% api-method-parameter name="hpub" type="String" %}
Issue HPUB Path
{% endapi-method-parameter %}

{% api-method-parameter name="source_file" type="String" %}
Issue Source File
{% endapi-method-parameter %}

{% api-method-parameter name="source" type="String" %}
Source type of issue
{% endapi-method-parameter %}

{% api-method-parameter name="category_ids" type="Array" %}
Issue category IDs
{% endapi-method-parameter %}

{% api-method-parameter name="classification_ids" type="Array" %}
Issue classification IDs
{% endapi-method-parameter %}

{% api-method-parameter name="properties" type="Hash" %}
Issue properties
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="Symbol" %}

{% endapi-method-parameter %}

{% api-method-parameter name="create_pages" type="Virtus::Attribute::Boolean" %}

{% endapi-method-parameter %}

{% api-method-parameter name="publish" type="Virtus::Attribute::Boolean" %}

{% endapi-method-parameter %}

{% api-method-parameter name="screen_type" type="String" %}

{% endapi-method-parameter %}

{% api-method-parameter name="file_size" type="Integer" %}

{% endapi-method-parameter %}

{% api-method-parameter name="generator" type="String" %}

{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "hide_locked": false,
  "categories": [
    "Sports",
    "Business",
    "Politics"
  ],
  "category_ids": [
    1,
    2,
    3
  ],
  "classifications": [
    "Sports",
    "Business",
    "Politics"
  ],
  "classification_ids": [
    1,
    2,
    3
  ],
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "product_id_amazon": null,
  "screen_type": "issue",
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null,
  "generator": "pdfix"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id" %}

{% api-method-summary %}
Update an Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **updates** a specific `issue` by `id` and **returns** the updated `issue`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
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

{% api-method-parameter name="product_id" type="String" %}
Issue product id
{% endapi-method-parameter %}

{% api-method-parameter name="product_id_apple" type="String" %}
Issue product id (Apple)
{% endapi-method-parameter %}

{% api-method-parameter name="product_id_google" type="String" %}
Issue product id (Google)
{% endapi-method-parameter %}

{% api-method-parameter name="product_id_amazon" type="String" %}
Issue product id (Amazon)
{% endapi-method-parameter %}

{% api-method-parameter name="unlock_type" type="String" %}
Unlock Type
{% endapi-method-parameter %}

{% api-method-parameter name="hide_locked" type="Virtus::Attribute::Boolean" %}
Hide if Locked
{% endapi-method-parameter %}

{% api-method-parameter name="price_tier" type="Integer" %}
Issue price tier
{% endapi-method-parameter %}

{% api-method-parameter name="cover" type="String" %}
Issue Cover
{% endapi-method-parameter %}

{% api-method-parameter name="hpub" type="String" %}
Issue HPUB Path
{% endapi-method-parameter %}

{% api-method-parameter name="source_file" type="String" %}
Issue Source File
{% endapi-method-parameter %}

{% api-method-parameter name="source" type="String" %}
Source type of issue
{% endapi-method-parameter %}

{% api-method-parameter name="category_ids" type="Array" %}
Issue category IDs
{% endapi-method-parameter %}

{% api-method-parameter name="classification_ids" type="Array" %}
Issue classification IDs
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="Symbol" %}

{% endapi-method-parameter %}

{% api-method-parameter name="jid_status" type="Symbol" %}

{% endapi-method-parameter %}

{% api-method-parameter name="custom_data" type="Hash" %}
Custom Data Hash
{% endapi-method-parameter %}

{% api-method-parameter name="custom_data[language]" type="String" %}

{% endapi-method-parameter %}

{% api-method-parameter name="custom_data[copy_of]" type="String" %}

{% endapi-method-parameter %}

{% api-method-parameter name="screenshots" type="[String]" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties" type="Hash" %}
Issue properties
{% endapi-method-parameter %}

{% api-method-parameter name="properties[page_turn_tap]" type="Virtus::Attribute::Boolean" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[vertical_bounce]" type="Virtus::Attribute::Boolean" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[max_zoom_level]" type="Float" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[dual_spread]" type="Virtus::Attribute::Boolean" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[dual_spread_cover]" type="Virtus::Attribute::Boolean" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[default_orientation]" type="String" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[orientation_phone]" type="String" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[orientation_tablet]" type="String" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[converted_to_typeloft]" type="Virtus::Attribute::Boolean" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[reverse_page_order]" type="Virtus::Attribute::Boolean" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[link_style]" type="String" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[allowed_devices]" type="[String]" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[allowed_platforms]" type="[String]" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[navigator]" type="Virtus::Attribute::Boolean" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[cover_colors]" type="[String]" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[features]" type="[String]" %}

{% endapi-method-parameter %}

{% api-method-parameter name="properties[web_url]" type="String" %}

{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "hide_locked": false,
  "categories": [
    "Sports",
    "Business",
    "Politics"
  ],
  "category_ids": [
    1,
    2,
    3
  ],
  "classifications": [
    "Sports",
    "Business",
    "Politics"
  ],
  "classification_ids": [
    1,
    2,
    3
  ],
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "product_id_amazon": null,
  "screen_type": "issue",
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null,
  "generator": "pdfix"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="post" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id/clone/:magazine_id" %}

{% api-method-summary %}
Clone an Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **creates** a new `issue` by cloning an existing `issue` and **returns** the saved `issue`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
{% endapi-method-parameter %}

{% api-method-parameter name="magazine_id" type="Integer" %}
Cloned Issue target magazine ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="user_id" type="Integer" required=true %}
Issue User ID
{% endapi-method-parameter %}

{% api-method-parameter name="cloneTitle" type="String" required=true %}
Cloned Issue title
{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "hide_locked": false,
  "categories": [
    "Sports",
    "Business",
    "Politics"
  ],
  "category_ids": [
    1,
    2,
    3
  ],
  "classifications": [
    "Sports",
    "Business",
    "Politics"
  ],
  "classification_ids": [
    1,
    2,
    3
  ],
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "product_id_amazon": null,
  "screen_type": "issue",
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null,
  "generator": "pdfix"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="post" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id/sort" %}

{% api-method-summary %}
Sort Issue Articles
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **sorts** a set of `articles` of an `issue` by `ids` and **returns** an `empty response` with status `204`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="article_ids" type="Array" required=true %}

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

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id/convert" %}

{% api-method-summary %}
Convert Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint converts an `issue` from PDF, EPUB or Folio
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "hide_locked": false,
  "categories": [
    "Sports",
    "Business",
    "Politics"
  ],
  "category_ids": [
    1,
    2,
    3
  ],
  "classifications": [
    "Sports",
    "Business",
    "Politics"
  ],
  "classification_ids": [
    1,
    2,
    3
  ],
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "product_id_amazon": null,
  "screen_type": "issue",
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null,
  "generator": "pdfix"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id/pack" %}

{% api-method-summary %}
Pack an issue to HPUB
{% endapi-method-summary %}

{% api-method-description %}
This endpoint pack an `issue` to HPUB and **returns** the `issue`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "hide_locked": false,
  "categories": [
    "Sports",
    "Business",
    "Politics"
  ],
  "category_ids": [
    1,
    2,
    3
  ],
  "classifications": [
    "Sports",
    "Business",
    "Politics"
  ],
  "classification_ids": [
    1,
    2,
    3
  ],
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "product_id_amazon": null,
  "screen_type": "issue",
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null,
  "generator": "pdfix"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id/export_pdf" %}

{% api-method-summary %}
Export issue to PDF
{% endapi-method-summary %}

{% api-method-description %}
This endpoint converts a TypeLoft 2 `issue` to PDF and **returns** the `issue`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "hide_locked": false,
  "categories": [
    "Sports",
    "Business",
    "Politics"
  ],
  "category_ids": [
    1,
    2,
    3
  ],
  "classifications": [
    "Sports",
    "Business",
    "Politics"
  ],
  "classification_ids": [
    1,
    2,
    3
  ],
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "product_id_amazon": null,
  "screen_type": "issue",
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null,
  "generator": "pdfix"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id/generate_web_url" %}

{% api-method-summary %}
Generate Web URL
{% endapi-method-summary %}

{% api-method-description %}
This endpoint generates a hosted version of an `issue`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "title": "Welcome to MagLoft",
  "info": null,
  "hpub": null,
  "source_file": null,
  "source": "typeloft",
  "unlock_type": "free",
  "hide_locked": false,
  "categories": [
    "Sports",
    "Business",
    "Politics"
  ],
  "category_ids": [
    1,
    2,
    3
  ],
  "classifications": [
    "Sports",
    "Business",
    "Politics"
  ],
  "classification_ids": [
    1,
    2,
    3
  ],
  "product_id": "purchase.issue_123456789",
  "product_id_apple": null,
  "product_id_google": null,
  "product_id_amazon": null,
  "screen_type": "issue",
  "publication_id": null,
  "coupon_code": null,
  "dirty": false,
  "user_id": null,
  "custom_stylesheet": null,
  "custom_data": null,
  "price_tier": null,
  "cover": null,
  "generator": "pdfix"
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id/process_links" %}

{% api-method-summary %}
Process Filename
{% endapi-method-summary %}

{% api-method-description %}
This endpoint process an `issue` filename links in TypeLoft Pages and **returns** an `empty response`  with status `204`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
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

{% api-method method="delete" host="https://www.magloft.com" path="/api/portal/v1/issues/:app_id/:id" %}

{% api-method-summary %}
Delete Issue
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **deletes** a specific `issue` by `id` and **returns** an `empty response`  with status `204`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Issue ID
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


