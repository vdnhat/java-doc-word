---
description: >-
  Context is a object of the core information that provides useful context about
  a data point, for example the user's IP address, locale or device,..
---

# Context Param

#### Creating an Context object

Each time calling the tracking event, you will need to create an Context object and fill out the context properties:

{% tabs %}
{% tab title="Swift" %}
```swift
let contextObj = ITContextObj(screenName: <String>, 
campaignName: <String>, campaignSource: <String>, 
campaignMedium: <String>, campaignTerm: <String>, 
campaignContent: <String>)
```
{% endtab %}

{% tab title="Objective-C" %}
```objectivec
ITContextObj *context1 = [[ITContextObj alloc] 
initWithScreenName:@"screen name"
campaignName:@"campaign name"
campaignSource:@"campaign source"
campaignMedium:@"campaign medium"
campaignTerm:@"campaign term"
campaignContent:@"campaign content"];
```
{% endtab %}
{% endtabs %}

#### Context Properties <a id="context-properties"></a>

<table>
  <thead>
    <tr>
      <th style="text-align:left"> <b>Name</b>
      </th>
      <th style="text-align:left"> <b>Type</b>
      </th>
      <th style="text-align:left"> <b>Description</b>
      </th>
      <th style="text-align:left"> <b>Default</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">screenName</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>The current navigation path: home,</p>
        <p>categories, search, detail,...</p>
      </td>
      <td style="text-align:left">null</td>
    </tr>
    <tr>
      <td style="text-align:left">campaignName</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">The campaign name</td>
      <td style="text-align:left">null</td>
    </tr>
    <tr>
      <td style="text-align:left">campaignSource</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">The campaign source</td>
      <td style="text-align:left">null</td>
    </tr>
    <tr>
      <td style="text-align:left">campaignMedium</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">The campaign medium</td>
      <td style="text-align:left">null</td>
    </tr>
    <tr>
      <td style="text-align:left">campaignContent</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">The campaign term</td>
      <td style="text-align:left">null</td>
    </tr>
    <tr>
      <td style="text-align:left">campaignTerm</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">The campaign content</td>
      <td style="text-align:left">null</td>
    </tr>
  </tbody>
</table>

