# Google Conversion Tracking And Remarketing API

#### Create a develop token \(for ANTSER\)

1. You must have a [Google Ads Manager Account](https://support.google.com/google-ads/answer/7459399) to apply for access to the API. Manager Accounts **cannot** be created using the same email address as an **existing** Google Ads account. You must therefore use an email address that hasn't already been associated with a Google Ads account to create your Manager Account.
2. Sign up for AdWords API access through your **Manager Account**. [Sign in](https://ads.google.com/home/tools/manager-accounts/), then navigate to  **TOOLS & SETTINGS &gt; SETUP &gt; API Center**. The **API Center** option will appear only for Google Ads Manager Accounts. All fields on the API Access form must be completed, and the Terms and Conditions accepted. Make sure your information is correct and your company's website URL is functioning: If the website is not a live page, we won't be able to process your application.
3. This Google Ads Manager Account will a provider, the user will be link to this account to generate the link id.

#### Create a link id for your app

To create a Link ID, do the following:

1. From the Google Ads dashboard, click **Tools** &gt; **Setup** section &gt; select **Linked Accounts** ![](https://docs.mparticle.com/images/adwords-setup.png)
2. Navigate to the **Third-party app analytics** tile, click **Details**, select **Create Link ID** ![](https://docs.mparticle.com/images/adwords-linked-accounts.png)
3. Navigate to **App analytics provider** &gt; **Other provider**, and enter provider ID \(please contact ANTSOMI\)
4. Select your app’s platform and find your app in the **Look up your app** field.

        ![](https://docs.mparticle.com/images/adwords-provider-id.png)

  5. Click the **CREATE LINK ID** button. The screen refreshes to show you the Third-party app analytics page with the LINK IDs you’ve just created.

#### Update the ANInsight Configuration File

* Configure the information property list file \(`ANInsight.plist`\) with an XML snippet that contains data about your app.

1. Right-click `info.plist`, and choose **Open As Source Code**.
2. Copy and paste the following XML snippet into the body of your file \( `<dict>...</dict>`\).
3. In `<string>` in the key `Dev_Token`, replace \[Dev token\] with your Dev token \(contact for ANTSOMI to received token\).
4. In `<string>` in the key `LinkID`, replace \[Link id\] with your link id which generated before \(contact for ANTSOMI to received token\).

```text
<key>GoogleIDs</key>
	<dict>
		<key>Dev_Token</key>
		<string>[Dev token]</string>
		<key>LinkID</key>
		<string>[Link id]</string>
	</dict>
```

#### Conversion Tracking and Remarketing API \(Server to server\)

{% api-method method="post" host="www.googleadservices.com" path="/pagead/conversion/app/1.0" %}
{% api-method-summary %}
Send a event e-commerce
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="dev\_token" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="link\_id" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="app\_event\_type" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="rdid" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="idtype" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="lat" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="app\_version" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="os\_version" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="sdk\_version" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="timestamp" type="string" required=true %}

{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="app\_event\_data" type="object" required=false %}
JSON object. Example:  
{  
    "item\_id": "1234",  
    "value": 93435.22  
}
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "ad_events": [],
    "errors": [],
    "attributed": false
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

> #### Notes: The app\_event\_type follow defines:

| Events | Description |
| :--- | :--- |
| first\_open |  |
| session\_start |  |
| in\_app\_purchase |  |
| view\_item\_list |  |
| view\_item |  |
| view\_search\_results |  |
| add\_to\_cart |  |
| ecommerce\_purchase |  |

