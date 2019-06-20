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

3.  The endpoint returns the JobID, job status and Publishlink in the response.

4.  Check the status of the job by sending a request to

    POST jobsmanagement/ v1.0/backgroundjob?\$filter=jobId eq
    '{{BackgroundJobID}}'

The output will be available once the job status is received as Completed. For
more details about the Job status endpoint \*\*click here\*\*.

1.  Get the output/result using the Publishlink.
