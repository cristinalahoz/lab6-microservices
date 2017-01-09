# Web Engineering 2016-2017

1. The two microservices are running and registered

   Accounts Service
   ![Accounts_Service_LOG] (images/image1.png)
   ![Acoounts_Service_WEB] (images/image2.png)

   Web Service

   ![Web_Service_LOG] (images/image3.png)
   ![Web_Service_WEB] (images/image4.png)

2. The service registration service has the two microservices registered

   ![Registration_Service_WEB] (images/image5.png)
   ![Registration_Service_WEB2] (images/image5.1.png)

3. A second account microservice is running in the port 4444 and it is registered

   Accounts Service number 2

   ![Accounts_Service_2_LOG] (images/image6.png)
   ![Accounts_Service_2_WEB] (images/image7.png)

   Account Service number 2 registration

   ![Accounts_Service_2_Registration_WEB] (images/image8.png)
   ![Accounts_Service_2_Registration_WEB2] (images/image8.1.png)

4. A brief report describing what happens when you kill the microservice with port 2222.
Can the web service provide information about the accounts? Why?

When you killed the Account server in port 2222 it become unavailable.
The web service tries o connect it, but after a couple of tries the web service search
for a new microservice registered with the name AccountsService. After the service find
the new microservice registered at port 4444, connect it and works correctly again.
