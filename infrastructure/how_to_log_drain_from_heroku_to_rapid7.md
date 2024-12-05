## Heroku log drains to Rapid7 InsightOps


### Step 1: Get a token from Rapid7 InsightOps
- press the "Add Data" button in the top right corner
- select "Quick add", fill the fields and press "Add new logs"
- copy the token from the "Log Token" field

### Step 2: Add the log drain to Heroku
- you need to be loggen in to Heroku CLI
- run `heroku drains:add https://https://eu.webhook.logs.insight.rapid7.com/v1/drain/%PASTE_TOKEN_HERE%  --app your-app-staging`
- check in Log search open preview
