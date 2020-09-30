# Log Event

Tracks an event. To track an event anywhere in the app, call:

{% tabs %}
{% tab title="Swift" %}
```swift
ITAnalytic.logEvent(action: <ITActionEvent>, contextObject: 
<ITContextObj>,extraObject: <ITExtraObj>, 
dimsObject: <[ITDimsObj]>, items: <[ITItemObj]>)
```
{% endtab %}

{% tab title="Objective-C" %}
```objectivec
[ITAnalytics logEventWithAction:<ITActionEvent>
contextObject:<ITContextObj>
extraObject:<ITExtraObj>
 dimsObject:<[ITDimsObj]>
itemsObject:<[ITItemObj]>];
```
{% endtab %}
{% endtabs %}

 **Parameters:**

<table>
  <thead>
    <tr>
      <th style="text-align:left"> <b>Parameters</b>
      </th>
      <th style="text-align:left"> <b>Required?</b>
      </th>
      <th style="text-align:left"> <b>Description</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">actionName</td>
      <td style="text-align:left">Yes</td>
      <td style="text-align:left">
        <p>The name of the event you wish to track which action</p>
        <p>defined in the ITActionEvent before.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">contextObject</td>
      <td style="text-align:left">No</td>
      <td style="text-align:left">Context is a ITContextObj object of the core information that provides
        useful context</td>
    </tr>
    <tr>
      <td style="text-align:left">extraObject</td>
      <td style="text-align:left">No</td>
      <td style="text-align:left">Extra is a ITExtraObj object of extra information that provides useful
        such as e-com properties</td>
    </tr>
    <tr>
      <td style="text-align:left">dimsObject</td>
      <td style="text-align:left">No</td>
      <td style="text-align:left">Dims is a list ITDimsObj object of the relation items that provides .
        You should only use Dims types for their intended meaning.</td>
    </tr>
    <tr>
      <td style="text-align:left">items</td>
      <td style="text-align:left">No</td>
      <td style="text-align:left">Items is a list object (user or product item)</td>
    </tr>
  </tbody>
</table>

**There are action event list to tracks:**

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Action Name</b>
      </th>
      <th style="text-align:left"><b>Description</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">ITActionEventScreenView</td>
      <td style="text-align:left">When app screen start loading</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventUserRegister</td>
      <td style="text-align:left">When a user registers account</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventSignIn</td>
      <td style="text-align:left">When a user login to your app</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventSignOut</td>
      <td style="text-align:left">When a user log out for your app</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventIdentify</td>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li>After a user registers</li>
          <li>After a user logs in</li>
          <li>When a user updates their info (eg. changes or add a new address)</li>
          <li>Upon loading any pages that are accessible by a logged in user (optional)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventProductSearch</td>
      <td style="text-align:left">User searched for products</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventProductListView</td>
      <td style="text-align:left">User viewed a product list or category</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventProductListFilter</td>
      <td style="text-align:left">User filtered a product list or category</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventProductClick</td>
      <td style="text-align:left">User clicked on a product</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventProductView</td>
      <td style="text-align:left">User viewed a product detail</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventProductAddWish</td>
      <td style="text-align:left">User added a product to my list wish</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventProductViewWish</td>
      <td style="text-align:left">User viewed their wish list</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventProductAddCompare</td>
      <td style="text-align:left">User added a product to compare</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventProductViewCompare</td>
      <td style="text-align:left">User viewed their compare list</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventAddToCart</td>
      <td style="text-align:left">User added a product to their shopping cart</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventViewCart</td>
      <td style="text-align:left">User viewed their shopping cart</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventRemoveCart</td>
      <td style="text-align:left">User removed a product from their shopping cart</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventProductCheckout</td>
      <td style="text-align:left">User initiated the order process (a transaction is created)</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventProductPayment</td>
      <td style="text-align:left">User added payment information</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventProductPurchase</td>
      <td style="text-align:left">User purchased and completed the order</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventAdvertisingImpression</td>
      <td style="text-align:left">Counts an impression each time a creative is downloaded in the user&apos;s
        device and has begun to load</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventAdvertisingView</td>
      <td style="text-align:left">When the creative is shown to the user</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventAdvertisingClick</td>
      <td style="text-align:left">When a user clicks on an ad creative, a click request is send to the event
        analytic server</td>
    </tr>
    <tr>
      <td style="text-align:left">ITActionEventAllowPushNotification</td>
      <td style="text-align:left">When a user allow push notification service</td>
    </tr>
  </tbody>
</table>

