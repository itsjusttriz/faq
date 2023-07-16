# Misc Endpoints - [_Back to Main_](index.md)

**Table of Contents**
- [Misc Endpoints](#misc-endpoints)
  - [*GET `/misc/temp`*](#get-misctemp)
  - [*GET `/misc/timeFrom`*](#get-misctimeFrom)
  - [*GET `/misc/timeUntil`*](#get-misctimeUntil)

---
### *`GET /misc/temp`*
> **Description:**  
> Gets a temperature value in either Celsius or Fahrenheit, depending on query parameters.

| Query Parameters | Required? | Description |
|-|-|-|
| `raw` | :x: | Accepts `true` or `false`.<br/> If `true`, you'll get a JSON response. Otherwise, a string.|
| `from` | ✅ | Accepts `fahrenheit`,`f`,`celsius`,`c`.<br/>This will be the value that you want to convert **from**.
| `to` | ✅ | Accepts `fahrenheit`,`f`,`celsius`,`c`.<br/>This will be the value that you want to convert **to**.
| `value` | ✅ | Accepts a number or a float.<br/>This will be the number value that you want to convert.

**Sample Request** (_with query parameters_)
```
https://api.itsjusttriz.com/misc/temp?from=f&to=c&value=110&raw=true
```

**Sample Response** (*JSON*)
> - Success!
> ```json
> {
>   "code": 200,
>   "message": "43.333333333333336",
>   "payload": {
>     "f": "110",
>     "c": "43.333333333333336"
>   }
> }
> ```
> - Fail!
> ```json
> {
>   "code": 404,
>   "message": "[ijt.api.ERROR] Something went wrong?",
>   "payload": {}
> }
> ```
**Sample Response** (*String*)
> ```
> 43.333333333333336
> ```
> ...or...
> ```
> [ijt.api.ERROR] Something went wrong?
> ```

---

### *`GET /misc/timeFrom`*
> **Description:**  
> Gets a time duration based on specified starting timestamp.

| Query Parameters | Required? | Description |
|-|-|-|
| `raw` | :x: | Accepts `true` or `false`.<br/> If `true`, you'll get a JSON response. Otherwise, a string.|
| `timestamp` | ✅ | Accepts a valid timestamp from the past (`2022-12-01T00:00`).<br/>This will be the timestamp used to begin the duration calculation.
| `includeWeeks` | ✅ | Accepts `true`/`false`.<br/>This will decide if you want to seperate the weeks from the days.<br/>e.g. instead of `12 days`, you'll get `1 weeks, 5 days`.

**Sample Request** (_with query parameters_)
```
https://api.itsjusttriz.com/misc/timeFrom?raw=true&timestamp=2022-12-01T00:00&includeWeeks=true
```

**Sample Response** (*JSON*)
> - Success!
> ```json
> {
>   "code": 200,
>   "message": "32 weeks, 3 days, 3 hours, 18 minutes, 6 seconds",
>   "payload": {
>     "weeks": 32,
>     "days": 3,
>     "hours": 3,
>     "minutes": 18,
>     "seconds": 6
>   }
> }
> ```
> - Fail!
> ```json
> {
>   "code": 404,
>   "message": "[ijt.api.ERROR] Invalid Timestamp: 2023-12-01T00:00. The timestamp MUST be from the past.",
>   "payload": {}
> }
> ```
**Sample Response** (*String*)
> ```
> 32 weeks, 3 days, 3 hours, 18 minutes, 6 seconds
> ```
> ...or...
> ```
> [ijt.api.ERROR] Invalid Timestamp: 2023-12-01T00:00. The timestamp MUST be from the past.
> ```

---

### *`GET /misc/timeUntil`*
> **Description:**  
> Gets a time duration based on specified ending timestamp.

| Query Parameters | Required? | Description |
|-|-|-|
| `raw` | :x: | Accepts `true` or `false`.<br/> If `true`, you'll get a JSON response. Otherwise, a string.|
| `timestamp` | ✅ | Accepts a valid timestamp from the future (`2023-12-01T00:00`).<br/>This will be the timestamp used to calculate the durations ending.
| `includeWeeks` | ✅ | Accepts `true`/`false`.<br/>This will decide if you want to seperate the weeks from the days.<br/>e.g. instead of `12 days`, you'll get `1 weeks, 5 days`.

**Sample Request** (_with query parameters_)
```
https://api.itsjusttriz.com/misc/timeUntil?raw=true&timestamp=2023-12-01T00:00&includeWeeks=true
```

**Sample Response** (*JSON*)
> - Success!
> ```json
> {
>   "code": 200,
>   "message": "19 weeks, 4 days, 20 hours, 38 minutes, 43 seconds",
>   "payload": {
>     "weeks": 19,
>     "days": 4,
>     "hours": 20,
>     "minutes": 38,
>     "seconds": 43
>   }
> }
> ```
> - Fail!
> ```json
> {
>   "code": 404,
>   "message": "[ijt.api.ERROR] Invalid Timestamp: 2022-12-01T00:00. The timestamp MUST be from the future.",
>   "payload": {}
> }
> ```
**Sample Response** (*String*)
> ```
> 19 weeks, 4 days, 20 hours, 38 minutes, 43 seconds
> ```
> ...or...
> ```
> [ijt.api.ERROR] Invalid Timestamp: 2022-12-01T00:00. The timestamp MUST be from the future.
> ```
