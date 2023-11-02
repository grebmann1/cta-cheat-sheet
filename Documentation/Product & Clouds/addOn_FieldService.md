[Home](../../README.md)
# Salesforce Field Service
Running a field service business means managing numerous moving parts. With Field Service, you get the tools that you need to manage work orders, scheduling, and your mobile workforce.\
Here are some of the things you can do.

- Create records that represent your field service workers, dispatchers, and agents, and add details about their skills, location, and availability
- Set up multilevel service territories that represent the regions where mobile workers can provide services
- Track the location and status of your inventory, warehouses, service vehicles, and customer sites
- Schedule one-time or recurring work orders for customers, and add details about worker preferences, required skills, and parts
- Create maintenance plans and templates to standardize your field service tasks
- Generate service reports to keep customers informed about service progress

## Licenses
Salesforce Field Service user different `user licenses` for each persona.

#### Field Service Licenses
|Features | Dispatcher | Technician | Contractor | Contractor Plus
|--|--|--|--|--|
|Work Orders|✅|✅|✅|✅
|Appointment Booking|✅|✅|✅|✅
|Asset, Inventory, and Product Tracking|✅|✅|✅|✅
|Opportunities|✅|✅|❌|✅
|Android and iOS Mobile App|❌|✅|✅|✅
|Schedule Optimization|✅|❌|❌|✅
|Dispatcher Console|✅|❌|❌|✅

#### Field Service Plus
Get the field service bundle that `combines both Technician/Mobile Employee and Dispatcher along with all Service Cloud and Sales Cloud functionality`.



# Documentation

## Data Model

### Core
![Data Model Core](../../Images/CTA%20-%20Diagrams%20-%20FSL%20-%20Core.png)
[More Details](https://developer.salesforce.com/docs/atlas.en-us.field_service_dev.meta/field_service_dev/fsl_dev_soap_core.htm)
### Inventory Management
![Data Model Inventory Management](../../Images/CTA%20-%20Diagrams%20-%20FSL%20-%20Inventory%20Management.png)

[More Details](https://developer.salesforce.com/docs/atlas.en-us.field_service_dev.meta/field_service_dev/fsl_dev_soap_inventory.htm)

### Waranty Management
![Data Model Warranty Management](../../Images/CTA%20-%20Diagrams%20-%20FSL%20-%20Warranty%20Management.png)

[More Details](https://developer.salesforce.com/docs/atlas.en-us.field_service_dev.meta/field_service_dev/fsl_dev_soap_warranty.htm)

## Mobile App
Field service provide a mobile app available in the differents store. Mobile workers using the app can:
- work while Offline
- Scan Barcode
- Capture Signature
- View their appointment schedule
- Track updates with push notifications
- View Knowledge articles to complete tricky tasks
- Track van stock and inventory consumed to complete jobs