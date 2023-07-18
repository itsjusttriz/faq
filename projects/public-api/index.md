# IJT.api Documentation
**Table of Contents**
- [IJT.api Documentation](#ijtapi-documentation)
  - [The base Api Url](#the-base-api-url)
  - [Usage Notes](#usage-notes)
  - [Endpoint paths](#endpoint-paths)
      - [/minecraft](#minecraft)
      - [/misc](#misc)
      - [/stackup](#stackup)
      - [/twitch](#twitch)

## The base Api Url
The base url for this API server is: [https://api.itsjusttriz.com]()

This URL is prone to changes at any time, but the above will be kept up-to-date whenever that may happen.

## Usage Notes
- Almost **ALL** endpoints will return a `String`, unless `?raw=true` is attached to the URL. If a successful call to an endpoint is intended to return JSON, the default `String` will state the following:
  > *Check 'payload' property. (Add `?raw=true` to the URL)*

## Endpoint paths

#### /minecraft

  - *`GET /minecraft/channels/get/{channel}`* [*See more...*](minecraft.md#get-minecraftchannelsgetchannel)
  - *`GET /minecraft/channels/set/{channel}/{modpackId}`* [*See more...*](minecraft.md#get-minecraftchannelssetchannelmodpackid)
  - *`GET /minecraft/channels/list`* [*See more...*](minecraft.md#get-minecraftchannelslist)
  - *`GET /minecraft/get/{modpackId}`* [*See more...*](minecraft.md#get-minecraftgetmodpackid)
  - *`GET /minecraft/list`* [*See more...*](minecraft.md#get-minecraftlist)

#### /misc

  - *`GET /misc/temp`* [*See more...*](misc.md#get-misctemperature)
  - *`GET /misc/timeFrom`* [*See more...*](misc.md#get-misctimeFrom)
  - *`GET /misc/temperature`* [*See more...*](misc.md#get-misctimeUntil)

#### /stackup

  - *`GET /stackup/events/{eventId}`* [*See more...*](stackup.md#get-stackupeventseventid)
  - *`GET /stackup/teams/{teamId}`* [*See more...*](stackup.md#get-stackupteamsteamid)
  - *`GET /stackup/participants/{participantId}`* [*See more...*](stackup.md#get-stackupparticipantsparticipantid)

#### /twitch

  - *`GET /twitch/user/{userIdOrName}`* [*See more...*](twitch.md#get-twitchuseruseridorname)
  - *`GET /twitch/vods/{userIdOrName}`* [*See more...*](twitch.md#get-twitchvodsuseridorname)