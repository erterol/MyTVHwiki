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
- agent sees a list of units returned
- agent composes the message
- agent sends the SMS

The filtering, adding/removing units is de-scoped at the moment. So is enriching the list of units data through more granular data from Keystone.

