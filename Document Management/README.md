Document Management
-----------

### Introduction

The documents created by AIMS360 APIs and the documents uploaded from the Attachment tab available on different modules of AIMS360 ERP application will be managed by AIMS360 Document Management service. 

### What you can do with the Document Management?

Using the Document Management service you will be allowed to preform the following

* `GET/documentmanagement/odata/v1.0/aimsdocument`<br>  Retrive the list of documents 

* `GET/documentmanagement/v1.0/aimsdocument/{AimsDocument GUID}` <br> Download a specific document

#### Document properties


| Field Name             	| Field Description                                                                                                                                            	|
|:------------------------	|:--------------------------------------------------------------------------------------------------------------------------------------------------------------	|
| documentGUID                     |  `"documentGUID": "9248b03b-b306-4fe8-a2b2-4e3189a57973-20190322065815704"` <br>The unique GUID of the document                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| accessScope                | `"accessScope": "PUBLIC"` <br>The access scope of the document. Valid access scopes are Public, Private and People In Organization        <br>For more details on Access scopes, [click here.](https://github.com/AIMS360/API/tree/master/Document%20Management/Document%20Access%20Scopes)                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| documentName           | `"documentName": "Forecasting_20190322065521.json"` <br>The name of the document                                                                                                                                                                                                                                                                                                                                                                                             |
| fileType             | `"fileType": "Json"` <br>The file format  of the document. Supports all file formats except .exe, .vb, .cs, .msi and .msu formats.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| category                 | ` "category": "backgrounJob"` <br>The category of the document. For the list of valid Categories, [click here.](https://github.com/AIMS360/API/tree/master/Document%20Management/Document%20Categories)                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| aimsReference                |   ` "aimsReference": "5190h4"` <br>The AIMS360 reference of the document                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| user                | `"User": "test@aims360.com"` <br>The email address of the user who created the document                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| title            | ` "title": "Forecasting_20190322065521.json"` <br>The title of the document                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| description                 |  `"description": "Forecasting_20190322065521.json"` <br>The description about the document                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| downloadUri            |  `"downloadUri": "https://apieast.aims360.rest/documentmanagement/v1.0/aimsdocument/9248b03b-b306-4fe8-a2b2-4e3189a57973-20190322065815704"` <br>The URI to download the document                                                                                                                                                                                                                                                                                                                                                                                                      |
| fileSize                |  ` "fileSize": 77328` <br>The size of the document in Bytes                                                                                                                                                                                                                                                                                                         |
| fileSizeInMB                |  `  "fileSizeInMB": 0.07374573` <br>The size of the document in  Mega Bytes                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| lastUploaded               |  `"lastUploaded": "2019-03-22T06:58:15.893Z"` <br>The date and time of the recent document upload                                                                                                                                                                                                                                                                                                                                                                                                                                            |

<br>


### Endpoints

**Retrives the list of all Documents** 

`GET/documentmanagement/odata/v1.0/aimsdocument`

**Response**

```json
[
  {
    "documentGUID": "9248b03b-b306-4fe8-a2b2-4e3189a57000-20190322065815000",
    "accessScope": "PUBLIC",
    "documentName": "Forecasting_20190322065521.json",
    "fileType": "JSON",
    "category": "backgrounJob",
    "aimsReference": "5190h4",
    "User": "test@aims360.com",
    "title": "Forecasting_20190322065521.json",
    "description": "Forecasting_20190322065521.json",
    "downloadUri": "https://apieast.aims360.rest/documentmanagement/v1.0/aimsdocument/9248b03b-b306-4fe8-a2b2-4e3189a57000-20190322065815000",
    "fileSize": 77328,
    "fileSizeInMB": 0.07374573,
    "lastUploaded": "2019-03-22T06:58:15.893Z"
  },
  {
    "documentGUID": "19803b1d-9547-4ed6-bf2f-111f1d9f4ec0-20190528081000000",
    "accessScope": "PUBLIC",
    "documentName": "backgroundjob_20190528081000843",
    "fileType": "JSON",
    "category": "backgrounJob",
    "aimsReference": "52336",
    "User": "TEST@AIMS360.COM",
    "title": "backgroundjob_20190528081000843",
    "description": "backgroundjob_20190528081000843",
    "downloadUri": "https://apieast.aims360.rest/documentmanagement/v1.0/aimsdocument/19803b1d-9547-4ed6-bf2f-111f1d9f4ec0-20190528081000000",
    "fileSize": 1367,
    "fileSizeInMB": 0.00130367279,
    "lastUploaded": "2019-05-28T08:10:00.96Z"
  },
  {
    "documentGUID": "a0005803-ea7e-4f65-87ad-697a710f000",
    "accessScope": "PRIVATE",
    "documentName": "SHP000043201.zip",
    "fileType": ".zip",
    "category": "Shipping Labels",
    "aimsReference": "000043201",
    "User": "TEST@AIMS360.COM",
    "title": "SHP000043201.zip",
    "description": "Labels",
    "downloadUri": "https://apieast.aims360.rest/documentmanagement/v1.0/aimsdocument/a0005803-ea7e-4f65-87ad-697a710f000",
    "fileSize": 1016,
    "fileSizeInMB": 0.0009689331,
    "lastUploaded": "2018-12-28T14:57:07.537Z"
  }
]
```

---------

**Retrives the list of Documents belongs to a specific category** 

`GET/documentmanagement/odata/v1.0/aimsdocument?$filter= category eq 'backgroundJob'`

**Response**

```json
[
  {
    "documentGUID": "9248b03b-b306-4fe8-a2b2-4e3189a57000-20190322065815000",
    "accessScope": "PUBLIC",
    "documentName": "Forecasting_20190322065521.json",
    "fileType": "JSON",
    "category": "backgrounJob",
    "aimsReference": "5190h4",
    "User": "test@aims360.com",
    "title": "Forecasting_20190322065521.json",
    "description": "Forecasting_20190322065521.json",
    "downloadUri": "https://apieast.aims360.rest/documentmanagement/v1.0/aimsdocument/9248b03b-b306-4fe8-a2b2-4e3189a57000-20190322065815000",
    "fileSize": 77328,
    "fileSizeInMB": 0.07374573,
    "lastUploaded": "2019-03-22T06:58:15.893Z"
  },
  {
    "documentGUID": "19803b1d-9547-4ed6-bf2f-111f1d9f4ec0-20190528081000000",
    "accessScope": "PUBLIC",
    "documentName": "backgroundjob_20190528081000843",
    "fileType": "JSON",
    "category": "backgrounJob",
    "aimsReference": "52336",
    "User": "TEST@AIMS360.COM",
    "title": "backgroundjob_20190528081000843",
    "description": "backgroundjob_20190528081000843",
    "downloadUri": "https://apieast.aims360.rest/documentmanagement/v1.0/aimsdocument/19803b1d-9547-4ed6-bf2f-111f1d9f4ec0-20190528081000000",
    "fileSize": 1367,
    "fileSizeInMB": 0.00130367279,
    "lastUploaded": "2019-05-28T08:10:00.96Z"
  }
]
```

    
 

-------
**Retrives details of a document with specific GUID** 


`GET/documentmanagement/odata/v1.0/aimsdocument?$filter= GUID eq a0005803-ea7e-4f65-87ad-697a710f000`

**Response**

```json
{
  "documentGUID": "a0005803-ea7e-4f65-87ad-697a710f000",
  "accessScope": "PRIVATE",
  "documentName": "SHP000043201.zip",
  "fileType": ".zip",
  "category": "Shipping Labels",
  "aimsReference": "000043201",
  "User": "TEST@AIMS360.COM",
  "title": "SHP000043201.zip",
  "description": "Labels",
  "downloadUri": "https://apieast.aims360.rest/documentmanagement/v1.0/aimsdocument/a0005803-ea7e-4f65-87ad-697a710f000",
  "fileSize": 1016,
  "fileSizeInMB": 0.0009689331,
  "lastUploaded": "2018-12-28T14:57:07.537Z"
}
```

------
**Downloads a specific document**


`GET/documentmanagement/v1.0/aimsdocument/{AimsDocument GUID}`

 Based on the Publish Access Scope, Bearer Token needs to be passed for authentication

**Response**

As per the access scope defined for the requested document, the user validation will be done if necessary and the file will be downloaded upon successful validation. 


<br>