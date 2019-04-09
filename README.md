# MyTVHwiki

## Hierarchy of reference numbers

### Property Reference number

They are made of the `scheme reference` and `unit reference`. For example: BARR and 001 or 002, making `BARR001`
This data sits in Universal Housing/Contact Manager, and is consumed by MyTVH.


### Block reference number ###

They are made of `scheme reference` and `block reference`. For example, BARR and OB1 or OB2, making `BARROB1`. 
BARROB1 might include all flats from 1-72, for example.
This data sits in Universal Housing/Contact Manager, but is not used in MyTVH.



### Sub-block reference number ###

They are made of `scheme reference`, `block reference` and `sub-block reference`. For example, BARR, OB1, and -1 or -2, making `BARROB1-1`.
BARROB1-1 might include all flats 1-6, while BARROB1-2 might have flats 7-12.

This data only exists in Keystone, an asset management system MTVH has. It is currently not used by MyTVH, but it is planned that we'll pull this data into MyTVH's database to target the right flats to send bulk-sms for emergency repairs.
