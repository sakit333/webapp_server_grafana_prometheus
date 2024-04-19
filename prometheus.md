# To install Prometheus in Master node
```bash
wget https://github.com/prometheus/prometheus/releases/download/v2.51.2/prometheus-2.51.2.linux-amd64.tar.gz
```
- unzip
```bash
tar -zxvf prometheus-2.51.2.linux-amd64.tar.gz
```
- edit file
```bash
vi prometheus-2.51.2.linux-amd64/prometheus.yml
```
- edit to add target of tomcat server
```bash
static_configs:
  - targets ["tomcat_public_ip:8080"]
```
- to run prometheus file
```bash
sh prometheus-2.51.2.linux-amd64/prometheus
```
or
```bash
./prometheus
```
- connect with webbrowser
```url
http://<master_public_ip>:9090
```
- **username** - admin
- **password** - admin
