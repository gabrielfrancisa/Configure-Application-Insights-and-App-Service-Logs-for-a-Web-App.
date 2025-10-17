# Configure-Application-Insights-and-App-Service-Logs-for-a-Web-App.
As an Administrator for an organization that needs to manage its Azure® web apps.

## create and deploy an Azure Web App that includes Application Insights and App Service logs. 
1. First, create a Web App, and then you will deploy the source code for the Web App. 
2. Next, we will enable Application Insights for monitoring.
3. Finally, you will enable App Service logs for auditing and debugging.


## 1. Create an Azure Web App
>> Sign in to the Azure portal as Pat-55553826@cloudslice.onmicrosoft.com 

>> Create an Azure Web App by using the values in the following table. For any property that is not specified, use the default value.

Property ----------	Value
1. Resource Group	corp-datalod55553826
2. Name	wa55553826
3. Secure unique default hostname	Off
4. Publish	Code
5. Runtime stack	ASP.NET V4.8
6. Region	East US
7. Windows Plan (East US)	Create new: AppPlan1
8. Pricing plan	Basic B1
9. Continuous deployment	Disable
10. Basic authentication	Enable
11. Enable virtual network injection	Off
12. Enable Application Insights	No

>> You use an Azure App Service Web App to host your website in the cloud in a fully managed environment.

>> An App Service plan defines the capacity and scalability of the web servers that support your website.

>>Review the documentation on:
1. Azure App Service
2. App Service plan
3. Open a new browser window on your local machine, and then go to the URL for the new Web App https://wa55553826.azurewebsites.net to verify that it is up and running.
4. You should see a default home page.
5. The Web App default home page


## 2. Deploy application code
>> Deploy the source code for the wa55553826 Web App by using the values in the following table. For any property that is not specified, use the default value.

Property ---------	Value
1. Source	External Git
2. Repository	https://github.com/LODSContent/LODSOC_app-service-web-dotnet-get-started
3. Branch	main
4. Repository Type	Public

>> You may have to wait 1-2 minutes for the new code to fully deploy.

>> In a new browser tab, go to the URL for the new Web App at https://wa55553826.azurewebsites.net to verify that it is up and running.

>> You should see an updated home page.

>> The updated home page

>> If you do not see the updated page, refresh the browser.

>> When you plan your deployment, make sure that you review the Azure App Service deployment best practices as part of your planning process.


## 3. Enable Application Insights
>> Enable Application Insights for the wa55553826 Web App by using the new resource name wa55553826 and the laws-55553826 Log Analytics Workspace.

>> You may have to wait 1-2 minutes for Application Insights to be fully enabled.

>> The Application Insights resource is created when you enable Application Insights and has the same name as the Web App/App Service but is a separate resource in the resource group.

>> Application Insights resource

>> Azure Application Insights provides a set of reports and charts that you can use to monitor the key metrics and performance of your cloud apps.

## Review the documentation on Azure Application Insights.
1. Open the Live metrics report on the Application Dashboard.
2. Expand this hint for guidance on opening the Live metrics report.
3. Keep the Live metrics report open to wait for future requests.

>> In a new browser window, go to the URL for the Web App at https://wa55553826.azurewebsites.net, and then refresh the browser a few times to generate valid requests.

>> Generate a failed request for the Web App by using the URL https://wa55553826.azurewebsites.net/default.

>> Return to the Live metrics report to view the successful and failed requests.

>> You should see the successful and failed requests from the last 60 seconds.

>> The Live metrics report

>> Close the Live metrics report page.

>> On the Application Dashboard, open the Failure report, and then display the data from the Last 30 minutes.

>> If you do not see the failed request, select Refresh. It may take 1-2 minutes for the latest failure to appear in the report.


## 4. Enable App Service logs
>> Enable App Service logs for the wa55553826 Web App by using the values in the following table. For any property that is not specified, use the default value.

Property------------Value
1. Application Logging (Filesystem)	On
2. Level	Error
3. Web server logging	File System
4. Quota (MB)	35
5. Retention Period (Days)	90
6. You can use Azure App Service logs to capture log messages that can help you to audit and debug your cloud apps.

## Review the documentation on Azure App Service logs.
1. Open the Log stream for the wa55553826 Web App.
2. If the Log stream option does not appear, then refresh the browser by using Ctrl+R.
3. Keep the Log stream page open to wait for future requests.
4. In a new browser window, go to the URL for the Web App at https://wa55553826.azurewebsites.net to generate a valid request.
5. Generate a failed request for the Web App by using the URL https://wa55553826.azurewebsites.net/default.
6. Return to the Log stream page, and then review the successful and failed requests.
7. You should see the requests appear in the Log stream within 1-2 minutes.
8. The successful request should display a return code of 200 and the failed request should display a return code of 404.

## The Log stream page
1. You may also see an AlwaysOn request appear in the Log stream. This is generated automatically every five minutes to prevent the Web App from entering idle mode.



5. Summary
Congratulations,

## You have accomplished the following:
1. Created an Azure Web App.
2. Deployed application code.
3. Enabled Application Insights.
4. Enabled App Service logs.
