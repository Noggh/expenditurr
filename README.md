# Expenditurr

## Description

Expenditurr is a application written in Haskell that let users run a backend and frontend to help
keep track of their incomes, outcomes and as well to empower them to schedule and program their financial
life.

Luckily users shall find it useful.

## Next Steps

- [x] Setup basic PostgreSQL container and run the application

## Running

Follow the commands below to start your application properly:

```bash
# before starting the application, start the DB container
# the default port I'm using is 15432, but you can change on docker-compose.yml
$ DATABASE_PWD=<dummy_password> docker compose up -d
```

Once your database is UP and Running, then start the application:

```bash
# if it's your first run, the official website recommends running this command before
$ stack install yesod-bin --install-ghc

# start the WARP server listening at port :10000
$ YESOD_PGPASS=<dummy_password> stack exec -- yesod devel
```
