# MyTVH Product Decision Records

These decisions are recorded to evidence to the decisions taken by the Service team on any given features / strategic directions.

They can be used to understand why certain decisions are taken, or why some options might have been chosen/discarded.

## List of Product Decisions ##

### 1. Scoping of the MVP for Sending bulk SMS to residents for communal repairs/outages ###

As a resident who is affected by an outage or a communal repair,
I need to know that MTVH is aware of it and is doing something about it,
So that I do not have to chase them for updates.

MTVH also needs to proactively target residents who are affected by the same issue, so that the organisation does not receive calls of the same nature over and over again.

Based on the mock-ups provided by the MTVH team, the feature is supposed to:

- be kicked off by an agent from an existing repair in MyTVH
- who is then presented with a list of affected units attached to that repair (this is done via `list_people_incident_contacts(property_ref)`
- who then filters out the units that is not wanted
- composes the message
- sends

From an MVP point of view, the thinnest piece we think we can slice this for a sprint work is to do:

- agent starting the process from a repair
- agent sees a list of phone numbers attached to the units for that repair
- agent composes the message
- agent sends the SMS

The filtering, adding/removing units is de-scoped at the moment. So is enriching the list of units data through more granular data from Keystone.

### UPDATE 22 May ###

We had to re-scope the MVP given the time that's left in the Sprint. In order for us to hit the same outcome and value to the end users (being able to send an SMS to a list of recipients attached to a repair), the following are in scope:

- agent starting the process from a repair
- agent sees a list of phone numbers attached to the units for that repair

The composition of the SMS and the sending of it will be handled by Notify for the time being.

### 2. Using Gov.uk Notify for sending bulk SMS to residents ###

We need a service that sends SMS messages to residents based on the phone number information and the text that will be composed by the agent in the first instance.

Notify is a mature common component developed by Government Digital Service, offered to public sector organisations. It is well looked after by GDS, continuously iterated, and plugs in well with Ruby apps.

We will be using Notify for this, as the first 25000 sms are free to use, and the subsequent pricing is attractive. 
