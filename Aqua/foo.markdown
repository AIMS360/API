AIMS360 Aqua API
----------------

### Introduction

Aqua is a data extraction API designed to simplify data extraction from
AIMS360. Aqua leverages the AIMS360 Grid views to allow for simple and
consistent access to AIMS360 data via API calls. Using Aqua API,
developers can extract data for additional processing and analysis.

![](media/image1.png){width="5.833333333333333in"
height="2.8406616360454944in"}

### Interaction with Aqua API

Aqua API is designed to process large number of records. Aqua API
consumer data request can be returns in JSON, Csv, or Excel. To achieve
this consumer of Aqua must complete the following steps:

![](media/image2.png){width="5.833333333333333in"
height="0.7889337270341207in"}

1.  Obtain a valid access token. **Click here** to know how to get
    access token

2.  Create a request for data by posting to POST reports/v1.0/exportdata
    endpoint.

Endpoint input properties
| 1 | 2 | 3 | 4 | 5 | 6 |
|---|---|---|---|---|---|
| A | B | C | D | E | F |

4.  Check the status of the job by sending a request to

POST jobsmanagement/ v1.0/backgroundjob?\$filter=jobId eq
\'{{BackgroundJobID}}\'

> The output will be available once the job status is received as
> Completed. For more details about the Job status endpoint **click
> here**.

5.  Get the output/result using the Publishlink.
