# scout
Valorant Twitch Extension

## Description
Valorant scout is a simple twitch extension that keeps viewers up to date with the streamer's overall stats. This will allow streamers to show their account's stats as a screen overlay removing the need to set up and maintain a rank command that shows their rank/stats in chat

## Riot API
For this extension, we will be utilizing the  `VAL-MATCH-V1` and `VAL-CONTENT-V1` apis.
We will showcase the streamers associated valorant profile at the top with his current stats. Below that we will show a list of recent matches that the viewer can click on and inspect matches in further detail.

### VAL-MATCH-V1
This extension will use the `/val/match/v1/matchlists/by-puuid/{puuid}` endpoint to fetch the player's recent matches. Viewers will be able to click on a match from the list and see further info provided by `/val/match/v1/matches/{matchId}` endpoint.

### VAL-CONTENT-V1
We will use the contents API to map resources from `VAL-MATCH-V1`, like a `mapId` from the `/val/match/v1/matches/{matchId}` response.
