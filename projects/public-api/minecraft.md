# Minecraft Endpoints

**Table of Contents**
- [Minecraft Endpoints](#minecraft-endpoints)
  - [*GET `/minecraft/channels/get/{channel}`*](#get-minecraftchannelsgetchannel)

---
### *`GET /minecraft/channels/get/{channel}`*
> **Description:**  
> Gets a modpack that's attached to a user, in our database, if any.

| Query Parameters | Required? | Description |
|-|-|-|
| `raw` | :x: | Accepts `true` or `false`.<br/> If `true`, you'll get a JSON response. Otherwise, a string.|

**Sample Request** (_with query parameters_)
```
https://api.itsjusttriz.com/minecraft/channels/get/itsjusttriz?raw=true
```

**Sample Response** (*JSON*)
> - Success!
> ```json
> {
>     "code": 200,
>     "message": "The current modpack is FTB Skies. This can be found on FTB App. Created by FTB Team. Known Status: public. https://www.feed-the-beast.com/modpacks/103-ftb-skies",
>     "payload": {
>         "id": "ftbskies",
>         "name": "FTB Skies",
>         "launcher": "FTB App",
>         "link": "https://www.feed-the-beast.com/modpacks/103-ftb-skies",
>         "dev": "FTB Team",
>         "type": "public",
>         "image": "https://www.feed-the-beast.com/_next/image?url=https%3A%2F%2Fapps.modpacks.ch%2Fmodpacks%2Fart%2F99%2FFTB%20Skies%20512x512.png&w=256&q=75"
>     }
> }
> ```
> - Fail!
> ```json
> {
>   "code": 404,
>   "message":"Invalid Entry!",
>   "payload": {}
> }
> ```
**Sample Response** (*String*)
> ```
> The current modpack is FTB Skies. This can be found on FTB App. Created by FTB Team.
> Known Status: public. https://www.feed-the-beast.com/modpacks/103-ftb-skies
> ```
> ...or...
> ```
> Invalid Entry!
> ```
