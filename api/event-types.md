---
description: There are event list strategy for list events to tracking.
---

# Event types

## 1. Page \(On Web\)

| **Group** |  **Name** | **Category** | **Action** | Trigger |
| :--- | :--- | :--- | :--- | :--- |
| Page | Page view | pageview | view | Page loaded |

## 2. Screen \(On App\)

| **Group** |  **Name** | **Category** | **Action** | Trigger |
| :--- | :--- | :--- | :--- | :--- |
| Screen | Screen view | screenview | view | Screen loaded |

## 3. User Identify

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Group</b>
      </th>
      <th style="text-align:left"><b> Name</b>
      </th>
      <th style="text-align:left"><b>Category</b>
      </th>
      <th style="text-align:left"><b>Action</b>
      </th>
      <th style="text-align:left">Trigger</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">User Identify</td>
      <td style="text-align:left">User Identify</td>
      <td style="text-align:left">user</td>
      <td style="text-align:left">identify</td>
      <td style="text-align:left">
        <ul>
          <li>After a user registers</li>
          <li>After a user logs in</li>
          <li>When a user updates their info (eg changes or adds a new address)</li>
          <li>Upon loading any pages that are accessible by a logged in user (optional)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">User Identify</td>
      <td style="text-align:left">User Sign-out</td>
      <td style="text-align:left">user</td>
      <td style="text-align:left">sign_out</td>
      <td style="text-align:left">This event should be sent when a user signs out for your service.</td>
    </tr>
  </tbody>
</table>

## 4. User Anonymous

> The reset method only clears the cookies and localStorage set by SDK . User generates a **uid** and sets this as anonymousId for all new visitors to your site/app.

| **Group** |  **Name** | **Category** | **Action** | Trigger |
| :--- | :--- | :--- | :--- | :--- |
| User Identify | Reset anonymous  | user | reset\_anonymous\_id | Calling reset resets the user\_id \(uid\) when user sign out and sign in with an other account.  |

## 5. Ecommerce Events

| **Group** |  **Name** | **Category** | **Action** | Trigger |
| :--- | :--- | :--- | :--- | :--- |
| Ecommerce | Products Searched | browsing  | product\_search | User searched for products |
| Ecommerce | Product List Viewed | browsing | product\_list\_view | User viewed a product list or category |
| Ecommerce | Product List Filtered | browsing | product\_list\_filter | User filtered a product list or category |
| Ecommerce | Product click | product | click | User clicked on a product |
| Ecommerce | Product view | product | view | User viewed a product details |
| Ecommerce | Add Wish  | product | add\_wish\_list | User added a product to my list wish. |
| Ecommerce | Add compare  | product | add\_compare | User added a product to compare. |
| Ecommerce | Add to Cart  | product | add\_to\_cart | User added a product to their shopping cart |
| Ecommerce | Remove  Cart | product | remove\_cart | User removed a product from their shopping cart |
| Ecommerce | Cart view | product | view\_cart | User viewed their shopping cart |
| Ecommerce | View wish list | product | view\_wish\_list | User viewed their wish list |
| Ecommerce | View compare list | product | compare\_list | User viewed their compare list |
| Ecommerce | Cart checkout | product | checkout | User initiated the order process \(a transaction is created\) |
| Ecommerce | Payment Info Entered | product | payment | User added payment information |
| Ecommerce | Purchase  | product | purchase | User purchased and completed the order |

## 6. Advertising  \(On any platforms\)

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Group</b>
      </th>
      <th style="text-align:left"><b> Name</b>
      </th>
      <th style="text-align:left"><b>Category</b>
      </th>
      <th style="text-align:left"><b>Action</b>
      </th>
      <th style="text-align:left">Trigger</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p></p>
        <p>Advertising</p>
      </td>
      <td style="text-align:left">Impression</td>
      <td style="text-align:left">advertising</td>
      <td style="text-align:left">impression</td>
      <td style="text-align:left">Counts an impression each time a creative is downloaded in the user&apos;s
        device and has begun to load.</td>
    </tr>
    <tr>
      <td style="text-align:left">Advertising</td>
      <td style="text-align:left">Viewable</td>
      <td style="text-align:left">advertising</td>
      <td style="text-align:left">view</td>
      <td style="text-align:left">when the creative is shown to the user</td>
    </tr>
    <tr>
      <td style="text-align:left">Advertising performance</td>
      <td style="text-align:left">Click</td>
      <td style="text-align:left">advertising</td>
      <td style="text-align:left">view</td>
      <td style="text-align:left">When a user clicks on an ad creative, a click request is sent to the event
        analytics server. System counts a click as soon as it receives the click
        request and then sends the user the defined click-through URL and redirected
        to this one</td>
    </tr>
  </tbody>
</table>

## 7. Custom Events \(On any platforms\)

| **Group** |  **Name** | **Category** | **Action** | Trigger |
| :--- | :--- | :--- | :--- | :--- |
| **Event Group X** | **Any event** | **event name Y** | **event action** |  |
| Custom   | User Login  | user | sign-in |  |
| Custom  Event  | User  | user | user\_register |  |
| Custom  Event | User Sign-out | user | user\_sign-out |  |
| Custom  Event | User Like | user | like |  |
| Custom  Event | User  | user | share |  |
| Custom  Event | User  | user | comment |  |
| ... | ... | ... | ... |  |

