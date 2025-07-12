# Unmanic Central Datastore

Unmanic Central Datastore is the backend component of the Unmanic Central platform, designed to collect, store, and serve logs and metrics from all your Unmanic installations. It provides a secure, reliable storage layer that interfaces seamlessly with visualization tools such as Grafana.

## Architecture

- **Data Ingestion**  
  Each Unmanic instance pushes logs, scan results, and performance metrics to the Central Datastore via secure HTTP(S) endpoints.
- **Storage**  
  Incoming data imported and indexed depending on the data type.
- **API**  
  The Datastore exposes a RESTful API that supports querying time-series data and logs.
- **Frontend**  
  A web-based UI available at https://central.unmanic.app/ provides dashboards, configuration screens, and visualizations of your collected data.

## Deploy With Compose

### First time

1. Clone this repo
2. Checkout the latest release branch `release/latest`.
   ```
   git checkout release/latest
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

To update, simply pull the latest changes from `release/latest` and run step 5 again.
As this is a single-commit branch, you can run this command below to always fetch the latest changes.

```
git fetch origin release/latest && git reset --hard FETCH_HEAD
```

It would be good to check from time-to-time if the `docker-compose.docker.env.example` has been updated with new config variables.

## Support

For all support, please join us on [Discord](https://streamingtech.co.nz/discord)

