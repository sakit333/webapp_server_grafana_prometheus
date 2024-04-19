# Install grafana in Master node
### https://grafana.com/grafana/download
```url
sudo yum install -y https://dl.grafana.com/enterprise/release/grafana-enterprise-10.4.2-1.x86_64.rpm
```
- reload daemon
```bash
sudo /bin/systemctl daemon-reload
```
```bash
 sudo /bin/systemctl enable grafana-server.service
```
```bash
sudo /bin/systemctl start grafana-server.service
```
--------------------------------------------------------------------------------------------------------
## connect with Grafana web terminal
```url
http://<master_public_ip>:3000
```
- **username** - admin
- **password** - admin
-----------------------------------------------------------------------------------------------------
## follow steps to create data source
- connections
- datasource
- select prometheus
### create data source
- connection -> prometheus server url --> http://<master_public_ip>:9090
- click save and test

### creating dashboard
- dashboard --> new --> import
- import JSOn file <Prometehus2.0stats.json>
- click on import
- Dashboard will start showing graphs
  
