![](api2.jpg)

**Examples**
```sh
curl https://api2.hackclub.com/ping
# returns "pong!"

curl https://api2.hackclub.com/v0/Operations/Badges
# returns JSON array of records from 'Badges' table in 'Operations' base

curl https://api2.hackclub.com/v0/Operations/Badges/rec9j291j3k928
# returns JSON object from airtable

curl https://api2.hackclub.com/v0/Operations/Addresses # or some other sensative data
# "ERROR: Tried to access table that is not in the whitelist."

# Lend your own Airtable API keys to get past the whitelist
curl -H "Authorization: Bearer VALID_AIRTABLE_KEY" https://api2.hackclub.com/v0/Operations/Addresses
# returns JSON array of non-whitelisted records from airtable
```