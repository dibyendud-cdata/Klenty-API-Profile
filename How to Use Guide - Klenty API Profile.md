# How To Use Guide (API Profile)

In this document we will demonstrate how to use **Klenty’s API Profile** in **Power BI Desktop**. The primary advantage of an API Profile (.apip file) is to retrieve data from the respective application without logging into it for the purpose of viewing or analysis of the required data. This document will take you through the steps of how to connect an API Profile (.apip) file to our API Driver (Power BI) and use that connection to visualize and analyze data in Power BI Desktop application

## **Pre-Requisites:**

1. Download the API Profile (.apip) file of the required application from the given [link](https://www.cdata.com/apidriver/download/) (We have used Klenty’s API Profile **.apip** file here). Save the file in any folder of your local system (E.g.: **C:\Program Files\CData\CData Power BI Connector for API\db\Klenty.apip** – for demonstration purposes)

2. Scroll down the page for the same link given above. Download and Install **API Driver for Power BI** from the Section **Download API Drivers**

![](https://github.com/dibyendud-cdata/Klenty-API-Profile/blob/main/How%20to%20Use%20Guide%20Images/1.%20API%20Driver%20for%20Power%20BI.PNG)

3. Follow the path -- C: Drive > Program Files > CData > CData Power BI Connector for API > Configure ODBC (This path may change based on where you have installed the API Driver) and open the **ConfigureODBC** application

4. Configure the ODBC Connection as given:

	a.  Enter **Profile** as: **C:\Program Files\CData\CData Power BI Connector for API\db\Klenty.apip** (as mentioned earlier, this path may change on the basis of where you have saved the API Profile file)
	
	b.  Enter **Profile Settings** as: **ApiKey=64010f37956ca624508e6fa1;User=davidl@cdata.com;Other=SupportEnhancedSQL=true;AuthScheme=None;SSLServerCert=\*;ProxyServer=localhost;ProxyPort=8888**
	
	c.  Set Auth Scheme as **None**
	
	d.  Click on **Test Connection** (For successful connection, a pop-up saying **The connection test was successful** will be displayed on your screen)
	
	e.  Click on **OK** post successful connection

![](https://github.com/dibyendud-cdata/Klenty-API-Profile/blob/main/How%20to%20Use%20Guide%20Images/2.%20ODBC%20Power%20BI%20API.PNG)

## **Using the API Profile in Power BI:**

1. Open Power BI Desktop application

2. Click on: Get Data > More… > CData API > Connect

![](https://github.com/dibyendud-cdata/Klenty-API-Profile/blob/main/How%20to%20Use%20Guide%20Images/3.%20Power%20BI%20-%20Get%20Data.PNG)

<br>

![](https://github.com/dibyendud-cdata/Klenty-API-Profile/blob/main/How%20to%20Use%20Guide%20Images/4.%20Power%20BI%20-%20Get%20Data%202.PNG)

3. Enter Data Source Name in **CData Power BI Connector for API** exactly as mentioned in the example. In this case – **CData Power BI API**

4. Enter the required SQL Query as given in **SQL Queries - Klenty** markdown file based on the view to be retrieved

5. Select **Import** in Data Connectivity mode and click on **OK**

![](https://github.com/dibyendud-cdata/Klenty-API-Profile/blob/main/How%20to%20Use%20Guide%20Images/5.%20CData%20Power%20BI%20Connector%20for%20API.PNG)

6. The application data can now be viewed in a box (based on the Data Source Name entered in **Step 3**)

![](https://github.com/dibyendud-cdata/Klenty-API-Profile/blob/main/How%20to%20Use%20Guide%20Images/6.%20CData%20Power%20BI%20API%20Data.PNG)

7. The data will now be loaded under the **Data** bar on the right (Query1 - in this case) as shown here. Select the columns as per the order you want them to be displayed in the table

8. Click on **Filter**

![](https://github.com/dibyendud-cdata/Klenty-API-Profile/blob/main/How%20to%20Use%20Guide%20Images/7.%20Power%20BI%20Dashboard.PNG)

9. As shown in the image given below, select **Basic or Advanced** filter type and select the checkboxes you would like your data to be filtered and displayed (as shown in the table)

![](https://github.com/dibyendud-cdata/Klenty-API-Profile/blob/main/How%20to%20Use%20Guide%20Images/8.%20Power%20BI%20Dashboard%202.PNG)

## **Additional Information on SQL Queries to be used:**

Some SQL Queries (mostly for Prospect and Prospect Status) given in the **SQL Queries – Klenty** file needs to be used as per requirement of the user.

Few examples are given below for clarity:

1. **Prospect Details by Email:** 

**SQL Query:**  Select \* from ProspectDetailsByEmail where Email = '**(input)**'

Here, (input) should contain the “email id” by which the prospect details need to be displayed. This will change as per the user’s requirements. Please do not forget to add the single quotes

2. **Prospects by Prospect Creation Date:**

**SQL Query:**  Select \* from ProspectByCreationDate where startDate='**(input)**' AND endDate = '**(input)**’

Here, (input) should contain the “prospect creation dates (start-date and end-date)” by which the prospect details need to be displayed.

3. **Get Prospects by Lists:**

**SQL Query:** Select \* from ProspectByList where List = '**(input)**'

Here, (input) should contain the “list name” by which the prospect details need to be displayed.

**Note:** Prospects by Lists (dynamic) query will display all the lists with any specific input   

<br>

**P.S:** For any query/additional support related to this document, kindly contact **dibyendud@cdata.com**

**--------------------------------------------------xxxxxxxxxxxxxxxxx-----------------------------------------------**
