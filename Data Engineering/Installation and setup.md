---
tags:
  - docker
  - clickhouse
  - airbyte
  - data-engineering
  - visualization
created_at: 2024 September 1
updated_at: 2024 September 1
---
---
## Deploy Airbyte using docker

[Docker Compose Docs](https://docs.airbyte.com/deploying-airbyte/docker-compose)

[MSSQL Integration](https://docs.airbyte.com/integrations/sources/mssql)

[Clickhouse Integration](https://docs.airbyte.com/integrations/destinations/clickhouse)

[Debug link for port issue](https://github.com/airbytehq/airbyte/discussions/35451)

### Changes
1. Updated docker compose service called - airbyte_proxy (ports)
	 - "8020:8000"
      - "8021:8001"
      - "8022:8003"
      - "8023:8006"
  2. Updated .env basic auth credentials - Refer to the server for credentials
 
  
  3. http://100.64.100.247:8020/
  ---

## Deploy Clickhouse using docker

