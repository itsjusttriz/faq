[<- _Back to Main_](index.md)
# Stackup Endpoints

**Table of Contents**
- [Stackup Endpoints](#stackup-endpoints)
    - [*`GET /stackup/events/{eventId}`*](#get-stackupeventseventid)

---
### *`GET /stackup/events/{eventId}`*
> **Description:**  
> Gets donation data for a StackUpDotOrg event, if any.

| Query Parameters | Required? | Description |
|-|-|-|
| `raw` | :x: | Accepts `true` or `false`.<br/> If `true`, you'll get a JSON response. Otherwise, a string.|
| `key` | :x: | Accepts any key from the raw data.<br/> This will give back, only, the value of that key from the raw data.|

**Sample Request** (_with query parameters_)
```
https://api.itsjusttriz.com/stackup/events/509?raw=true
```

**Sample Response** (*JSON*)
> - Success!
> ```json
> {
>   "code": 200,
>   "message": "\"Call to Arms - 2023\" is this year's StackUpDotOrg fundraising event in support of Army Veterans! In total so far, $273,071.57 out of $350,000 has been raised by 79 teams. Click here for more info, or to donate: https://stackup.donordrive.com/index.cfm?fuseaction=donate.event&eventID=509",
>   "payload": {
>       "fundraisingGoal": 350000,
>       "numParticipants": 1182,
>       "numTeams": 79,
>       "registerURL": "https://stackup.donordrive.com/index.cfm?fuseaction=register.start&eventID=509",
>       "donateURL": "https://stackup.donordrive.com/index.cfm?fuseaction=donate.event&eventID=509",
>       "pageURL": "https://stackup.donordrive.com/index.cfm?fuseaction=donorDrive.event&eventID=509",
>       "avatarImage": "https://assets.donordrive.com/StackUp/images/$avatars$/site_100.jpg",
>       "publishDateUTC": "2023-01-01T01:32:37.870+0000",
>       "donCutoffDateUTC": "2024-01-01T05:00:00.0+0000",
>       "timeZone": "America/New_York",
>       "type": "P",
>       "hasDates": true,
>       "regCutoffDateUTC": "2024-01-01T04:30:00.0+0000",
>       "sumDonations": 273071.57,
>       "eventID": 509,
>       "name": "Call to Arms - 2023",
>       "endDateUTC": "2024-01-01T04:45:00.0+0000",
>       "avatarImageURL": "https://assets.donordrive.com/StackUp/images/$avatars$/site_100.jpg",
>       "startDateUTC": "2023-01-01T05:00:00.0+0000",
>       "numDonations": 5460
>   }
> }
> ```
> - Fail!
> ```json
> {
>   "code": 404,
>   "message":"[ijt.api.ERROR] Invalid entry! Could not find any information for Event: 509.",
>   "payload": {}
> }
> ```
**Sample Response** (*String*)
> ```
> "Call to Arms - 2023" is this year's StackUpDotOrg fundraising event in support of Army Veterans! In total so far, $273,071.57 out of $350,000 has been raised by 79 teams. Click here for more info, or to donate: https://stackup.donordrive.com/index.cfm?fuseaction=donate.event&eventID=509
> ```
> ...or...
> ```
> [ijt.api.ERROR] Invalid entry! Could not find any information for Event: 509.
> ```
[&#8593; *Back to top*](#minecraft-endpoints)

---