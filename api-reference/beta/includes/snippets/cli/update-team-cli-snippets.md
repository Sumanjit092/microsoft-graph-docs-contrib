---
description: "Automatically generated file. DO NOT MODIFY"
---

```bash


mgc-beta teams patch --team-id {team-id} --body '{\
 "isMembershipLimitedToOwners": true,\
  "memberSettings": {\
    "allowCreateUpdateChannels": true\
  },\
  "messagingSettings": {\
    "allowUserEditMessages": true,\
    "allowUserDeleteMessages": true\
  },\
  "funSettings": {\
    "allowGiphy": true,\
    "giphyContentRating": "strict"\
  },\
  "discoverySettings": {\
    "showInTeamsSearchAndSuggestions": true\
  }\
}\
'

```