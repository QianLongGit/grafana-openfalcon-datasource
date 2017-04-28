# Open-Falcon plugin for Grafana

[Open-Falcon](https://github.com/open-falcon/falcon-plus) is an open-source, enterprise-level, and large-scale service monitoring system and time series database. It's initially released by Xiaomi SRE team in 2015 and heavily used in Xiaomi. Open-Falcon is now one of the most popular monitoring system in China internet companies.

# Installation

### Download prebuild version of grafana official site
[https://grafana.com/grafana/download](https://grafana.com/grafana/download) `Grafana v4.2`

**or you can install grafana via homebrerw:**

```
brew update 
brew install grafana
```

### Checkout the plugin
```shell
cd {GRAFANA_PATH_Installed}/data/plugins
git clone https://github.com/open-falcon/grafana-openfalcon-datasource

# 修正
cd /usr/share/grafana/public/app/plugins/datasource # ubuntu
sudo git clone https://github.com/open-falcon/grafana-openfalcon-datasource
sudo mv grafana-openfalcon-datasource fastweb-openfalcon-datasource
```

### Start grafana-server
```shell
{GRAFANA_PATH_Installed}/bin/grafana-server

# 修正
sudo service grafana-server start # http://docs.grafana.org/installation/debian/#start-the-server-init-d-service
```

## After Installation

If the installation is successful, Open-Falcon datasource would be shown as follow:
![](img/openfalcon_datasource.png)

## How to Set up datasource
* the backend services is provide by [falcon-plus](https://github.com/open-falcon/falcon-plus/tree/master/modules/api).

![](img/setup_grafana.png)
