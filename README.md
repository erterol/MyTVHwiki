# MyTVHwiki

## Key terminology ##

Metropolitan Thames Valley exists to provide people with homes. An individual `Property` or residence is a `Unit`. Units are grouped into `Blocks` (e.g. A, B, C etc...) and the blocks into `Schemes`, e.g. 'Harris Close'.

`Residents` are formed of two discrete groups: `Tenants`, who have qualified for low-cost social housing, and `Homeowners` who own all or part of their unit. Residents pay `Rent` to Metropolitan Thames Valley and homeowners pay a `Service Charge` and also rent if they are in a `Shared Ownership` agreement. `Keyworkers` are a particular class of tenant who qualify for social housing on account of their profession, e.g. nurses, teachers, etc.

Each unit is occupied by a `Household` which consists of residents whose connection to a property is codified in an `Agreement`. A resident may make `Payments` into `Accounts` which are linked to agreements. A payment may be made using the MyTVH system (via Stripe) in which case it's instantly reflected in the relevant `Account Balance`. 

Metropolitan Thames Valley `Agents` have backoffice access to the MyTVH system including the ability to `Masquerade` as a resident, in order to perform operations on their behalf. 

These operations are payments, repairs and enquiries.

To make an `Enquiry`: an enquiry is associated with a category such as 'Accounts', 'Tenant services' or 'Parking & garages' and is routed to its respective email `Tray` where an agent can take it on and respond.

## Payments ##

Residents can make online payments via MyTVH, processed via Stripe.

There are some other payment mechanisms which are used. There is a delay before transactions made in these other ways appear in account balances:

- Standing order

- Direct Debit: via the 'Allpay' service

- Paypoint card: via Allpay

- Phone: using Interactive Voice Recording (IVR) via Callpay (an Allpay company) or via a phone call to an agent who can take process the payment

In Sept 2019 EU payment regulations will change how MOTO (Mail Order Telephone Order) payments must be processed. At present it's not clear how well Stripe will support MOTO payments under the new regulations.



## Hierarchy of reference numbers

### Property Reference number

They are made of the `schemes` and `units`. For example: BARR and 001 or 002, making `BARR001`
This data sits in Universal Housing/Contact Manager, and is consumed by MyTVH.


### Block reference number ###

They are made of `scheme reference` and `block reference`. For example, BARR and OB1 or OB2, making `BARROB1`. 
BARROB1 might include all flats from 1-72, for example.
This data sits in Universal Housing/Contact Manager, but is not used in MyTVH.



### Sub-block reference number ###

They are made of `scheme reference`, `block reference` and `sub-block reference`. For example, BARR, OB1, and -1 or -2, making `BARROB1-1`.
BARROB1-1 might include all flats 1-6, while BARROB1-2 might have flats 7-12.

This data only exists in Keystone, an asset management system MTVH has. It is currently not used by MyTVH, but it is planned that we'll pull this data into MyTVH's database to target the right flats to send bulk-sms for emergency repairs.
