# Articles

API for managing articles

{% api-method method="get" host="https://api.example.com/" path="/api/portal/v1/articles/:app_id" %}

{% api-method-summary %}
List Articles
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a list of all `articles` that belong to the magazine
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}


{% api-method-query-parameters %}

{% api-method-parameter name="order_by" type="Symbol" %}
Field to sort results by
{% endapi-method-parameter %}

{% api-method-parameter name="order_dir" type="Symbol" %}
Direction (asc, desc) to sort results by
{% endapi-method-parameter %}

{% api-method-parameter name="issue_id" type="Integer" %}

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
  "html": null,
  "assets": null,
  "cover": null,
  "date": null,
  "unlock_type": "free",
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
  "publication_id": null,
  "issue_id": null,
  "position": null,
  "visible": true,
  "rss_feed_id": null,
  "source": null
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://api.example.com/" path="/api/portal/v1/articles/:app_id/page/:page" %}

{% api-method-summary %}
Retrieve paginated list of articles
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a page list of all `articles` that belong to the magazine
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

{% api-method method="get" host="https://api.example.com/" path="/api/portal/v1/articles/:app_id/:id" %}

{% api-method-summary %}
Get Article
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a specific `article` by `id`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Article ID
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
  "html": null,
  "assets": null,
  "cover": null,
  "date": null,
  "unlock_type": "free",
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
  "publication_id": null,
  "issue_id": null,
  "position": null,
  "visible": true,
  "rss_feed_id": null,
  "source": null
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="post" host="https://api.example.com/" path="/api/portal/v1/articles/:app_id" %}

{% api-method-summary %}
Create an Article
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **creates** a new `article` and **returns** the saved `article`
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
Article Title
{% endapi-method-parameter %}

{% api-method-parameter name="info" type="String" %}
Article Description
{% endapi-method-parameter %}

{% api-method-parameter name="html" type="String" %}
Article HTML
{% endapi-method-parameter %}

{% api-method-parameter name="date" type="String" %}
Article Publish Date
{% endapi-method-parameter %}

{% api-method-parameter name="cover" type="String" %}
Article Cover
{% endapi-method-parameter %}

{% api-method-parameter name="category_ids" type="Array" %}
Article category IDs
{% endapi-method-parameter %}

{% api-method-parameter name="issue_id" type="Integer" %}
Issue ID
{% endapi-method-parameter %}

{% api-method-parameter name="unlock_type" type="String" %}
Unlock Type
{% endapi-method-parameter %}

{% api-method-parameter name="position" type="Integer" %}
Order Position of the Article within an Issue
{% endapi-method-parameter %}

{% api-method-parameter name="source" type="String" %}
Article type
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
  "html": null,
  "assets": null,
  "cover": null,
  "date": null,
  "unlock_type": "free",
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
  "publication_id": null,
  "issue_id": null,
  "position": null,
  "visible": true,
  "rss_feed_id": null,
  "source": null
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="put" host="https://api.example.com/" path="/api/portal/v1/articles/:app_id/:id" %}

{% api-method-summary %}
Update an Article
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **updates** a specific `article` by `id` and **returns** the updated `article`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" %}
Article ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="title" type="String" %}
Article Title
{% endapi-method-parameter %}

{% api-method-parameter name="info" type="String" %}
Article Description
{% endapi-method-parameter %}

{% api-method-parameter name="html" type="String" %}
Article HTML
{% endapi-method-parameter %}

{% api-method-parameter name="assets" type="Hash" %}
Article Assets
{% endapi-method-parameter %}

{% api-method-parameter name="date" type="String" %}
Article publish date
{% endapi-method-parameter %}

{% api-method-parameter name="cover" type="String" %}
Article Cover
{% endapi-method-parameter %}

{% api-method-parameter name="category_ids" type="Array" %}
Article category IDs
{% endapi-method-parameter %}

{% api-method-parameter name="issue_id" type="Integer" %}
Issue ID
{% endapi-method-parameter %}

{% api-method-parameter name="unlock_type" type="String" %}
Unlock Type
{% endapi-method-parameter %}

{% api-method-parameter name="position" type="Integer" %}
Order Position of the Article within an Issue
{% endapi-method-parameter %}

{% api-method-parameter name="visible" type="Virtus::Attribute::Boolean" %}
A boolean indicating whether this article is visible
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
  "html": null,
  "assets": null,
  "cover": null,
  "date": null,
  "unlock_type": "free",
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
  "publication_id": null,
  "issue_id": null,
  "position": null,
  "visible": true,
  "rss_feed_id": null,
  "source": null
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="delete" host="https://api.example.com/" path="/api/portal/v1/articles/:app_id/:id" %}

{% api-method-summary %}
Delete Article
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **deletes** a specific `article` by `id` and **returns** an `empty response`  with status `204`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
Article ID
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

{% api-method method="post" host="https://api.example.com/" path="/api/portal/v1/articles/:app_id/flexpdf-import" %}

{% api-method-summary %}
FlexPDF Import
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **creates** multiple `article` and **returns** 
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="articles" type="Array" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="articles[title]" type="String" required=true %}
Article Title
{% endapi-method-parameter %}

{% api-method-parameter name="articles[html]" type="String" required=true %}
Article HTML
{% endapi-method-parameter %}

{% api-method-parameter name="articles[cover]" type="String" required=true %}
Article Cover
{% endapi-method-parameter %}

{% api-method-parameter name="articles[issue_id]" type="Integer" required=true %}
Issue ID
{% endapi-method-parameter %}

{% api-method-parameter name="articles[unlock_type]" type="String" required=true %}
Unlock Type
{% endapi-method-parameter %}

{% api-method-parameter name="articles[position]" type="Integer" required=true %}
Order Position of the Article within an Issue
{% endapi-method-parameter %}

{% api-method-parameter name="articles[source]" type="String" required=true %}
Article type
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


