[<- _Back to Main_](index.md)
# Minecraft Endpoints

**Table of Contents**
- [Minecraft Endpoints](#minecraft-endpoints)
    - [*`GET /minecraft/channels/get/{channel}`*](#get-minecraftchannelsgetchannel)
    - [*`GET /minecraft/channels/set/{channel}/{modpackId}`*](#get-minecraftchannelssetchannelmodpackid)
    - [*`GET /minecraft/channels/list`*](#get-minecraftchannelslist)
    - [*`GET /minecraft/get/{modpackId}`*](#get-minecraftgetmodpackid)
    - [*`GET /minecraft/list`*](#get-minecraftlist)

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
[&#8593; *Back to top*](#minecraft-endpoints)

---
### *`GET /minecraft/channels/set/{channel}/{modpackId}`*
> **Description:**  
> Assigns a modpack to a user, in our database, if any.

| Query Parameters | Required? | Description |
|-|-|-|
| `raw` | :x: | Accepts `true` or `false`.<br/> If `true`, you'll get a JSON response. Otherwise, a string.|

**Sample Request** (_with query parameters_)
```
https://api.itsjusttriz.com/minecraft/channels/set/itsjusttriz/ftbone?raw=true
```

**Sample Response** (*JSON*)
> - Success!
> ```json
> {
>     "code": 200,
>     "message": "Assigned \"FTB One\" to #itsjusttriz. [1 change(s)]",
>     "payload": {
>       "channel": "itsjusttriz",
>       "changes": 1,
>       "modpack": {
>         "id": "ftbone",
>         "name": "FTB One",
>         "launcher": "FTB App",
>         "link": "https://feed-the-beast.com/modpack/97_ftb_one",
>         "dev": "FTB Team",
>         "type": "public_beta",
>         "image": "https://apps.modpacks.ch/modpacks/art/93/logo.png"
>       }
>     }
> }
> ```
> - Fail!
> ```json
> {
>   "code": 404,
>   "message":"[ijt.api.ERROR] Invalid entry! Visit http://itsjusttriz.com/#/projects/modpacks for the correct modpackId.",
>   "payload": {}
> }
> ```
**Sample Response** (*String*)
> ```
> Assigned "FTB One" to #itsjusttriz. [1 change(s)]
> ```
> ...or...
> ```
> [ijt.api.ERROR] Invalid entry! Visit http://itsjusttriz.com/#/projects/modpacks for the correct modpackId.
> ```
[&#8593; *Back to top*](#minecraft-endpoints)

---
### *`GET /minecraft/channels/list`*
> **Description:**  
> Lists all modpacks, assigned to users in our database, if any.

| Query Parameters | Required? | Description |
|-|-|-|
| `raw` | :x: | Accepts `true` or `false`.<br/> If `true`, you'll get a JSON response. Otherwise, a string.|

**Sample Request** (_with query parameters_)
```
https://api.itsjusttriz.com/minecraft/channels/list?raw=true
```

**Sample Response** (*JSON*)
> - Success!
> ```json
> {
>     "code": 200,
>     "message": "Found 9 documents. Check \"payload\" property.",
>     "payload": {
>       "itsjusttriz": {
>         "id": "ftbone",
>         "name": "FTB One",
>         "launcher": "FTB App",
>         "link": "https://feed-the-beast.com/modpack/97_ftb_one",
>         "dev": "FTB Team",
>         "type": "public_beta",
>         "image": "https://apps.modpacks.ch/modpacks/art/93/logo.png"
>       },
>       "...8 more"
>     }
> }
> ```
> - Fail!
> ```json
> {
>   "code": 404,
>   "message":"[ijt.api.ERROR] Invalid entry!",
>   "payload": {}
> }
> ```
**Sample Response** (*String*)
> ```
> Found 9 documents. Check "payload" property.
> ```
> ...or...
> ```
> [ijt.api.ERROR] Invalid entry!
> ```
[&#8593; *Back to top*](#minecraft-endpoints)

---
### *`GET /minecraft/get/{modpackId}`*
> **Description:**  
> Gets a modpack from our database, if any.

| Query Parameters | Required? | Description |
|-|-|-|
| `raw` | :x: | Accepts `true` or `false`.<br/> If `true`, you'll get a JSON response. Otherwise, a string.|

**Sample Request** (_with query parameters_)
```
https://api.itsjusttriz.com/minecraft/get/ftbone?raw=true
```

**Sample Response** (*JSON*)
> - Success!
> ```json
> {
>     "code": 200,
>     "message": "Found 1 document { FTB One }",
>     "payload": {
>       "id": "ftbone",
>       "name": "FTB One",
>       "launcher": "FTB App",
>       "link": "https://feed-the-beast.com/modpack/97_ftb_one",
>       "dev": "FTB Team",
>       "type": "public_beta",
>       "image": "https://apps.modpacks.ch/modpacks/art/93/logo.png
>     }
> }
> ```
> - Fail!
> ```json
> {
>   "code": 404,
>   "message":"[ijt.api.ERROR] Invalid entry!",
>   "payload": {}
> }
> ```
**Sample Response** (*String*)
> ```
> Found 1 document { FTB One }
> ```
> ...or...
> ```
> [ijt.api.ERROR] Invalid entry!
> ```
[&#8593; *Back to top*](#minecraft-endpoints)

--- 

---
### *`GET /minecraft/list`*
> **Description:**  
> Lists all modpacks from our database, if any.

| Query Parameters | Required? | Description |
|-|-|-|
| `raw` | :x: | Accepts `true` or `false`.<br/> If `true`, you'll get a JSON response. Otherwise, a string.|

**Sample Request** (_with query parameters_)
```
https://api.itsjusttriz.com/minecraft/list?raw=true
```

**Sample Response** (*JSON*)
> - Success!
> ```json
> {
>     "code": 200,
>     "message": "Found 194 documents.",
>     "payload": [
>       {
>          "id": "ftbone",
>          "name": "FTB One",
>          "launcher": "FTB App",
>          "link": "https://feed-the-beast.com/modpack/97_ftb_one",
>          "dev": "FTB Team",
>          "type": "public_beta",
>          "image": "https://apps.modpacks.ch/modpacks/art/93/logo.png"
>       },
>       "...193 more"
> }
> ```
> - Fail!
> ```json
> {
>   "code": 404,
>   "message":"[ijt.api.ERROR] Invalid entry! It seems this table is empty.",
>   "payload": {}
> }
> ```
**Sample Response** (*String*)
> ```
> Found 194 documents.
> ```
> ...or...
> ```
> [ijt.api.ERROR] Invalid entry! It seems this table is empty.
> ```
[&#8593; *Back to top*](#minecraft-endpoints)

--- 
