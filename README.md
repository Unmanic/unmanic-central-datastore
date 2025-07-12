# Unmanic Central Datastore

Unmanic Central Datastore is the backend component of the Unmanic Central platform, designed to collect, store, and serve logs and metrics from all your Unmanic installations. It provides a secure, reliable storage layer that interfaces seamlessly with visualization tools such as Grafana.

## Architecture

- **Data Ingestion**  
  Each Unmanic instance pushes logs, scan results, and performance metrics to the Central Datastore via secure HTTP(S) endpoints.
- **Storage**  
  Incoming data imported and indexed depending on the data type.
- **API**  
  The Datastore exposes a RESTful API that supports querying time-series data and logs.

## Support

For all support, please join us on [Discord](https://streamingtech.co.nz/discord)

