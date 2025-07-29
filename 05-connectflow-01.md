# Webex Connect Flow

The objective is to create a Webex Connect flow for this healthcare use case. To save you time, part of the workflow has already been created in advance. We will see how to add the most relevant functionalities, and we will do it in sections:

1. Introduction


PENDING TO FINISH

2. Create a new blank flow
3. Flow trigger
4. Welcome message
5. Surgery Reminder
6. Video Meeting Scheduling
7. Create and share Instant Connect Meeting Links
8. Update CRM

## Introduction

This is the interaction flow:

* Customer name is read from CRM
* Surgery date is generated
* Surgery reminder is sent
* Video Consultation is scheduled with an specialist. This process is handled by a Webex AI Autonomous Agent
* Video with instructions is sent to the customer
* Webex Instant Connect meeting links are created, and shared with the customer and the expert just before the meeting begins
* CRM is updated, indicating that the customer requested the video escalation, and the specialist chosen (DO I KEEP THIS ??)
* Customer and expert join the meeting

## Get Customer Data from CRM

1. Log in Control Hub with your admin user, go to **Services**, **Contact Center**:

    <p align="center">
    <img src="images/cc-admin.png" alt="Contact Center Administration" width="150">
    </p>

    In the **Quick Links** section on the right, click on **Webex Connect** 


2. Go to Services

   <p align="center">
   <img src="images/services-new.png" alt="Webex Connect Services" width="450">
   </p>

Select the Services for you POD, and click on the Service named '_Healthcare Main Flow_'


Mission accomplished! Learn how to integrate Webex Connect with external databases

