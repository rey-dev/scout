# scout
Valorant Twitch Extension


## Description
Twitch overlay extension that will show valorant account rank and statistics on stream. This removes the need for the streamer to create and manage rank/stat commands in chat, as well as provide an interactive ui for viewers.


## Riot API
For this extension, we will be utilizing the  `VAL-MATCH-V1` and `VAL-CONTENT-V1` apis.
We will showcase the streamers associated valorant profile at the top with his current stats. Below that we will show a list of recent matches that the viewer can click on and inspect matches in further detail.

### VAL-MATCH-V1
This extension will use the `/val/match/v1/matchlists/by-puuid/{puuid}` endpoint to fetch the player's recent matches. Viewers will be able to click on a match from the list and see further info provided by `/val/match/v1/matches/{matchId}` endpoint.

### VAL-CONTENT-V1
We will use the contents API to map resources from `VAL-MATCH-V1`, like a `mapId` from the `/val/match/v1/matches/{matchId}` response.
