# Webex Connect Flow

The objective is to create a Webex Connect flow for a healthcare use case. We will do it in sections:

1. Introduction
2. Create a new blank flow
3. Flow trigger
4. Welcome message
5. Surgery Reminder
6. Video Meeting Scheduling
7. Create and share Instant Connect Meeting Links
8. Update CRM

## Introduction

This is the interaction flow:

* Customer triggers the conversation on WhatsApp
* Customer name is read from CRM
* Surgery date is generated
* Surgery reminder is sent
* Video Consultation is scheduled with an specialist
* Video with instructions is sent to the customer
* Webex Instant Connect meeting links are created, and shared with the customer and the expert just before the meeting begins
* CRM is updated, indicating that the customer requested the video escalation, and the specialist chosen
* Customer and expert join the meeting

## Create a new blank flow

1. Log in to your [Webex Connect](https://sandbox.us.webexconnect.io/) sandbox (or in your own production tenant), go to **Services**:

   <img src="images/services.png" width="400">

   and choose some of your existing services, or create a new one. Then click on **Flows**, **Create Flow**

2. Give the flow a name, e.g.: `My first flow`

   - For **Method** select: `New Flow` and `Start from Scratch`

   - For **Trigger Category** select: `WhatsApp`

3. The **Event** should be `Incoming Message`.

4. Under **Conditions**, choose `whatsapp.message`, `equalsignorecase` and enter the key word that will trigger the flow, in this case: `instantconnect`. Rename this node to something like `Start` and click on **Save**.

   ![Event](images/event.png)

   This will trigger the flow when the world `instantconnect`is sent to the system (no case sensitive).

## Flow trigger

Add a **WhatsApp** node to the canvas, and connect it to the **Configure WhatsApp Event** node (number 2). You should find the WhatsApp node in the Node Palette on the left of the screen:

   ![alt text](images/palette.png)

   You can connect nodes in Webex Connect by dragging and dropping the green button from the first node to the second node.

   ![Connecting nodes](images/connect-nodes.png)

   > **Note:** You can check the node number on the bottom-left corner of the node configuration screen, or by clicking the **Debug** button once you have a live version of the flow.
