## From Heroku DB directly to local DB


There is a method to pull postgres dump from prod to my local DB

`heroku pg:pull DATABASE_URL mylocaldb --app example-app`

It's better than creating pg_dump, downloading it, restoring local DB from dump. Basically, it's one-stop-solution

source - https://devcenter.heroku.com/articles/managing-heroku-postgres-using-cli#pg-push-and-pg-pull


---
even more useful when DB runs within a docker container -  use next command:
`PGPASSWORD=pg_pass_here PGHOST=localhost PGUSER=pg_username_here heroku pg:pull DATABASE_URL local_db_name --exclude-table-data "ultra_sensetive_data_or_something;event_store.events;event_store.streams;event_store.subscriptions;event_store.stream_events;event_store.snapshots;oban_jobs" --app company_prefix-my_awesome_app_name-staging`
