# Docker Compose Releases

Here are the latest published Docker Compose stack for self-hosting this project.

These can be deployed on either Docker or Docker Swarm.

## Deploy With Compose

### First time

1. Clone this repo
   ```
   git clone <url>
   ```
2. Checkout the latest release branch `<branch>`.
   ```
   git checkout <branch>
   ```
3. Copy `docker-compose.docker.env.example` to `.env`
   ```
   cp -fv ./docker-compose.docker.env.example  ./.env
   ```
4. Edit the `.env` file as required
5. Create the directory you have configured as your `DATA_PATH`
   ```
   mkdir -p $(grep '^DATA_PATH=' .env | cut -d= -f2-)/postgresql
   ```
6. Start stack with `docker compose` or `podman compose`
   ```
   sudo docker compose -f ./docker-compose.docker.yml up
   ```

### Updating

To update, simply pull the latest changes from `<branch>` and run step 5 again.
As this is a single-commit branch, you can run this command below to always fetch the latest changes.

```
git fetch origin <branch> && git reset --hard FETCH_HEAD
```

It would be good to check from time-to-time if the `docker-compose.docker.env.example` has been updated with new config variables.
