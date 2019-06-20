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

1.  Obtain a valid access token. **Click here** to know how to get access token

2.  Create a request for data by posting to POST reports/v1.0/exportdata
    endpoint.

<<<<<<< HEAD
3.  The endpoint returns the JobID, job status and Publishlink in the response.

4.  Check the status of the job by sending a request to

    POST jobsmanagement/ v1.0/backgroundjob?\$filter=jobId eq
    '{{BackgroundJobID}}'
=======
Endpoint input properties

\| exportType \| \*\*\&quot;\*\* exportType \*\*\&quot;\*\* :\&quot;View"

Defines what needs to be exported. Valid values for this property are

View: When AIMS360 View data needs to be exported

Rreport: When AIMS360 Report data needs to be exported \|

\| --- \| --- \|

\| exportDataSettings \| The details required to export required data. For
exporting AIMS360 View, the details of the View need to be specified and for
exporting AIMS360 Report data, the report criteria need to be specified \|

\| Source \| \&quot;Source": \&quot;Orders"

The source of the AIMS360 View. Click here for the list of Sources \|

\| viewName \| \&quot;viewName": \&quot;Open Orders\&quot;

The name of the AIMS360 View. This can be System View or the Custom View
available in the View dropdown on the AIMS360 application for different modules
\|

\| exportCriteriaVersion \| \&quot;exportCriteriaVersion": \&quot;v1.0"

The version of the generated report/view \|

\| outputFormat \| \&quot;outputFormat": \&quot;csv"

The preferred format of the output. The supported formats are Excel, PDF,
Formatted Excel and JSON \|

\| publishLinkAccessScope \| \&quot;publishLinkAccessScope": \&quot;Private"The
scope to access the publishlink. Valid scopes are Public, Private and
PeopleInOrganization \|

1.  The endpoint returns the JobID, job status and Publishlink in the response.

Response properties

\| jobId \| \&quot;jobId": \&quot;XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"

The ID of the job created to serve the request \|

\| --- \| --- \|

\| jobStatus \| \&quot;jobStatus": \&quot;Queued"

The status of the job \|

\| publishLink \|
\&quot;publishLink":"https://api.aims360.rest/reports/v1.0/publishlink/XXXXXXXXXXXXXXXXXXXXXXXX/XXXXXXXXXXXXXXXXXXXXXXXX"The
link to access the output of the job \|

\| publishLinkAccessScope \| \&quot;publishLinkAccessScope": \&quot;Private"

The scope to access the publishlink. Valid scopes are Public, Private and
PeopleInOrganization \|

1.  Check the status of the job by sending a request to

POST jobsmanagement/ v1.0/backgroundjob?\$filter=jobId eq
\&\#39;{{BackgroundJobID}}&\#39;
>>>>>>> 9a505ceafc7a02261be4e8cafae3feb309e11cbd

The output will be available once the job status is received as Completed. For
more details about the Job status endpoint \*\*click here\*\*.

1.  Get the output/result using the Publishlink.
