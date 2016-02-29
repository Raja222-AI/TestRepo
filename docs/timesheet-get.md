## Fetching timesheet API
For a given user, this returns the timesheet for the current week OR for the week starting on the provided date.
Date must be in 'DDMMYYYY' format.

**Path:**`/api/v1/timesheet/get?startDate=DDMMYYYY` OR `/api/v1/timesheet/get`

**Method:**`GET`

**Headers:** 
```
x-access-token
x-email-id
userId
```

**URL Parameters** None

**Cookies** None

### Response

**Success**

```
[
  {
    "_id": "TS5",	// this will be Object id
    "user": {
      "_id": "INC0081",	// this will be Object id
      "displayName": "Murali",
      "avatar": "avatar/murali.jpg"
    },
    "createdAt": "2016-02-28T18:30:00.000Z",
    "updatedAt": "2016-03-03T18:30:00.000Z",
    "startDate": "29-02-2016",
    "endDate": "04-03-2016",
    "submittedHours": 45,
    "allocatedHours": 45,
    "days": [
      {
        "date": "2016-02-28T18:30:00.000Z",
        "status": "prefilled"
      },
      {
        "date": "2016-02-29T18:30:00.000Z",
        "status": "submitted"
      },
      {
        "date": "2016-03-01T18:30:00.000Z",
        "status": "approved"
      },
      {
        "date": "2016-03-02T18:30:00.000Z",
        "status": "rejected"
      },
      {
        "date": "2016-03-03T18:30:00.000Z",
        "status": "submitted"
      }
    ]
  }
]

```

**Failure**

Any error result is indicated via the HTTP response status code. Error object will not be available.