# Welcome to https://exchangeblacklist.com
This is an always up-to-date community driven blacklist of cryptocurrency exchanges that have been flagged as scams due to real-world user experiences.  Please submit your stories and source materials as pull requests and the list will be updated.  For ease of access we choose the JSON format which will allow you to easily build queries around dangerous exchanges.  Stay frosty!

# API Endpoints
https://exchangeblacklist.com/api

# API Examples
```List all blacklisted exchanges still trading
curl https://exchangeblacklist.com/api | jq '.data | select((status[].still_trading == "true") and .url)'```

List all known exchanges currently blacklisted by url
curl https://exchangeblacklist.com/api | jq .data.[].url

List all known exchanges without user API
curl https://exchangeblacklist.com/api | jq '.data.[] | select(.user_api_enabled == "true")'
