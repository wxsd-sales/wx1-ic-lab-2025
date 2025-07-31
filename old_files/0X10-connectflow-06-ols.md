# Update CRM

According to the [mockAPI.io API documentation](https://github.com/mockapi-io/docs/wiki/Quick-start-guide), the way to update a record is:

![mockAPI Update Record](images/mockio_update_record.png)

We need to know the `{userId}` for the record we want to update. We got this value in the response of the http request we did in the **Webex Connect Flow: Reminder** section, let's see how we can use this value at ay time in the flow:

1. Get the 'mockAPI' **Data Parser** node number, there are several ways of doing this:

    - Clicking on **NOTES** icon
    
    ![Notes Icon](images/notes-icon.png)

    - You can also double-click on the node, you will see the node number at the bottom left
    
    ![Node Number](images/node-number.png)

    In this example, 'mockAPI' **Data Parser** node number is 5 (n5).

2. Add a new **HTTP Request** node, add it to the canvas, and connect it to the previous **HTTP Request** node.

- Choose `PUT` as the **Method**
- Go to **Endpoint URl**, select `mockAPIEndpoint`under **Custom Variables** in **Input Variables** section
- In the same **Input Variables** section, type '/', go to the `mockAPI`**Data Parser** node (node 5 in this example), and select `id`:

![DB record Id](images/customerId.png)

- Add `Content-Type`as **Header**, with **Value** `application/json`
- And configure the Body =

        {
            "videoCallScheduled": true,
            "specialist": "$(specialist)"
        }

- Rename the node to 'Update CRM', and **Save** it

Now we are ready to test our flow !








