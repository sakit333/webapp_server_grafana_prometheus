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
