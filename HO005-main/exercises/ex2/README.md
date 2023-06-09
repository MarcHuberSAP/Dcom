# Exercise 2 - Create a Business Partner Details Page

After you have created the entry page of your application, you will now create a page to show the details of the selected business partner.

### Create a New Page

You will add a new page to your application and add page parameters so you can access data from your application.

1. On the top left section, choose the name of your current page **Home**, which is highlighted in light blue, to open the **PAGES** menu.

2. Choose **ADD NEW PAGE** and then Select **OK**.

   <img src="./assets/ba_createPage.png">

3. Choose **Details** as **Page name**. A new page will be created and opened.

4. On the Details page, choose the toggle button to switch to **VARIABLES** tab.

5. Choose the **PAGE PARAMETERS** button on the left side of the screen.

6. Choose **ADD PARAMETER**.

7. It creates a new parameter as a list entry, choose entry to edit.

8. On the right side of the screen, change the **Parameter name** to **businessPartnerId**.

9. Again, choose  **ADD PARAMETER** and select the new entry.

10. Change **Parameter name** to **businesspartnerName**.

11. Choose **Save**.

    <img src="./assets/ba_pageparameters1.png">

12. Switch back to **View** via the toggle button.

### Enable Navigation from Home Page to Details Page

To show the business partner details on the details page, you need to connect the **Home** page and the **Details** page. In this section, you will first create a new navigation logic to pass the page parameter created in the previous step.
On the details page, you will then load the business partner address by passing the business partner id to the **A_BusinessPartnerAddress** entity.

1. On the top left section, choose the name of your current page **Details**, which is highlighted in light blue, to open the **PAGES** menu. 
2. Select **Home** to open the home page.
3. Select the first row in the list.

4. At the bottom of App Builder where you can see **Add logic to LIST ITEM1**. Choose the arrow to open the logic canvas.

   <img src="./assets/ba_enableNavigation.png" height="400px">

5. In the component menu on the left side, choose **NAVIGATION** &rarr; **Open page** to add a function that opens a new page.

6. Drag and drop it to the Logic canvas.

7. Hover over the **Component tap** and choose the round dot. Connect the dots of the **Component tap** and the **Open page** component. It creates a new connection and sets the logic to open a new page on the event of tapping an item in the list item.

   <img src="./assets/logiccanvas2.png">

8. Choose the open page component.

9. On the right side of the screen, select **PROPERTIES** &rarr; **Parameters** &rarr; **businessPartnerId**.

10. Choose the **X** button. It opens a popup.

11. Select **Data item in repeat**.

12. Select **current**.

13. Scroll the list and select **BusinessPartner** and choose **SAVE**.

    <img src="./assets/ba_pageVariable.png">

14. Repeat the steps 9-12 to the **businesspartnerName** parameter and select **current.BusinessPartnerFullName**, scroll and choose **SAVE**.
15. Choose **SAVE** to save the changes.
16. With this step now, you can open the details page you created to show the business partner address by passing the business partner id to the A_BusinessPartnerAddress entity.


### Load Business Partner Address on the Details Page

The detail page receives the Business partner ID from the main page. In this step, the ID is used to get the address of the selected business partner.

1. From the left side of the screen, choose **Home**.

2. Select the **Details** page to switch to the details page.

3. Toggle to the **VARIABLES** tab.

4. Select **DATA VARIABLES** on the left.

5. Choose **ADD DATA VARIABLE**.

6. Select **A_BusinessPartnerAddress** from the list.
   <img src="./assets/ba_detailspage2.png">

7. Choose the **Filter Conditions** button on the right.    

8. A popup opens. Select **Object with properties** and choose **ADD CONDITION**.

   <img src="./assets/objectwithproperties.png">

9. In the **Property** dropdown, select **Business Partner**.

10. Under **Compared Value**, choose button **ABC**.

   <img src="./assets/propertybinding.png">

11. Select **Data and Variables**.

    <img src="./assets/bindingdatavariables.png">

12. Select **Page Parameter**.

    <img src="./assets/bindingpageparameter.png">

13. Select **businesspartnerid** and choose **Save**.

    <img src="./assets/bpid.png">

14. Choose the **SAVE** button to save changes to the page.

15. Toggle to the **VIEW** mode now.

Now, your application loads the business partner's address and stores it to the data variable.


### Display the Business Partner Name on the Details Page

Next, you will change the header of the details page, so it displays the current Business Partner.

1. Select the default description on the page and delete it by pressing **X**.

   <img src="./assets/ba_datailspage3.png">

2. Select headline component. On the right side of the screen, choose **ABC** button in **Content** section.

   <img src="./assets/ba_detailspage4.png">

3. Select **Data and Variables**

   <img src="./assets/bindingdatavariables.png">

4. Select **PageParameter**.

   <img src="./assets/bindingpageparameter.png">

5. Select **businessPartnerName** and choose **Save**.

<img src="./assets/editbinding.png">



### Display Business Partner Addresses on the Details Page

Next, you will add a list element, which displays the address of the business partner.

1. Drag the **List item** from the **CORE** tab on the left.

   <img src="./assets/ba_detailspage5.png">

2. From the right **PROPERTIES** panel, find **Arrow Visible** section and select **false** from the dropdown.

3. Choose the **Repeat with** button on the left side of the screen.

   <img src="./assets/ba_detailspage6.png">

1. In the popup, select **Data and Variables** &rarr; **Data Variable**.

    <img src="./assets/objectdata.png">

5. Select **A_BusinessPartnerAddress1** from the list.

6. Choose **SAVE**.

   <img src="./assets/bpaddress.png" height="400px">

7. On the right side of the screen, choose **ABC** button under **Primary Label**.

8. Select **Data item in repeat**.

9.  Choose **current**.

10. Scroll and select **StreetName**. Choose **SAVE**.

    <img src="./assets/streetname.png" height="400px">

11. On the right side of the screen, Choose **ABC** button under the **Secondary Label**.

12. Select **Data item in repeat**.

    <img src="./assets/secondarylabel.png">

13. Choose **current**.

14. Scroll and select **PostalCode**. Choose **SAVE**.

     <img src="./assets/postalcode.png">

     <img src="./assets/primarylabel.png" height="400px">

15. Choose **SAVE** at the top of page.

Now, that your app is developed, Let's preview the application.

### Preview Your Application

1. Choose **LAUNCH**.

2. Choose **OPEN PREVIEW PORTAL** and choose **Open web preview** button in **Preview on Web**.
   
   <img src="./assets/ba_preview1.png">

3. Select your application and choose **OPEN**.

   <img src="./assets/ba_preview2.png">

4. Choose the list item to see the details page.

5. The main page should look like:

   ![main page](../ex0/assets/images/preview1.png)

6. The details page should look like:

   <img src="./assets/ba_deatilspagePreview.png">



