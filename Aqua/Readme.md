AIMS360 Aqua API
----------------

### Introduction

Aqua is a data extraction API designed to simplify data extraction from AIMS360.
Aqua leverages the AIMS360 Grid views to allow for simple and consistent access
to AIMS360 data via API calls. Using Aqua API, developers can extract data for
additional processing and analysis.

![](media/20d78213d0af9ca6f565d23a3494d39d.png)

### Interaction with Aqua API

Aqua API is designed to process large number of records. Aqua API consumer data
request can be returns in JSON, Csv, or Excel. To achieve this consumer of Aqua
must complete the following steps:

![](media/f104067fe9e7d2e5db9593a201c0528c.png)

1.  Obtain a valid access token. [Click here](https://github.com/AIMS360/API/blob/master/README.md) to know how to generate access token

2.  Create a request for data by posting to `POST reports/v1.0/exportdata`
    API.

Endpoint input properties

| Field Name             | Field Description                                                                                                                                                                                       |
|:------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| exportType             | `"exportType":"View"` <br>Defines what needs to be exported. Valid values for this property are <br>View: When AIMS360 View data needs to be exported <br>Report: When AIMS360 Report data needs to be exported       |
| exportDataSettings     | The details required to export data. <br> For exporting AIMS360 View, the details of the View need to be specified <br> `"exportDataSettings": {` <br> `"source":"Orders",` <br>`"viewName": "Open Orders"` <br>`}` <br> **source:** The source of the AIMS360 View. <br> **viewName:** The name of the AIMS360 View. This can be a System View or a Custom View available in the View dropdown on the AIMS360 application for different modules       <br>Click here for the list of Views                             |
| outputFormat           | `"outputFormat": "csv"` <br>The preferred format of the output. <br>The supported formats for Views are JSON, CSV and Excel <br> The supported formats for Reports are JSON, CSV, Excel and PDF  (based on the report the supported formats varies)                                                                             |
| publishLinkAccessScope | `"publishLinkAccessScope": "Private"` <br>The scope to access the publishlink. Valid scopes are Public, Private and PeopleInOrganization                                                                      |

3.  The API returns the JobID, job status, publishlink and publishlink access scope in the response.

Response properties

| Field Name             	| Field Description                                                                                                                                            	|
|:------------------------	|:--------------------------------------------------------------------------------------------------------------------------------------------------------------	|
| jobId                  	| `"jobId": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"` <br>The ID of the job created to serve the request                                                               	|
| jobStatus              	| `"jobStatus": "Queued"` <br>The status of the job                                                                                                                  	|
| publishLink            	| `"publishLink":"https://api.aims360.rest/reports/v1.0/publishlink/XXXXXXXXXXXXXXXXXXXXXXXX/XXXXXXXXXXXXXXXXXXXXXXXX"` <br>The link to access the output of the job 	|
| publishLinkAccessScope 	| `"publishLinkAccessScope": "Private"` <br> The scope to access the publishlink. Valid scopes are Public, Private and PeopleInOrganization                          	|

4.  Check the status of the job by sending a request to

`POST jobsmanagement/v1.0/backgroundjob?\$filter=jobId eq'{{BackgroundJobID}}'`

  For more details about the Job status API [click here](https://github.com/AIMS360/API/tree/master/Jobs).

Once the job status is received as Completed, the output can be obtained using publishlink.

5.  Get the output/result using the Publishlink. 

<br>

