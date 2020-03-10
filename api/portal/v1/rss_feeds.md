# RSS Feeds

API for managing rss feeds

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/rss_feeds/:app_id" %}

{% api-method-summary %}
List RSS Feeds
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a list of all `RSS Feeds` that belong to the publication
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
  "url": "https://blog.magloft.com/feed/",
  "title": "MagLoft Blog",
  "description": "MagLoft Blog Description",
  "cover": "https://mms.magloft.com/USERID/ASSETID",
  "active": true,
  "job_id": "123412341234",
  "job_status": "pending",
  "import_source": true,
  "import_author": true,
  "auto_publish": true,
  "show_related_articles": true,
  "imported_at": "2018-01-24 10:55:35",
  "created_at": "2018-01-24 10:55:35",
  "updated_at": "2018-01-24 10:55:35",
  "category_ids": [
    1,
    2,
    3
  ]
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="post" host="https://www.magloft.com" path="/api/portal/v1/rss_feeds/:app_id" %}

{% api-method-summary %}
Create RSS Feed
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **creates** a new `RSS Feed` and **returns** the saved `RSS Feed`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="url" type="String" required=true %}
External Blog URL to import articles from
{% endapi-method-parameter %}

{% api-method-parameter name="title" type="String" %}
Title of the RSS Feed
{% endapi-method-parameter %}

{% api-method-parameter name="import_source" type="Virtus::Attribute::Boolean" %}
Boolean indicating whether the RSS Feed will import source of article
{% endapi-method-parameter %}

{% api-method-parameter name="import_author" type="Virtus::Attribute::Boolean" %}
Boolean indicating whether the RSS Feed will import author of article
{% endapi-method-parameter %}

{% api-method-parameter name="show_related_articles" type="Virtus::Attribute::Boolean" %}
Boolean indicating whether the imported article will show related articles
{% endapi-method-parameter %}

{% api-method-parameter name="auto_publish" type="Virtus::Attribute::Boolean" %}
Boolean indicating whether the article from the RSS Feed will be automatically published
{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "url": "https://blog.magloft.com/feed/",
  "title": "MagLoft Blog",
  "description": "MagLoft Blog Description",
  "cover": "https://mms.magloft.com/USERID/ASSETID",
  "active": true,
  "job_id": "123412341234",
  "job_status": "pending",
  "import_source": true,
  "import_author": true,
  "auto_publish": true,
  "show_related_articles": true,
  "imported_at": "2018-01-24 10:55:35",
  "created_at": "2018-01-24 10:55:35",
  "updated_at": "2018-01-24 10:55:35",
  "category_ids": [
    1,
    2,
    3
  ]
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="get" host="https://www.magloft.com" path="/api/portal/v1/rss_feeds/:app_id/:id" %}

{% api-method-summary %}
Get RSS Feed
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **returns** a specific `rss feed` by `id`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
RSS Feed ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "url": "https://blog.magloft.com/feed/",
  "title": "MagLoft Blog",
  "description": "MagLoft Blog Description",
  "cover": "https://mms.magloft.com/USERID/ASSETID",
  "active": true,
  "job_id": "123412341234",
  "job_status": "pending",
  "import_source": true,
  "import_author": true,
  "auto_publish": true,
  "show_related_articles": true,
  "imported_at": "2018-01-24 10:55:35",
  "created_at": "2018-01-24 10:55:35",
  "updated_at": "2018-01-24 10:55:35",
  "category_ids": [
    1,
    2,
    3
  ]
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="put" host="https://www.magloft.com" path="/api/portal/v1/rss_feeds/:app_id/:id" %}

{% api-method-summary %}
Update RSS Feed
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **updates** a specific `rss feed` by `id` and **returns** the updated `rss feed`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" %}
RSS Feed ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}



{% api-method-body-parameters %}

{% api-method-parameter name="title" type="String" %}
Title of the RSS Feed
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="String" %}
Description of the RSS Feed
{% endapi-method-parameter %}

{% api-method-parameter name="cover" type="String" %}
Cover URL of the RSS Feed
{% endapi-method-parameter %}

{% api-method-parameter name="active" type="Virtus::Attribute::Boolean" %}
Boolean indicating whether the RSS Feed is currently active
{% endapi-method-parameter %}

{% api-method-parameter name="import_source" type="Virtus::Attribute::Boolean" %}
Boolean indicating whether the RSS Feed will import source of article
{% endapi-method-parameter %}

{% api-method-parameter name="import_author" type="Virtus::Attribute::Boolean" %}
Boolean indicating whether the RSS Feed will import author of article
{% endapi-method-parameter %}

{% api-method-parameter name="auto_publish" type="Virtus::Attribute::Boolean" %}
Boolean indicating whether the article from the RSS Feed will be automatically published
{% endapi-method-parameter %}

{% api-method-parameter name="show_related_articles" type="Virtus::Attribute::Boolean" %}
Boolean indicating whether the imported article will show related articles
{% endapi-method-parameter %}

{% endapi-method-body-parameters %}

{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "url": "https://blog.magloft.com/feed/",
  "title": "MagLoft Blog",
  "description": "MagLoft Blog Description",
  "cover": "https://mms.magloft.com/USERID/ASSETID",
  "active": true,
  "job_id": "123412341234",
  "job_status": "pending",
  "import_source": true,
  "import_author": true,
  "auto_publish": true,
  "show_related_articles": true,
  "imported_at": "2018-01-24 10:55:35",
  "created_at": "2018-01-24 10:55:35",
  "updated_at": "2018-01-24 10:55:35",
  "category_ids": [
    1,
    2,
    3
  ]
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}

{% api-method method="delete" host="https://www.magloft.com" path="/api/portal/v1/rss_feeds/:app_id/:id" %}

{% api-method-summary %}
Delete RSS Feed
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **deletes** a specific `RSS Feed` by `id` and **returns** an `empty response` with status `204`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
RSS Feed ID
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

{% api-method method="post" host="https://www.magloft.com" path="/api/portal/v1/rss_feeds/:app_id/:id/synchronize" %}

{% api-method-summary %}
Synchronize RSS Feed
{% endapi-method-summary %}

{% api-method-description %}
This endpoint **synchronizes** entries from an existing `RSS Feed` by `id` and **returns** the `synchronization results`
{% endapi-method-description %}

{% api-method-spec %}

{% api-method-request %}

{% api-method-path-parameters %}

{% api-method-parameter name="app_id" type="String" required=true %}
App ID (Publication) to scope this request for.
{% endapi-method-parameter %}

{% api-method-parameter name="id" type="Integer" required=true %}
RSS Feed ID
{% endapi-method-parameter %}

{% endapi-method-path-parameters %}




{% endapi-method-request %}

{% api-method-response %}

{% api-method-response-example httpCode=200 %}

```json
{
  "id": 1234,
  "url": "https://blog.magloft.com/feed/",
  "title": "MagLoft Blog",
  "description": "MagLoft Blog Description",
  "cover": "https://mms.magloft.com/USERID/ASSETID",
  "active": true,
  "job_id": "123412341234",
  "job_status": "pending",
  "import_source": true,
  "import_author": true,
  "auto_publish": true,
  "show_related_articles": true,
  "imported_at": "2018-01-24 10:55:35",
  "created_at": "2018-01-24 10:55:35",
  "updated_at": "2018-01-24 10:55:35",
  "category_ids": [
    1,
    2,
    3
  ]
}
```

{% endapi-method-response-example %}

{% endapi-method-response %}

{% endapi-method-spec %}

{% endapi-method %}


