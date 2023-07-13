# IJT.api Documentation
**Table of Contents**
- [IJT.api Documentation](#ijtapi-documentation)
  - [Api Base Url](#api-base-url)
  - [Api Usage Notes](#api-usage-notes)
  - [Api Endpoints](#api-endpoints)
    - [/minecraft/get](#minecraftget)

## Api Base Url
The base url for this API server is: [https://api.itsjusttriz.com]()

This URL is prone to changes at any time, but the above will be kept up-to-date whenever that may happen.

## Api Usage Notes
- Almost **ALL** endpoints will return a `String`, unless `?raw=true` is attached to the URL. If a successful call to an endpoint is intended to return JSON, the default `String` will state the following:
> ```
> Check the \'payload\' property. (Add ?raw=true to the URL)
> ```

## Api Endpoints
### /minecraft/get