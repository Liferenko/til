## OrbStack

I was looking for something not that hungry as Docker Desktop is. OrbStack appeared.

So now it's not only resolve my issue when running local Postgres - I even can make a VM mostly the same way. So instead of containers I got Vagrant alternative as well.

More here - https://docs.orbstack.dev/headless#getting-started

Example of usage:
1. `orb` - starts OrbStack
2. `your docker-compose command here to start Psql container from compose.yml`
3. `orb create ubuntu ci-runner` - create VM
