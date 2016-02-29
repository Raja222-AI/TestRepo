## Timesheet - fetching tasks for the allocated projects
For a given user, this returns an array of tasks for all the allocated projects of the current week OR the week of the provided date.
Date must be in 'DDMMYYYY' format

**Path:**`/api/v1/timesheet/tasks?date=DDMMYYYY` OR `/api/v1/timesheet/tasks`

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
    "_id": "TASK-1.1", //ObjectID format
    "project": {
      "id": "PRJ-1", //ObjectID format
      "name": "OCR-1"
    },
    "milestone": "Design",
    "name": "Database Design",
    "type": ""
  },
  {
    "_id": "TASK-1.2",
    "project": {
      "id": "PRJ-1",
      "name": "OCR-1"
    },
    "milestone": "Design",
    "name": "Database Design",
    "type": ""
  },
  {
    "_id": "TASK-6.1",
    "project": {
      "id": "PRJ-6",
      "name": "OCR-6"
    },
    "milestone": "Design",
    "name": "Database Design",
    "type": ""
  },
  {
    "_id": "TASK-6.2",
    "project": {
      "id": "PRJ-6",
      "name": "OCR-6"
    },
    "milestone": "Design",
    "name": "Database Design",
    "type": ""
  },
  {
    "_id": "TASK-4.1",
    "project": {
      "id": "PRJ-4",
      "name": "OCR-4"
    },
    "milestone": "Design",
    "name": "Database Design",
    "type": ""
  },
  {
    "_id": "TASK-4.2",
    "project": {
      "id": "PRJ-4",
      "name": "OCR-4"
    },
    "milestone": "Design",
    "name": "Database Design",
    "type": ""
  },
  ....
]

```

**Failure**

Any error result is indicated via the HTTP response status code. Error object will not be available.