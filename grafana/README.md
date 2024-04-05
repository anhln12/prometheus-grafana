# Run Grafana in Docker Container
```
docker run -d --name=grafana -p 3000:3000 grafana/grafana
```
# You need to mount the Docker Volume to store your persistent data and then bind it to a host port
```
docker run -d --name grafana -p 9000:3000 -v /opt/grafana-data:/var/lib/grafana grafana/grafana:8.3.0
```
# Use Docker volumes
```
docker volume create grafana-storage
docker run -d -p 3000:3000 --name=grafana --volume grafana-storage:/var/lib/grafana grafana/grafana:8.3.0
```
# Set User & Password
```
docker run -d --name grafana -p 9000:3000 -e GF_SECURITY_ADMIN_USER=admin -e GF_SECURITY_ADMIN_PASSWORD=Asim#2024qaz -v /opt/grafana-data:/var/lib/grafana grafana/grafana:8.3.0
```
# Plugin
```
docker run -d --name grafana -p 9000:3000 --user "$(id -u)" -e GF_SECURITY_ADMIN_USER=admin -e GF_SECURITY_ADMIN_PASSWORD=Asim#2024qaz -e "GF_INSTALL_PLUGINS=grafana-clock-panel, grafana-simple-json-datasource, grafana-worldmap-panel, grafana-piechart-panel" --volumn /opt/grafana-data:/var/lib/grafana grafana/grafana:8.3.0
```
# Reset passwd
```
docker exec -it <name of grafana container> grafana-cli admin reset-admin-password <fill in password>
```

**Refe:**

https://grafana.com/docs/grafana/latest/setup-grafana/installation/docker/

https://www.smarthomebeginner.com/grafana-docker-compose-guide/
