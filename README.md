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

<img width="1440" alt="Screenshot 2024-09-10 at 1 05 40 PM" src="https://github.com/user-attachments/assets/60c05d3d-756f-40a4-b0c5-76c71b5e7252">

Spidering: Use the Spider tool to discover all the pages and endpoints of your application.
<img width="1440" alt="Screenshot 2024-09-10 at 12 51 26 PM" src="https://github.com/user-attachments/assets/d17e1f98-5132-4096-b7c1-73ee7d6c244f">
Active Scan: Perform an active scan to detect potential vulnerabilities.

On click the attack starts , you can view details about the attack below



