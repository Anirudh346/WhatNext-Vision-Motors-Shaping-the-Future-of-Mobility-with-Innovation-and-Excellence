# WhatNext Vision Motors – Shaping the Future of Mobility with Innovation and Excellence

# 📌 Project Overview  
This Salesforce CRM solution powers WhatNext Vision Motors, a modern automotive company focused on revolutionizing the vehicle ordering experience. By automating stock validation, dealer assignment, and customer communication, the project boosts efficiency and customer satisfaction.

# 🧱 Custom Data Model  
The system is built on custom objects with meaningful relationships:  
- **Vehicle__c** – Stores vehicle details and available stock  
- **Vehicle_Dealer__c** – Lists authorized dealers and their locations  
- **Vehicle_Customer__c** – Contains customer information  
- **Vehicle_Order__c** – Tracks vehicle orders  
- **Vehicle_Test_Drive__c** – Schedules and monitors test drives  
- **Vehicle_Service_Request__c** – Maintains service and maintenance logs  

All objects are connected via **Lookup** or **Master-Detail** relationships.

# 🔁 Process Automation with Flows  
**AutoAssignDealer (Record-Triggered Flow)**  
- Triggers on new Vehicle Order creation  
- Identifies the nearest dealer using customer’s city  
- Automatically assigns dealer to the order  

**TestDriveReminder (Scheduled Flow)**  
- Runs one day before the test drive  
- Fetches the customer email  
- Sends an automated reminder  

# 👨‍💻 Apex Development  
**Triggers and Handlers**  
- **VehicleOrderTrigger** – Listens to insert/update events on Vehicle_Order__c  
- **VehicleOrderTriggerHandler** – Prevents order if stock is zero and updates stock when order is confirmed  

**Batch Apex**  
- **VehicleOrderBatch** – Confirms pending orders when stock is replenished  
- **VehicleOrderBatchScheduler** – Runs the batch daily to check stock and process pending orders  

# 🚀 Key Features  
- **Auto Dealer Assignment** – Automatically matches orders with the nearest dealer  
- **Stock Validation** – Prevents out-of-stock vehicle orders  
- **Batch Job Processing** – Handles pending orders as stock becomes available  
- **Email Reminders** – Notifies customers before test drives  

# 🧰 Tech Stack  
- Salesforce Lightning Experience  
- Apex Triggers & Classes  
- Batch Apex & Scheduled Apex  
- Record-Triggered and Scheduled Flows  
- Dynamic Lightning Pages  
- Change Sets for Deployment  
