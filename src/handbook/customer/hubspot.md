---
navTitle: Hubspot
---


We use [HubSpot](https://www.hubspot.com/) to track and manage all of our customer interactions.
It enables the creation of customer contacts, and then logging of emails/notes associated to that customer.

## Contact Management

Given that we have multiple client-facing roles within FlowFuse, it's important to document those that
we talk to to ensure no crossover in sales and conversations.

### Lifecycle Stage

All contacts in HubSpot need to have a defined lifecycle. It is required that all contacts pass through each lifecycle stage at the appropriate time based on their interaction with FlowFuse marketing and sales. Contacts should not skip a stage. It is up to the contact owner to ensure their contacts have the appropriate lifecycle stage set.

The folowing is a description of each stage. 

| Lifecycle Stage|Description
| - | - |
| Subscriber | Contact has signed up to hear more information, when it is available, about FlowFuse, e.g. newsletter subscriber |
| Lead | Contact that has converted on our website, or through some other interaction, with our organisation beyond a subscription sign up. For example, registered for a webinar, signed up for a free trial, etc.|
| Marketing Qualified Lead | The contact has requested to talk to someone directly at FlowFuse about the product/services of FlowFuse, either through book a demo, contact us, or direct outreach to a FlowFuse employee. Support requests are not considered MQL. |
| Product Qualified Lead | The Customer success team identifies a contact that they believe is a candidate for an upsell opportunity. Customer success will identify an PQL by monitoring FlowFuse Cloud usage and engaging with these users in a consultative manner. Any contact already identified as an MQL, SQL or Opportunity should not be a candidate for PQL. |
| Sales Qualified Lead | After the initial discussion with an MQL, the sales team will qualify if the contact is a potential customer by changing the lifecycle stage to SQL. This status of this stage is then further qualified in the [Lead Status](#lead-status) property. |
| Opportunity | A contact becomes an Opportunity once a Deal has been opened. The [3 W's need to be answered before opening a deal](#from-sql-to-opportunity)  |
| Customer | An active, paying, user of FlowFuse. |
| Evangelist | FlowFuse will not actively use Evangelist lifecycle stage. |
| Other | Does not fit into any of the other descriptions, likely someone we are talking to about FlowFuse, but will never be a paying customer, .e.g. Partners |

#### Lifecycle changes

##### From MQL to SQL - Qualifying questions

1. Have you adopted Node-RED? If so, what have you built with Node-RED?
1. How many Node Red instances do you have, and how many people are developing on Node-RED?
1. Is Node-RED used in production?	
1. What are you looking to build in the next year with Node-RED?

##### From SQL to Opportunity

For each sales opportunity a clear answer for the customers needs and wants should be known. It boils down to the following questions:

| Question | |
| :------- | :------ |
| Why change? | What's the trigger to invest in FlowFuse and Node-RED? |
| Why now? | Timeline is everything! |
| Why FlowFuse? | What value does FlowFuse offer to the customer, what features are of most interest? |

If, and only if, the answers are known and added as notes to HubSpot, an
opportunity is added to the HubSpot deals board.

| Deal Stages |  | |
| :------- | :--:| :---- |
| Opportunity | 10% | When there is a legitimate opportunity to close the prospect within the next 6 months. This stage is primarily triggered by the timeline or urgency of the need for FlowFuse. |
| POC Started | 30% | When the prospect enters a POC or has a POC kick-off call scheduled in the near future. |
| Value Validated | 60% | FlowFuse has been technically proven in a POC. Procurement steps typically follow or are running concurrently: security, legal, budget, DM intro/meeting. |
| Contract Sent | 90% | Contact is sent with an expiration date that has been communicated to the customer. While quotes may be sent at any time throughout the process, a deal should only enter this stage if it is reasonably guaranteed that a signature is pending based on current knowledge. |
| Closed Won/Lost | 0% || 100% | Deals in these stages will remain visible on the deal board to keep them top of mind for learnings and/or follow up. |

### Lead Status

For leads who are [MQLs or SQLs](#lifecycle-stage) the `Lead status`
field is used to mark what the status is. Even though they're beyond being a lead.
This field is maintained by the primary contact owner, likely the account executive.

At this stage we're using the default set of status's in HubSpot:

| Lead status | When to use |
| :---------: | :---------- |
| New | The contact in question has had only _marketing_ contact (E-mails, etc). |
| Open | In the stage where a contact is assigned to a Account exec, but no official connection has be made. Usually contacts are only in this stage for a short while.|
| Attempted to contact | From the moment the AE reached out, until there's a reply from them. |
| Connected | MQLs and SQL that have replied and engaged with FlowFuse. |
| In Progress | After contact has been made, this status captures the nurturing process toward an opportunity. |
| Open Deal | When a deal is on the board, and the opportunity is real, this is the status! |
| Unqualified | Either this contact specifically cannot lead the sales process, or the account itself has been found unqualified. |
| Unresponsive | We have not received a reply in 2 weeks, they are ghosting us. |
| Bad timing | FlowFuse was, for whatever reason, not a great fit right now. However, it's potentially a good fit later. |

### Outbound

`Activation Outbound` is a custom property that's set to `Yes` when the first meeting with the contact came through outbound
drip campaigns or other outbound lead-gen actions. This property will be set to `Yes` when the contact was in HubSpot
through other marketing activities too, but wasn't nurtured to the point of a meeting yet.

## Importing Contacts Into HubSpot

If you import contacts into HubSpot, it is important that the First Name and Last Name are populated correctly. Currently the FlowFuse Cloud database stores first and last name in a single field called Name. If you import this field into HubSpot the default is set to populate the Last Name field. The First Name field will not be populated so any email personalization with First Name will not be effective.  

The ideal process for importing FlowFuse Cloud contacts is that you first split the Name field into a First Name and Last Name. Google Sheets has the ability to split a column of text into two columns based on the delimiter of a space. Once that is completed then you can import the list into HubSpot.

## Recommended Apps

We have several extension applications for HubSpot, these are a few that can be beneficial if you're interacting with customers:

- **G-Mail Extension ([link](https://app-eu1.hubspot.com/ecosystem/26586079/marketplace/apps/sales/sales-enablement/gmail))** - Automatically creates contacts when you e-mail them for the first time, and logs e-mail activity against that contact in HubSpot.