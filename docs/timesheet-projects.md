## Timesheet - Fetching allocated projects API
For a given user, this returns an array of allocated projects for the current week OR for the week of the provided date.
Date must be in 'DDMMYYYY' format.

**Path:**`/api/v1/timesheet/projects?date=DDMMYYYY` OR `/api/v1/timesheet/projects`

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
  ....,
  {
    "_id": "ALLOC-6", //ObjectID format
    "project": {
      "_id": "PRJ-6", //ObjectID format
      "name": "OCR-6"
    },
    "resource": {
      "_id": "INC0081", //ObjectID format
      "displayName": "MURALI-1",
      "avatar": "AVATAR/MURALI.JPG",
      "designation": "DEV"
    },
    "milestone": "Design",
    "name": "OCR",
    "type": "Billable",
    "startDate": "2016-02-28T18:30:00.000Z",
    "endDate": "2016-03-05T18:29:59.999Z",
    "allocationPercentage": 50
  },
  {
    "_id": "ALLOC-4",
    "project": {
      "_id": "PRJ-4",
      "name": "OCR-4"
    },
    "resource": {
      "_id": "INC0081",
      "displayName": "MURALI-1",
      "avatar": "AVATAR/MURALI.JPG",
      "designation": "DEV"
    },
    "milestone": "Design",
    "name": "OCR",
    "type": "Billable",
    "startDate": "2016-02-24T18:30:00.000Z",
    "endDate": "2016-02-29T18:29:59.999Z",
    "allocationPercentage": 50
  },
  {
    "_id": "ALLOC-1",
    "project": {
      "_id": "PRJ-1",
      "name": "OCR-1"
    },
    "resource": {
      "_id": "INC0081",
      "displayName": "MURALI-1",
      "avatar": "AVATAR/MURALI.JPG",
      "designation": "DEV"
    },
    "milestone": "Design",
    "name": "OCR",
    "type": "Billable",
    "startDate": "2016-01-31T18:30:00.000Z",
    "endDate": "2016-02-29T18:29:59.999Z",
    "allocationPercentage": 50
  },
  ....
]

```

**Failure**

Any error result is indicated via the HTTP response status code. Error object will not be available.