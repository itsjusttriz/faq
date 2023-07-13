# Minecraft Endpoints

**Table of Contents**
- [Minecraft Endpoints](#minecraft-endpoints)
  - [*`GET /minecraft/channels/get/{channel}`*](#get-minecraftchannelsgetchannel)

## *`GET /minecraft/channels/get/{channel}`*
Gets a modpack that's attached to a user, in our database, if any.

If *`?raw=true`* is present, you will receive a JSON Object. Otherwise, you'll receive a *`String`*.

**Sample Response** (*JSON*)
```json
{
    "code": 200,
    "message": "The current modpack is FTB Skies. This can be found on FTB App. Created by FTB Team. Known Status: public. https://www.feed-the-beast.com/modpacks/103-ftb-skies",
    "payload": {
        "id": "ftbskies",
        "name": "FTB Skies",
        "launcher": "FTB App",
        "link": "https://www.feed-the-beast.com/modpacks/103-ftb-skies",
        "dev": "FTB Team",
        "type": "public",
        "image": "https://www.feed-the-beast.com/_next/image?url=https%3A%2F%2Fapps.modpacks.ch%2Fmodpacks%2Fart%2F99%2FFTB%20Skies%20512x512.png&w=256&q=75"
    }
}
```
**Sample Response** (*String*)
```
The current modpack is FTB Skies. This can be found on FTB App. Created by FTB Team.
Known Status: public. https://www.feed-the-beast.com/modpacks/103-ftb-skies
```