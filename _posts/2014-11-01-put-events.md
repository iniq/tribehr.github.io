---
category: API v2
title: 'Modify an Event'
type: 'PUT'
path: '/events'

layout: default
---

### Request

Modify an existing Event. Supports all of the same parameters as the **`POST`** request above, but you
**must** include an **`:id`** parameter that matches the ID in the URL.

The example request here updates the name and start date of event #254.

```PUT /events/{id}.json
X-API-Version: 2.0.0
id=254&
name=New%20event%20%28Updated%20Time%21%29&
start_date=2013-08-30T18%3A00%3A00%2B00%3A00
```

### Response

```Status: 200 OK```
```{
    "id": 254,
    "name": "New event (Updated Time!)",
    "start_date": "2013-08-30T18:00:00+00:00",
    "end_date": "2013-08-30T22:00:00+00:00",
    "notes": "HTML description of new event",
    "is_official_holiday": true,
    "created": "2013-08-19T18:02:04+00:00",
    "modified": "2013-08-19T18:30:35+00:00",
    "url": "/events/254.json",
    "event_type": {
        "id": 1,
        "name": "Lunch",
        "url": "/event_types/1.json"
    },
    "locations": [
        {
            "id": 1,
            "name": "Central Rental",
            "url": "/locations/1.json"
        },
        {
            "id": 7,
            "name": "Headquarters",
            "url": "/locations/7.json"
        }
    ]
}
```