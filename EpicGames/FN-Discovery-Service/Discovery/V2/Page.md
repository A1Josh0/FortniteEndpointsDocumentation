## FN - Discovery Service: Discovery Surface Page (V2)

URL: https://fn-service-discovery-live-public.ogs.live.on.epicgames.com/api/v2/discovery/surface/:surfaceName/page \
Method: POST \
Auth Required: Yes (`discovery:surface:query READ`)

## Headers

`X-Epic-Access-Token`: The [current discovery access token](/Fortnite/Creative/DiscoveryAccessToken.md)

<br/>

```json
{
  "testVariantName": "BrowseVariant3",
  "panelName": "BrowseNewUpdatesThisWeek",
  "pageIndex": 0,
  "playerId": "94b1569506b04f9f8557af611e8c5e47",
  "partyMemberIds": ["94b1569506b04f9f8557af611e8c5e47"],
  "matchmakingRegion": "EU",
  "platform": "Windows",
  "isCabined": false
}
```

## Path Parameters

`surfaceName`: See [Surfaces](../README.md#surfaces)

## Parameters

`panelName`: The panel you want to load a different page of <br/>
`pageIndex`: The page you want to load from the panel <br/>
`partyMemberIds`: Array of the party member account ids (or an empty array) <br/>
`matchmakingRegion`: Your matchmaking region (e.g. `EU`) <br/>
`platform`: Your platform (e.g. `Windows`) <br/>
`isCabined`: If your Account is in Cabined Mode (from [own account info](../../../AccountService/Account/Lookup/AccountId.md))

> Technically the request wont fail if only `testVariantName`, `panelName` and `pageIndex` are provided

## Query Parameters

`appId`: `Fortnite` <br/>
`stream`: The Fortnite Branch (URL Encoded), so the branch `++Fortnite+Release-26.30` would need to be encoded like `%2B%2BFortnite%2BRelease-26.30`

---

_Example Response (shortened)_

```json
{
  "results": [
    {
      "lastVisited": null,
      "linkCode": "3829-1693-8905",
      "isFavorite": false,
      "globalCCU": 2
    },
    {
      "lastVisited": null,
      "linkCode": "0482-1284-7823",
      "isFavorite": false,
      "globalCCU": 138
    },
    {
      "lastVisited": null,
      "linkCode": "3522-1332-2508",
      "isFavorite": false,
      "globalCCU": 1
    },
    {
      "lastVisited": null,
      "linkCode": "4243-3675-9905",
      "isFavorite": false,
      "globalCCU": -1
    }
  ],
  "hasMore": false,
  "panelTargetName": null
}
```