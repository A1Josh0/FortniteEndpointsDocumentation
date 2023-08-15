# Battle Breakers MCP Profile Operations

## Request

**Method**: `POST` \
**URL**: `https://wex-public-service-live-prod.ol.epicgames.com/wex/api/game/v2/profile/:accountId/:operation` \
**Body**: `Individual`

## Query Parameters

| Name      | Value       | Default Value |
| --------- | ----------- | ------------- |
| profileId | {profileId} | profile0      |
| rvn       | -1          | -1            |

<br/>

## Profiles

| ProfileId   | Description                                                  |
| ----------- | ------------------------------------------------------------ |
| profile0    | Shared Profile Data (like "common_core" for Fortnite)        |
| levels      | Unlocked Zones, Worlds                                       |
| friends     | Stores all Friends Data (Epic didnt use the Friends Service) |
| monsterpit  |                                                              |
| multiplayer | PVP Stuff                                                    |
