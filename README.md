# WhatNext-Vision-Motors-Shaping-the-Future-of-Mobility-with-Innovation-and-Excellence
This repository showcases the Salesforce CRM implementation for WhatNext Vision Motors, a cutting-edge automotive company reimagining the way vehicles are ordered, test-driven, and delivered. By leveraging automation, Apex development, and dynamic Salesforce features, the project elevates customer engagement and operational efficiency.

#🧱 Custom Data Model & Object Relationships
At the core of the solution lies a set of custom objects, tailored to capture and manage key business processes:

Vehicle__c – Details of available vehicles, including real-time stock levels

Vehicle_Dealer__c – Authorized dealerships with location mapping

Vehicle_Customer__c – Stores customer profiles

Vehicle_Order__c – Records of customer orders

Vehicle_Test_Drive__c – Test drive scheduling and tracking

Vehicle_Service_Request__c – Tracks service history and maintenance

All objects are interconnected through Lookup and Master-Detail relationships for data integrity and reporting.

🔁 Business Automation with Flows
Automation plays a pivotal role in optimizing user experience and process consistency:

AutoAssignDealer (Record-Triggered Flow)

Activated on new Vehicle_Order__c creation

Identifies nearest dealer by matching the customer’s city

Automatically assigns dealer to the order

TestDriveReminder (Scheduled Flow)

Runs one day before the scheduled test drive

Retrieves customer email and sends a reminder

👨‍💻 Apex Development
Custom Apex code is used to manage stock availability, trigger logic, and background processing:

Apex Triggers & Handler
VehicleOrderTrigger – Trigger on Vehicle_Order__c (before/after insert and update)

VehicleOrderTriggerHandler – Prevents placing orders with zero stock and updates stock upon order confirmation

Batch & Scheduled Apex
VehicleOrderBatch – Batch class that confirms pending orders once stock is replenished

VehicleOrderBatchScheduler – Scheduled Apex that executes the batch job daily to check for stock updates and process pending orders

🚀 Project Features
This Salesforce solution transforms traditional dealership management with a blend of automation and intelligence:

Dealer Auto-Assignment – Automatically maps orders to the nearest authorized dealer

Stock Validation – Prevents order creation if vehicle stock is zero (via Apex validation)

Automated Order Processing – Batch jobs regularly scan for pending orders and confirm them if stock is available

Test Drive Notifications – Sends automated reminders to customers a day prior to scheduled test drives

🧰 Tech Stack
Salesforce Lightning Experience

Apex Triggers & Classes

Batch & Scheduled Apex Jobs

Record-Triggered & Scheduled Flows

Dynamic Lightning Pages & Forms

Change Sets for Deployment

📌 Summary
This project modernizes the end-to-end vehicle ordering and customer interaction process for WhatNext Vision Motors. With intelligent automation, real-time stock tracking, and proactive customer engagement, the company is set to deliver a superior experience and streamline dealership operations through Salesforce CRM.

