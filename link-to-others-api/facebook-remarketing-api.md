# Facebook Remarketing API

#### Before You Start

You will need:

* A [Facebook Developer Account](https://developers.facebook.com/apps)
* A [Facebook Ad Account ](https://www.facebook.com/ads/manager/accounts/)
* A [Facebook app](https://developers.facebook.com/docs/apps)

#### Configure Your Facebook App

Go to the [App Dashboard](https://developers.facebook.com/apps), click **My Apps**, and create a new app if you don't already have one. Navigate to **Settings** &gt; **Basic** to view the **App Details** Panel with your **App ID**, your **App Secret**, and other details about your app. 

Scroll down to the bottom of page, and click **Add Platform**. Choose **iOS**, add your app details, and save your changes.

Set up your app for advertising by adding the following details:

* **App Domains** - Provide Apple App Store URL of your app.
* **Privacy Policy URL** - Provide a [Privacy Policy](https://l.facebook.com/l.php?u=https%3A%2F%2Fen.wikipedia.org%2Fwiki%2FPrivacy_policy&h=AT2HUiHAnkjos3FqnW3UpXndcU6o9GOWlSWgH4E-8AYx1ukUwEKDApOHBeLIrJRW5zAcwGCRKdsGaG68rhLrd_vC8j_m_bUmyQwMvTYhyWaJxlGFP9xhX8kSQRInA6OnJkdnYfNqSt8) URL. Required to take your app public.
* **Terms of Service URL** - Provide a [Terms of Service](https://l.facebook.com/l.php?u=https%3A%2F%2Fen.wikipedia.org%2Fwiki%2FTerms_of_service&h=AT281XGs3pKpKN2JEV0Nkoqz3x4NSk8yUffxDbGvr64uc9ZTNiZQqDfQ4cl_zmt8XJUG-uhqtTwOFNDE12LgqLg8bnlsHLhReJApgZoHoEgrLEHp81fc9ScA_f7Nlb7YiUY31oM5ZDAd64Pg0MxM1ukW) URL.
* **Platform** - Scroll to the bottom of the Settings panel to add the iOS Platform.

#### Update the CDP365\_Config Configuration File

* Configure the information property list file \(`CDP365_Config.plist`\) with an XML snippet that contains data about your app.

1. Right-click `info.plist`, and choose **Open As Source Code**.
2. Copy and paste the following XML snippet into the body of your file \( `<dict>...</dict>`\).
3. In &lt;key&gt;, replace your key with follow define bellow: \(With each Facebook app id will manage a kind of event e-commerce\)

   `ID_AddToCarts`

   `ID_Purchase`

   `ID_ViewProduct`

   `ID_DetailProduct`

   `ID_ViewListProducts`

4. In `<string>` in the key, replace \[Access Token\] with format: \[Your app id\]\|\[Your app secret\] 

```text
<key>FacebookIDs</key>
	<dict>
		<key>[Your key (follow define)]</key>
		<string>[Access Token]</string>
	</dict>
```

* Example:

```text
<key>FacebookIDs</key>
	<dict>
		<key>ID_AddToCarts</key>
		<string>564378231162716|a41a23103dc371f2dbaa194cf1dbed6d</string>
		<key>ID_Purchase</key>
		<string>564378231162716|a41a23103dc371f2dbaa194cf1dbed6d</string>
		<key>ID_ViewProduct</key>
		<string>564378231162716|a41a23103dc371f2dbaa194cf1dbed6d</string>
		<key>ID_DetailProduct</key>
		<string>564378231162716|a41a23103dc371f2dbaa194cf1dbed6d</string>
	</dict>
```

{% api-method method="post" host="https://graph.facebook.com" path="/v7.0/\[FB\_App\_ID\]/activities" %}
{% api-method-summary %}
Send a event e-commerce
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="access\_token" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="JSON body" type="object" required=true %}
JSON data with required keys:   
"`event`",   
"`advertiser_id`",   
"`application_tracking_enabled`", "`advertiser_tracking_enabled`" ,   
"`custom_events`"  
And the key "`custom_events`" required keys:   
"`_eventName`",  
"`fb_content`",  
"`fb_content_type`",
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "success": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

* Example for body json data:

```markup
{
  "event": "CUSTOM_APP_EVENTS",
  "advertiser_id": "1111-1111-1111-1111",
  "application_tracking_enabled": "1",
  "advertiser_tracking_enabled": "1",
  "custom_events": [{
  	"_eventName": "fb_mobile_purchase",
  	"fb_content":[
  		{
  		"id": "1234",
  		"quantity": "1"
		},
		{
  		"id": "1214",
  		"quantity": "1"
		}
	],
  	"fb_content_type": "product",
  	"_valueToSum": 12234.8,
  	"fb_currency": "VND"
  }],
  "bundle_id": "com.ants.magento"
}
```

