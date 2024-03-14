# Billing Webhook

This webhook is essential for externally billed apps within our marketplace. It must be accessed by developers to authorize the installation of the app.

The primary purpose of this webhook is to capture and update payment information for apps that employ a Paid business model and do not utilize HighLevel's internal billing mechanism.

## 1. Prerequisites for using this webhook

Before using this webhook, ensure that you meet the following prerequisites on the [Marketplace](https://marketplace.gohighlevel.com):

1. You should have an app with a Business Model marked as Paid.
2. External Billing must be enabled for your app.
3. You must have entered the Billing URL.

## 2. Retrieving Parameters from the Billing URL

When an Agency or Location installs your app, they will be redirected to the Billing URL specified in the configuration. You will receive the following parameters in the URL:

| Parameter Name | Possible Values      | Notes                                                                   |
| -------------- | -------------------- | ----------------------------------------------------------------------- |
| clientId       | `<client_id>`        | Used for validation.                                                    |
| installType    | `location`, `agency` | You will receive `agency,location` in case of both agency and location. |
| locationId     | `<location_id>`      | You will receive this in case of `location` or `agency,location`.       |
| companyId      | `<agency_id>`        | You will receive this in case of `agency` or `agency,location`.         |

## 3. Using The Webhook

After successfully processing the payment on your end, you need to make a request to our billing webhook endpoint:

```
https://services.leadconnectorhq.com/oauth/billing/webhook
```

The parameters you need to include in the webhook request are as follows:

**Request Method:**
POST

**Request Headers:**

| Name                | Value              | Notes                                                                          |
| ------------------- | ------------------ | ------------------------------------------------------------------------------ |
| x-ghl-client-key    | Your client key    | This should be from the same client for which you are authorizing the payment. |
| x-ghl-client-secret | Your Client Secret | The corresponding client secret for the client key used.                       |
| Content-Type        | application/json   |

**Request Body:**

| Name           | Value                | Notes                                                             |
| -------------- | -------------------- | ----------------------------------------------------------------- |
| clientId       | Your client ID       |                                                                   |
| authType       | Enum                 | Possible values are `company` and `location`.                     |
| locationId     | `<location_id>`      | Required when authType is `location`.                             |
| companyId      | `<company_id>`       | Required when authType is `company`.                              |
| subscriptionId | Your subscription ID | You can include this if you have configured a subscription model. |
| paymentId      | Your Payment ID      | In case of a one-time payment model, you can send this parameter. |
| amount         | Billed Amount        | Required.                                                         |
| status         | Enum                 | Possible values are `COMPLETED` and `FAILED`.                     |
| paymentType    | Enum                 | Possible values are `one_time` and `recurring`.                   |

### Example

Here is a sample cURL command for the webhook request:

```shell
curl --location 'https://services.leadconnectorhq.com/oauth/billing/webhook' \
--header 'x-ghl-client-key: <client_key>' \
--header 'x-ghl-client-secret: <client_secret>' \
--header 'Content-Type: application/json' \
--data '{
    "clientId": "<client_id>",
    "authType": "location",
    "locationId": "<location_id>",
    "subscriptionId": "<subscription_id>",
    "paymentId": "<payment_id>",
    "amount": 12,
    "status": "COMPLETED",
    "paymentType": "recurring"
}'
```

## Webhook FAQs

### Can I get multiple location ids in the Billing URL?

Yes, in the case of multiple installations, you will receive a list of locationIds in a comma-separated format in the billing URL.

### Can I update for multiple locations in one call?

No, you need to trigger the webhook for each location and company separately.
