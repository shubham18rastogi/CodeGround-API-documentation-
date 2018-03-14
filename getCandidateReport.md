---
layout : default
getCandidateReportClass: active
---

<center> <h1>Get Candidate Report</h1></center>
<br><br>                                          

### Description
Returns report of Candidate

### URL
```
Method Type: GET
https://BASE-URL/harvest/api/v1/getCandidateReport/{inviteId}
```

### Sample Response Data
Returns an Object, where object represent a Candidate's Report .
```
{
    "statuscode": "Completed",  //  status code
    "email": "6@a.com",  //  candidate's email
    "name": "Name",  //  candidate's name
    "phoneNumber": 123456789,  //  candidate's phone number
    "testMaxMarks": 4,  //  total marks of test
    "candidateScore": 4,  //  marks scored by candidate
    "questionairResponse": {},  //  List of responses that candidate chose
    "testStartTime": 1520399194068,  //  starting time of test in miliseconds
    "testDuration": 17654  //  time taken by candidate to complete the test 
}
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
{"errorMessage": "invalid inviteId"}
or
{"errorMessage": "candidate has not attempted the test"}
or
{"errorMessage": "inviteId can't be 0 or null"}
```
```
Status Code: 500
{"errorMessage": "Internal Server Error, please share the exception id with the CG team::Exception id is xxxxx"}
```

