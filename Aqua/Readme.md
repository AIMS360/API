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

1.  Obtain a valid access token by posting to
    <https://api.aims360.rest/authentication>

2.  Create a request for Data and obtain jobId and publishLink by posting to
    https://api.aims360.rest/reports /v1.0/reports/exportdata

3.  Check status of job send a get request to
    https://api.aims360.rest/jobsmanagement/ v1.0/backgroundjob?\$filter=jobId
    eq '{{BackgroundJobID}}'

4.  Get the results from the publishLink once job is completed
