---
layout : default
getLiveTestClass : active
---


<center> <h1>Get All Test</h1></center>
<br>                                           

### Description
Returns the list of all *Live* tests.

### URL
```
Method Type: GET
https://BASE-URL/harvest/api/v1/getLiveTests/{pageNo}
```

### Sample Response Data
Returns an array of Object, where each object represent a live test .
```
[
    {
        "testId": 343,  // Test Id
        "testName": "public2", // Test name
        "testOpenTime": 1520317324138, // When did the test opened timestamp in GMT
        "testCloseTime": 1521526860000,// When will the test close timestamp in GMT
        "totalMarks": 8,  // total marks for the test
        "cutOffMarks": 0,  // cut off Marks for the test
        "candidateReportNotificationUrl": null  //  whenever candidate completes the test this Webhook 
                                                    will be called to notify.
    },
    {
        "testId": 318,
        "testName": "hello127",
        "testOpenTime": 1519985460232,
        "testCloseTime": 1521367800000,
        "totalMarks": 4,
        "cutOffMarks": 0,
        "candidateReportNotificationUrl": null
    },
    {
        "testId": 315,
        "testName": "hello126",
        "testOpenTime": 1519985444680,
        "testCloseTime": 1520763000000,
        "totalMarks": 4,
        "cutOffMarks": 0,
        "candidateReportNotificationUrl": null
    }
]
```

### Possible Exceptions
```
Status Code: 600
{"errorMessage": "apiKey can't be null"}
or 
{"errorMessage": "apikey not mapped to a user"}
```

```
Status Code: 602
{"errorMessage": "Page number can't be negative"}
```

```
Status Code: 500
{"errorMessage": "Internal Server Error, please share the exception id with the CG team::Exception id is xxxxx"}
```

