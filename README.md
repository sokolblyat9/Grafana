# Grafana через Docker контейнер

### 1ая версия контейнера: Режим сети HOST

```
docker run -d --name=GRAFANA \
    -e "GF_PLUGINS_PREINSTALL=grafana-clock-panel, grafana-simple-json-datasource" \
    -e GF_DEFAULT_INSTANCE_NAME=Grafana_Continer \
    -e GF_SECURITY_ADMIN_USER=IlyaS \
    -e GF_SECURITY_ADMIN_PASSWORD=abobus \
    -v grafana-storage:/var/lib/grafana \
    -p 3000:3000 grafana/grafana:12.4.0-20977568970-ubuntu
```

## Рабочий конфиг с режимом сети HOST:

**Если нужно указать конкретный путь, где хочется расположить файлы Grafanы:**


```
docker run -d --name=GRAFANA \
    -e "GF_PLUGINS_PREINSTALL=grafana-clock-panel, grafana-simple-json-datasource" \
    -e GF_DEFAULT_INSTANCE_NAME=Grafana_Continer \
    -e GF_SECURITY_ADMIN_USER=IlyaS \
    -e GF_SECURITY_ADMIN_PASSWORD=abobus \
    -v /home/DU/DOKER/GRAFANA/grafana:/var/lib/grafana \
    -p 3000:3000 grafana/grafana:12.4.0-20977568970-ubuntu
```

Но после запуска кода, Grafana не встанет, в docker logs CONTAINER_ID будет сыпать ошибки!!


**скрин**


Для решения пока что перейти в папку:

cd /home/DU/DOKER/GRAFANA

chown 472:472 grafana/

Только после этого система запустится!

<br><br/>
<br><br/>
<br><br/>

# Grafana на систему

<br><br/>
<br><br/>
<br><br/>
