# project-2-gomycode
Deploying a Web Service to Render
This guide explains how to deploy a web service to Render using a GitHub repository.

Prerequisites
A GitHub account
A Render account
A web service project hosted on GitHub
Steps to Deploy
1. Sign Up / Log In to Render
Visit Render and sign up for an account if you haven't already. Log in to your account.
2. Create a New Web Service on Render
Once logged in, go to the Render dashboard.
Click on the "+ New" button and select "Web Service" from the dropdown menu.
![render image 1](https://github.com/user-attachments/assets/a76edc6c-68e7-4dd8-bb2e-b9ca4344547e)
3. Connect Your GitHub Repository
Render will prompt you to connect your GitHub account if you haven't already done so. Authorize Render to access your GitHub repositories.
Select the repository that contains your web service project.
<img width="1210" alt="Screenshot 2024-09-02 at 12 38 01 PM" src="https://github.com/user-attachments/assets/f3f70774-89f1-413b-9f95-35f93dccdb6f">
4. Configure the Service
Name: Enter a name for your service.
Region: Choose the region closest to your target audience.
Branch: Select the branch you want to deploy (e.g., main).
Build Command: Specify the command to build your application (e.g., npm install for Node.js projects).
Start Command: Specify the command to start your web service (e.g., npm start for Node.js projects).
Instance Type: Choose an instance type based on your application's needs.
5. Environment Variables
If your application requires environment variables, you can add them in the "Environment" section. For example:

PORT: The port on which your web service will run (Render sets this automatically, but you can override it if necessary).
6. Deploy
After configuring the above settings, click "Create Web Service" to deploy your application.

Render will start building and deploying your application. You can monitor the deployment process in the Render dashboard. Once the deployment is complete, your web service will be accessible via the URL provided by Render.

7. Monitoring and Updates
Logs: You can view logs for your service in the Render dashboard to monitor the application's status and debug issues.
Automatic Deploys: Render can automatically deploy updates when you push new changes to the connected GitHub branch.
Conclusion
You have successfully deployed your web service to Render using GitHub. For more detailed instructions and advanced configurations, refer to the Render documentation.
Carrying out a web app security test with ZAP
After deploying the web service, it's crucial to ensure it is secure and free from vulnerabilities
 The following steps outline how to use OWASP ZAP (Zed Attack Proxy) for security testing. We would be using ZAP website
Setting Up OWASP ZAP
Download and Install: Download OWASP ZAP and follow the installation instructions for your operating system.
Start OWASP ZAP: Launch the application and familiarize yourself with its interface.
Running a Security Scan
Target Application:
Set the target URL to your deployed web service's URL on Render. Enter the url to attack then click 
the attack button
![Uploading Screenshot 2024-09-02 at 2.41.33 PM.png…]()
Spidering: Use the Spider tool to discover all the pages and endpoints of your application.
<img width="966" alt="Screenshot 2024-09-02 at 2 59 16 PM" src="https://github.com/user-attachments/assets/06cc791e-7d69-4bfb-b1fa-7426bd69212e">
Active Scan: Perform an active scan to detect potential vulnerabilities.

On click the attack starts , you can view details about the attack below
<img width="970" alt="Screenshot 2024-09-02 at 4 18 44 PM" src="https://github.com/user-attachments/assets/0e77a0ce-85fb-4cf5-8796-ed0565df5345">
Understanding the ZAP Report
Here is a summary of a ZAP scan report:

Strength: The severity level of the test.
Progress: The progress of the test.
Elapsed: The time taken to complete the test.
Reqs: Number of requests made during the test.
Alerts: Number of alerts triggered.
Sample ZAP Report
here are the reports
<img width="979" alt="Screenshot 2024-09-03 at 8 18 44 AM" src="https://github.com/user-attachments/assets/39bd48b9-516a-4693-9a81-f17ffa941ce1">
<img width="991" alt="Screenshot 2024-09-03 at 8 19 45 AM" src="https://github.com/user-attachments/assets/c40edfde-8239-47a2-9d3f-e49746b23bed">
<img width="955" alt="Screenshot 2024-09-03 at 8 21 19 AM" src="https://github.com/user-attachments/assets/1969d87c-6765-45de-90b4-4c128ab11a05">
<img width="986" alt="Screenshot 2024-09-03 at 8 22 29 AM" src="https://github.com/user-attachments/assets/73ee4c0c-71d9-4b11-8e1e-7c3158bbaf7c">
<img width="988" alt="Screenshot 2024-09-03 at 8 23 47 AM" src="https://github.com/user-attachments/assets/5623fecb-6710-43f5-9651-9e283000e51c">
<img width="996" alt="Screenshot 2024-09-03 at 8 25 03 AM" src="https://github.com/user-attachments/assets/5cf567c3-4596-4cf2-ae12-6e3bbb76721e">
<img width="1088" alt="Screenshot 2024-09-03 at 9 12 55 AM" src="https://github.com/user-attachments/assets/8003713b-c1ef-466d-a533-c70bb4777203">
<img width="1056" alt="Screenshot 2024-09-03 at 9 13 43 AM" src="https://github.com/user-attachments/assets/5924fe79-a67f-4d53-a414-04bde0cff618">
<img width="1092" alt="Screenshot 2024-09-03 at 9 14 53 AM" src="https://github.com/user-attachments/assets/8ba87557-a036-4fc5-bf52-4438758f554b">
<img width="1088" alt="Screenshot 2024-09-03 at 9 19 01 AM" src="https://github.com/user-attachments/assets/21d01106-775d-41c6-b9c6-d5bd6f43b800">
<img width="1080" alt="Screenshot 2024-09-03 at 9 19 52 AM" src="https://github.com/user-attachments/assets/202a1865-232f-4ff2-9ddb-d4722d51525f">
<img width="1058" alt="Screenshot 2024-09-03 at 9 20 39 AM" src="https://github.com/user-attachments/assets/8db743e5-21f4-4ef1-b48b-7a61f58ed4aa">
<img width="1035" alt="Screenshot 2024-09-03 at 9 21 24 AM" src="https://github.com/user-attachments/assets/72f30710-b71c-4692-9b01-6ca11fdcebfe">
<img width="1059" alt="Screenshot 2024-09-03 at 9 22 15 AM" src="https://github.com/user-attachments/assets/9430f2b1-1a8b-464c-ae4f-099d6b9f72fa">
<img width="1014" alt="Screenshot 2024-09-03 at 9 24 14 AM" src="https://github.com/user-attachments/assets/8b92233e-9b55-4d56-9efa-e5f506b31583">
<img width="1014" alt="Screenshot 2024-09-03 at 9 24 14 AM" src="https://github.com/user-attachments/assets/8a5f81c8-ea28-429b-a54d-c91fe456db5e">
<img width="1008" alt="Screenshot 2024-09-03 at 9 25 02 AM" src="https://github.com/user-attachments/assets/0e139b27-8d22-42a9-83a1-2d9a94f56a36">
<img width="1008" alt="Screenshot 2024-09-03 at 9 25 02 AM" src="https://github.com/user-attachments/assets/0e139b27-8d22-42a9-83a1-2d9a94f56a36">
<img width="1077" alt="Screenshot 2024-09-03 at 9 27 56 AM" src="https://github.com/user-attachments/assets/68229715-d187-4091-952d-6f027adf7581">
<img width="1038" alt="Screenshot 2024-09-03 at 9 28 33 AM" src="https://github.com/user-attachments/assets/8a748207-4ca1-4197-b793-ac773ab3f831">
<img width="1038" alt="Screenshot 2024-09-03 at 9 28 33 AM" src="https://github.com/user-attachments/assets/b18ecd36-0ebe-4db2-bd06-1ff04c23252a">
<img width="1007" alt="Screenshot 2024-09-03 at 9 29 23 AM" src="https://github.com/user-attachments/assets/24e35c97-9148-46fb-8ba2-6aaffcbc43e8">
<img width="1012" alt="Screenshot 2024-09-03 at 9 31 47 AM" src="https://github.com/user-attachments/assets/49bb6251-bcaa-4176-a9b0-d6e0e81c9686">
<img width="949" alt="Screenshot 2024-09-03 at 9 32 32 AM" src="https://github.com/user-attachments/assets/cd4905bb-0456-4598-a249-e218afbb560c">
<img width="1045" alt="Screenshot 2024-09-03 at 9 33 18 AM" src="https://github.com/user-attachments/assets/4a892039-12de-4d06-8ffc-d6d558938f62">
<img width="1440" alt="Screenshot 2024-09-03 at 9 34 43 AM" src="https://github.com/user-attachments/assets/e2df180d-76c9-455e-82e0-96d50ea4aeef">
<img width="1018" alt="Screenshot 2024-09-03 at 9 34 55 AM" src="https://github.com/user-attachments/assets/c2122a08-a69e-4e12-9ef4-200b696666d6">
<img width="1033" alt="Screenshot 2024-09-03 at 9 38 05 AM" src="https://github.com/user-attachments/assets/11bf96b3-4cf2-4633-8514-799ecb32c422">
<img width="1015" alt="Screenshot 2024-09-03 at 9 39 02 AM" src="https://github.com/user-attachments/assets/bdcb37c2-6c15-4724-8ce7-bbea0efb70f3">
