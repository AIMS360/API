AIMS360 Jobs
------------

### Introduction

For an API request, if the time to prepare the response is more than few seconds
then the request will be handled by a Background job. The request will be placed
in the queue and a job will be created to serve the request. The JobID and
status will be returned as the response to the request.

The status of the job needs to be checked in the regular intervals and when the
job status is \&quot;Completed&quot; the results are ready to access.

To check the status of the Job, the below endpoint needs to be called by passing
the respective JobID

Get /jobsmanagement/odata/v1.0/backgroundjob?\$filter=jobId eq
\&\#39;cd89746d-78a6-4dc2-86b1-aaaf32c0ba36-20190116141747515&\#39;

Response Properties

\| ID \| \&quot;ID&quot;: 52714

Primary Key of the Job \|

\| --- \| --- \|

\| jobCategoryID \| \&quot;jobCategoryID&quot;: 1002

The ID of the category to which the job belongs \|

\| categoryName \| \&quot;categoryName&quot;: \&quot;Reports&quot;

The name of the category to which the job belongs \|

\| jobSubCategoryID \| \&quot;jobSubCategoryID&quot;: 1003

The ID of the sub-category to which the job belongs \|

\| subCategoryName \| \&quot;subCategoryName&quot;: \&quot;Production
Forecasting Report\&quot;

The name of the sub-category to which the job belongs \|

\| jobDescription \| \&quot;jobDescription&quot;: \&quot;Create Production
Forecasting Report\&quot;

Description of the job \|

\| clientRequestId \| \&quot;clientRequestId&quot;: null

The request ID of the client \|

\| jobStatus \| \&quot;jobStatus&quot;: \&quot;Completed&quot;

The status of the job. The possible values are Queued, Completed, Failed \|

\| jobStatusText \| \&quot;jobStatusText&quot;: \&quot;Production forecast
report completed.\&quot;

Description about the job status \|

\| publishLink \|
\&quot;publishLink&quot;:&quot;https://api.aims360.rest/reports/v1.0/publishlink/XXXXXXXXXXXXXXXXXXXXXXXX/XXXXXXXXXXXXXXXXXXXXXXXX&quot;
The link to access the output of the job \|

\| requestURL \| \&quot;requestURL&quot;:
\&quot;https://api.aims360.rest/documentmanagement/v1.0/aimsdocument/1b59c33b-589b-4356-b829-908614848403-20190607060901986&quot;
\|

\| publishLinkAccessScope \| \&quot;publishLinkAccessScope&quot;:
\&quot;Private&quot;

The scope to access the publishlink. Valid scopes are Public, Private and
PeopleInOrganization \|

\| percentCompleted \| \&quot;percentCompleted&quot;: 100

The percentage of job completion \|

\| jobID \| \&quot;jobID&quot;:
\&quot;d29fac30-650a-4ff2-b2b1-acab3c7472ea-20190607060819639&quot;

The unique ID of the job \|

\| responseType \| \&quot;responseType&quot;: \&quot;File Attachment\&quot;

The type of job response \|

\| response \| \&quot;response&quot;:
\&quot;[{\\&quot;documentName\\&quot;:\\&quot;Forecasting\\_20190607060922.xlsx\\&quot;,\\&quot;DownloadLink\\&quot;:\\&quot;https://api.aims360.rest/documentmanagement/v1.0/aimsdocument/d29fac30-650a-4ff2-b2b1-acab3c7472ea-20190607060819639/4wwrcVf6HjwefEBkCuKvCfsAZBMKALdKUDrT1a1ou7pT4sn84NONPQPx9StenougircnaZN5sxB7c0JMNRLqe67QhpWVLkUJQY3d20190607060857054\\&quot;,\\&quot;SizeInMB\\&quot;:0.0,\\&quot;Type\\&quot;:\\&quot;.xlsx\\&quot;,\\&quot;DocumentID\\&quot;:\\&quot;d29fac30-650a-4ff2-b2b1-acab3c7472ea-20190607060819639\\&quot;,\\&quot;ExpiryDate\\&quot;:\\&quot;2019-07-07T06:09:22.6593866Z\\&quot;,\\&quot;Version\\&quot;:\\&quot;1.0\\&quot;}]&quot;
\|

\| startDate \| \&quot;startDate&quot;: \&quot;2019-06-07T06:08:19.64Z&quot;

The date when the job started \|

\| completedDate \| \&quot;completedDate&quot;:
\&quot;2019-06-07T06:09:22.737Z&quot;

The date when the job is completed \|

\| purgeDateTime \| \&quot;purgeDateTime&quot;:
\&quot;2019-07-07T06:08:19.64Z&quot;

The date and time when to purge the job and associated request and response \|

\| clientID \| \&quot;clientID&quot;:
\&quot;44FDE9CF-230A-4516-A128-AE464776F1C5&quot;

The unique ID of the Client \|

\| DatabaseName \| \&quot;DatabaseName&quot;: \&quot;AZ0XXData1&quot;

The name of the client\&\#39;s database \|

\| accountCode \| \&quot;accountCode&quot;: \&quot;AZ022&quot;

The account code of the client \|

\| purgeDays \| \&quot;purgeDays&quot;: 30

The number of purge days \|

\| canReRun \| \&quot;canReRun&quot;: \&quot;Yes&quot;

Determines whether the job can be run again or not \|

\| maximumDateTimeToExecuteJob \| \&quot;maximumDateTimeToExecuteJob&quot;: null

If the job can be run again, the maximum date and time with in which the job can
be rerun \|

\| numberOfAttempts \| \&quot;numberOfAttempts&quot;: 0

The number of attempts taken to run the job \|

\| CanPublish \| \&quot;CanPublish&quot;: \&quot;Yes&quot;

Determines whether the job publishes any results or not \|

\| createdBy \| \&quot;createdBy&quot;: \&quot;support\@aims360.com&quot;

The email address of the operator who created the job \|

\| createdDate \| \&quot;createdDate&quot;: \&quot;2019-06-07T06:08:19.64Z&quot;

The date and time when the job is created \|

\| modifiedBy \| \&quot;modifiedBy&quot;: \&quot;support\@aims360.com&quot;

The email address of the operator who modified most recently \|

\| modifiedDate \| \&quot;modifiedDate&quot;:
\&quot;2019-06-07T06:09:22.737Z&quot;

The date and time when the job is modified \|

\| rowversion \| \&quot;rowversion&quot;: \&quot;AAAAAAAIJCU=&quot;

The version of the row \|

\*\*Rerun job\*\*

The job can be run again if the \&quot;canReRun&quot; property of the job is
Yes. To rerun the job, the below endpoint needs to be called by passing the
respective JobID

POST
jobsmanagement/v1.0/backgroundjob/d29fac30-650a-4ff2-b2b1-acab3c7472ea-20190607060819639/rerun

Response properties

\| jobId \| \&quot;jobId&quot;:
\&quot;XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX&quot;

The ID of the job created to serve the request \|

\| --- \| --- \|

\| jobStatus \| \&quot;jobStatus&quot;: \&quot;Queued&quot;

The status of the job \|

\| publishLink \|
\&quot;publishLink&quot;:&quot;https://api.aims360.rest/reports/v1.0/publishlink/XXXXXXXXXXXXXXXXXXXXXXXX/XXXXXXXXXXXXXXXXXXXXXXXX&quot;
The link to access the output of the job \|

\| publishLinkAccessScope \| \&quot;publishLinkAccessScope&quot;:
\&quot;Private&quot;

The scope to access the publishlink. Valid scopes are Public, Private and
PeopleInOrganization \|
