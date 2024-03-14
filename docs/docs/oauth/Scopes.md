---
tags: [OAuth 2.0]
stoplight-id: vcctp9t1w8hja
---

# **Scopes**

Here is a list of the scopes you require to access the API Endpoints and Webhook Events.

| Scope                           | API Endpoints                                                         | Webhook Events                      | Access Type          |
| ------------------------------- | --------------------------------------------------------------------- | ----------------------------------- | -------------------- |
| businesses.readonly             | GET /businesses                                                       |                                     | Sub-Account          |
| &nbsp;                          | GET /businesses/:businessId                                           |                                     | Sub-Account          |
| businesses.write                | POST /businesses                                                      |                                     | Sub-Account          |
| &nbsp;                          | PUT /businesses/:businessId                                           |                                     | Sub-Account          |
| &nbsp;                          | DELETE /businesses/:businessId                                        |                                     | Sub-Account          |
| calendars.write                 | POST /calendars/                                                      |                                     | Sub-Account          |
| &nbsp;                          | PUT /calendars/:calendarId                                            |                                     | Sub-Account          |
| &nbsp;                          | DELETE /calendars/:calendarId                                         |                                     | Sub-Account          |
| calendars.readonly              | GET /calendars/                                                       |                                     | Sub-Account          |
| &nbsp;                          | GET /calendars/:calendarId                                            |                                     | Sub-Account          |
| &nbsp;                          | GET /calendars/:calendarId/free-slots                                 |                                     | Sub-Account          |
| calendars/groups.readonly       | GET /calendars/groups                                                 |                                     | Sub-Account          |
| calendars/groups.write          | POST /calendars/groups                                                |                                     | Sub-Account          |
| &nbsp;                          | POST /calendars/groups/validate-slug                                  |                                     | Sub-Account          |
| &nbsp;                          | DELETE /calendars/groups/:groupId                                     |                                     | Sub-Account          |
| &nbsp;                          | PUT /calendars/groups/:groupId                                        |                                     | Sub-Account          |
| &nbsp;                          | PUT /calendars/groups/:groupId/status                                 |                                     | Sub-Account          |
| calendars/resources.readonly    | GET /calendars/resources/:resourceType                                |                                     | Sub-Account          |
| &nbsp;                          | GET /calendars/resources/:resourceType/:id                            |                                     | Sub-Account          |
| calendars/resources.write       | POST /calendars/resources                                             |                                     | Sub-Account          |
| &nbsp;                          | PUT /calendars/resources/:resourceType/:id                            |                                     | Sub-Account          |
| &nbsp;                          | DELETE /calendars/resources/:resourceType/:id                         |                                     | Sub-Account          |
| calendars/events.readonly       | GET /calendars/events/appointments/:eventId                           |                                     | Sub-Account          |
| &nbsp;                          | GET /calendars/events                                                 |                                     | Sub-Account          |
| &nbsp;                          | GET /calendars/blocked-slots                                          |                                     | Sub-Account          |
| calendars/events.write          | DELETE /calendars/events/:eventId                                     |                                     | Sub-Account          |
| &nbsp;                          | POST /calendars/events/block-slots                                    |                                     | Sub-Account          |
| &nbsp;                          | PUT /calendars/events/block-slots/:eventId                            |                                     | Sub-Account          |
| &nbsp;                          | POST /calendars/events/appointments                                   |                                     | Sub-Account          |
| &nbsp;                          | PUT /calendars/events/appointments /:eventId                          |                                     | Sub-Account          |
| campaigns.readonly              | GET /campaigns/                                                       | CampaignStatusUpdate                | Sub-Account          |
| contacts.readonly               | GET /contacts/:contactId                                              | ContactCreate                       | Sub-Account          |
| &nbsp;                          | GET /contacts/:contactId/tasks                                        | ContactDelete                       | Sub-Account          |
| &nbsp;                          | GET /contacts/:contactId/tasks/:taskId                                | ContactDndUpdate                    | Sub-Account          |
| &nbsp;                          | GET /contacts/:contactId/notes                                        | ContactTagUpdate                    | Sub-Account          |
| &nbsp;                          | GET /contacts/:contactId/notes/:id                                    | NoteCreate                          | Sub-Account          |
| &nbsp;                          | GET /contacts/:contactId/appointments                                 | NoteDelete                          | Sub-Account          |
| &nbsp;                          | GET /contacts/                                                        | TaskCreate                          | Sub-Account          |
| &nbsp;                          | GET /contacts/business/:businessId                                    | TaskDelete                          | Sub-Account          |
| contacts.write                  | POST /contacts/                                                       | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /contacts/:contactId                                              | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /contacts/:contactId                                           | &nbsp;                              | Sub-Account          |
| &nbsp;                          | POST /contacts/:contactId/tasks                                       | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /contacts/:contactId/tasks/:taskId                                | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /contacts/:contactId/tasks/:taskId/completed                      | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /contacts/:contactId/tasks/:taskId                             | &nbsp;                              | Sub-Account          |
| &nbsp;                          | POST /contacts/:contactId/tags                                        | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /contacts/:contactId/tags                                      | &nbsp;                              | Sub-Account          |
| &nbsp;                          | POST /contacts/:contactId/notes                                       | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /contacts/:contactId/notes/:id                                    | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /contacts/:contactId/notes/:id                                 | &nbsp;                              | Sub-Account          |
| &nbsp;                          | POST /contacts/:contactId/campaigns/:campaignId                       | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /contacts/:contactId/campaigns/removeAll                       | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /contacts/:contactId/campaigns/:campaignId                     | &nbsp;                              | Sub-Account          |
| &nbsp;                          | POST /contacts/:contactId/workflow/:workflowId                        | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /contacts/:contactId/workflow/:workflowId                      | &nbsp;                              | Sub-Account          |
| conversations.readonly          | GET /conversations/:conversationsId                                   | ConversationUnreadWebhook           | Sub-Account          |
| &nbsp;                          | GET /conversations/search                                             | &nbsp;                              | Sub-Account          |
| conversations.write             | POST /conversations/                                                  | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /conversations/:conversationsId                                   | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /conversations/:conversationsId                                | &nbsp;                              | Sub-Account          |
| conversations/message.readonly  | GET conversations/messages/:messageId/locations/:locationId/recording | InboundMessage                      | Sub-Account          |
| &nbsp;                          |                                                                       | OutboundMessage                     | Sub-Account          |
| conversations/message.write     | POST /conversations/messages                                          | ConversationProviderOutboundMessage | Sub-Account          |
| &nbsp;                          | POST /conversations/messages/inbound                                  | &nbsp;                              | Sub-Account          |
| &nbsp;                          | POST /conversations/messages/upload                                   | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /conversations/messages/:messageId/status                         | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /conversations/messages/:messageId/schedule                    | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /conversations/messages/email/:emailMessageId/schedule         | &nbsp;                              | Sub-Account          |
| forms.readonly                  | GET /forms/                                                           | &nbsp;                              | Sub-Account          |
| &nbsp;                          | GET /forms/submissions                                                | &nbsp;                              | Sub-Account          |
| invoices.readonly               | GET /invoices/                                                        | &nbsp;                              | Sub-Account          |
| &nbsp;                          | GET /invoices/:invoiceId                                              | &nbsp;                              | Sub-Account          |
| &nbsp;                          | GET /invoices/generate-invoice-number                                 | &nbsp;                              | Sub-Account          |
| invoices.write                  | POST /invoices                                                        | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /invoices/:invoiceId                                              | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /invoices/:invoiceId                                           | &nbsp;                              | Sub-Account          |
| &nbsp;                          | POST /invoices/:invoiceId/send                                        | &nbsp;                              | Sub-Account          |
| &nbsp;                          | POST /invoices/:invoiceId/void                                        | &nbsp;                              | Sub-Account          |
| &nbsp;                          | POST /invoices/:invoiceId/record-payment                              | &nbsp;                              | Sub-Account          |
| &nbsp;                          | POST /invoices/text2pay                                               | &nbsp;                              | Sub-Account          |
| invoices/schedule.readonly      | GET /invoices/schedule/                                               | &nbsp;                              | Sub-Account          |
| &nbsp;                          | GET /invoices/schedule/:scheduleId                                    | &nbsp;                              | Sub-Account          |
| invoices/schedule.write         | POST /invoices/schedule                                               | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /invoices/schedule/:scheduleId                                    | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /invoices/schedule/:scheduleId                                 | &nbsp;                              | Sub-Account          |
| &nbsp;                          | POST /invoices/schedule/:scheduleId/schedule                          | &nbsp;                              | Sub-Account          |
| &nbsp;                          | POST /invoices/schedule/:scheduleId/auto-payment                      | &nbsp;                              | Sub-Account          |
| &nbsp;                          | POST /invoices/schedule/:scheduleId/cancel                            | &nbsp;                              | Sub-Account          |
| invoices/template.readonly      | GET /invoices/template/                                               | &nbsp;                              | Sub-Account          |
| &nbsp;                          | GET /invoices/template/:templateId                                    | &nbsp;                              | Sub-Account          |
| invoices/template.write         | POST /invoices/template/                                              | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /invoices/template/:templateId                                    | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /invoices/template/:templateId                                 | &nbsp;                              | Sub-Account          |
| links.readonly                  | GET /links/                                                           | &nbsp;                              | Sub-Account          |
| links.write                     | POST /links/                                                          | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /links/:linkId                                                    | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /links/:linkId                                                 | &nbsp;                              | Sub-Account          |
| locations.readonly              | GET /locations/:locationId                                            | LocationCreate                      | Sub-Account, Company |
|                                 |                                                                       | LocationUpdate                      | Sub-Account, Company |
|                                 | GET /locations/search                                                 | &nbsp;                              | Sub-Account, Company |
|                                 | GET /locations/timeZones                                              | &nbsp;                              | Sub-Account          |
| locations.write                 | POST /locations/                                                      | &nbsp;                              | Company              |
|                                 | PUT /locations/:locationId                                            | &nbsp;                              | Company              |
|                                 | DELETE /locations/:locationId                                         | &nbsp;                              | Company              |
| locations/customValues.readonly | GET /locations/:locationId/customValues                               | &nbsp;                              | Sub-Account          |
| &nbsp;                          | GET /locations/:locationId/customValues/:id                           | &nbsp;                              | Sub-Account          |
| locations/customValues.write    | POST /locations/:locationId/customValues                              | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /locations/:locationId/customValues/:id                           | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /locations/:locationId/customValues/:id                        | &nbsp;                              | Sub-Account          |
| locations/customFields.readonly | GET /locations/:locationId/customFields                               | &nbsp;                              | Sub-Account          |
| &nbsp;                          | GET /locations/:locationId/customFields/:id                           | &nbsp;                              | Sub-Account          |
| locations/customFields.write    | POST /locations/:locationId/customFields                              | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /locations/:locationId/customFields/:id                           | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /locations/:locationId/customFields/:id                        | &nbsp;                              | Sub-Account          |
| locations/tags.readonly         | GET /locations/:locationId/tags                                       | &nbsp;                              | Sub-Account          |
|                                 | GET /locations/:locationId/tags/:tagId                                | &nbsp;                              | Sub-Account          |
| locations/tags.write            | POST /locations/:locationId/tags/                                     | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /locations/:locationId/tags/:tagId                                | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /locations/:locationId/tags/:tagId                             | &nbsp;                              | Sub-Account          |
| locations/templates.readonly    | GET /locations/:locationId/templates                                  | &nbsp;                              | Sub-Account          |
| locations/tasks.readonly        | POST /locations/:locationId/tasks/search                              | &nbsp;                              | Sub-Account          |
| medias.readonly                 | GET /medias/files                                                     | &nbsp;                              | Sub-Account          |
| medias.write                    | POST /medias/upload-file                                              | &nbsp;                              | Sub-Account          |
| funnels/redirect.readonly       | GET /funnels/lookup/redirect/list                                     | &nbsp;                              | Sub-Account          |
| funnels/redirect.write          | POST /funnels/lookup/redirect                                         | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /funnels/lookup/redirect/:id                                   | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PATCH /funnels/lookup/redirect/:id                                    | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /medias/:fileId                                                | &nbsp;                              | Sub-Account          |
| opportunities.readonly          | GET /opportunities/search                                             | OpportunityCreate                   | Sub-Account          |
| &nbsp;                          | GET /opportunities/:id                                                | OpportunityDelete                   | Sub-Account          |
| &nbsp;                          | GET /opportunities/pipelines                                          | OpportunityStageUpdate              | Sub-Account          |
| &nbsp;                          | &nbsp;                                                                | OpportunityStatusUpdate             | Sub-Account          |
| &nbsp;                          | &nbsp;                                                                | OpportunityMonetaryValueUpdate      | Sub-Account          |
| opportunities.write             | DELETE /opportunities/:id                                             | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /opportunities/:id/status                                         | &nbsp;                              | Sub-Account          |
| &nbsp;                          | POST /opportunities                                                   | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /opportunities/:id                                                | &nbsp;                              | Sub-Account          |
| payments/orders.readonly        | GET /payments/orders/                                                 | &nbsp;                              | Sub-Account          |
| &nbsp;                          | GET /payments/orders/:orderId                                         | &nbsp;                              | Sub-Account          |
| payments/transactions.readonly  | GET /payments/transactions/                                           | &nbsp;                              | Sub-Account          |
| &nbsp;                          | GET /payments/transactions/:transactionId                             | &nbsp;                              | Sub-Account          |
| payments/subscriptions.readonly | GET /payments/subscriptions/                                          | &nbsp;                              | Sub-Account          |
| &nbsp;                          | GET /payments/subscriptions/:subscriptionId                           | &nbsp;                              | Sub-Account          |
| products.readonly               | GET /products/                                                        | &nbsp;                              | Sub-Account          |
| &nbsp;                          | GET /products/:productId                                              | &nbsp;                              | Sub-Account          |
| products.write                  | POST /products/                                                       | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /products/:productId                                              | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /products/:productId                                           | &nbsp;                              | Sub-Account          |
| products/prices.readonly        | GET /products/:productId/price/                                       | &nbsp;                              | Sub-Account          |
| &nbsp;                          | GET /products/:productId/price/:priceId                               | &nbsp;                              | Sub-Account          |
| products/prices.write           | POST /products/:productId/price/                                      | &nbsp;                              | Sub-Account          |
| &nbsp;                          | PUT /products/:productId/price/:priceId                               | &nbsp;                              | Sub-Account          |
| &nbsp;                          | DELETE /products/:productId/price/:priceId                            | &nbsp;                              | Sub-Account          |
| oauth.readonly                  | GET /oauth/installedLocations                                         | &nbsp;                              | Company              |
| oauth.write                     | POST /oauth/locationToken                                             | &nbsp;                              | Company              |
| saas/location.write             | PUT /update-saas-subscription/:locationId                             | &nbsp;                              | Sub-Account, Company |
| &nbsp;                          | POST /enable-saas/:locationId                                         | &nbsp;                              | Sub-Account, Company |
| saas/location.read              | GET /locations                                                        | &nbsp;                              | Sub-Account, Company |
| saas/company.write              | POST /bulk-disable-saas/:companyId                                    | &nbsp;                              | Sub-Account, Company |
| snapshots.readonly              | GET /snapshots                                                        | &nbsp;                              | Company              |
| surveys.readonly                | GET /surveys/                                                         | &nbsp;                              | Sub-Account          |
| &nbsp;                          | GET /surveys/submissions                                              | &nbsp;                              | Sub-Account          |
| users.readonly                  | GET /users/                                                           | &nbsp;                              | Sub-Account, Company |
| &nbsp;                          | GET /users/:userId                                                    | &nbsp;                              | Sub-Account, Company |
| users.write                     | POST /users/                                                          | &nbsp;                              | Sub-Account, Company |
| &nbsp;                          | DELETE /users/:userId                                                 | &nbsp;                              | Sub-Account, Company |
| &nbsp;                          | PUT /users/:userId                                                    | &nbsp;                              | Sub-Account, Company |
| workflows.readonly              | GET /workflows/                                                       | &nbsp;                              | Sub-Account          |
