This topic contains the reference information that you need to know when working in the **Users Control > Roles** section.
***
## Roles Page
On the **Roles** page, you see the creation date, role name, and the actions that you can perform.
***
## Create and Edit Role Page

The following table describes the attributes that are used when creating or updating a role.

| Attribute | Description|
| --- | --- |
| **Name** |A unique name for the role, e.g. _Category Manager Role_. |
|**Bundle**  | Bundle, in other words, is a module. It is used to identify what module a specific user can or cannot manage. |
|**Controller**  | This identifies the controller responsible for the bundle. |
| **Action** | This identifies what action can be performed for a specific module.  |
| **Permission** | Can be either allow or deny. |
@(Warning)(Note)(The bundle, controller, and action values are provided by developers from your team, as they have access to the source code.)
***
**Example**
Imagine you need to deny adding new carrier companies to the Shipment section. You will put the following:
**Bundle**: _shipment_
**Controller**: _carrier_
**Action**: _add_
**Permission**: _deny_

When the user with this role clicks **Add new Carrier Company**, they will get the **Access denied** view.
![Access Denied view](https://cdn.document360.io/9fafa0d5-d76f-40c5-8b02-ab9515d3e879/Images/Documentation/Access%20Denied%20view.gif){height="40" width="40"}
