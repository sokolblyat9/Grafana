# Grafana через Docker контейнер

### 1ая версия контейнера:

```
docker run -d --name=GRAFANA \
    -e "GF_PLUGINS_PREINSTALL=grafana-clock-panel, grafana-simple-json-datasource" \
    -e GF_DEFAULT_INSTANCE_NAME=Grafana_Continer \
    -e GF_SECURITY_ADMIN_USER=IlyaS \
    -e GF_SECURITY_ADMIN_PASSWORD=abobus \
    -v grafana-storage:/var/lib/grafana \
    -p 3000:3000 grafana/grafana:12.4.0-20977568970-ubuntu
```





<br><br/>
<br><br/>
<br><br/>

# Grafana на систему

<br><br/>
<br><br/>
<br><br/>
