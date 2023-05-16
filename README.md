## Ansible Install and configure

- sudo apt install git python3-pip
- pip3 install ansible

- sudo cp /etc/profile ~/.profile
- sudo nano ~/.profile
- add to the end of file: export PATH="/home/{user}/.local/bin:$PATH"
- echo $PATH

- ansible --version


### Docs

- https://www.cloudbooklet.com/how-to-install-php-fpm-with-apache-on-ubuntu-22-04/


## Node exporter, Prometheus and Grafana

- Install Node exporter https://prometheus.io/docs/guides/node-exporter/
- wget https://github.com/prometheus/node_exporter/releases/download/v1.5.0/node_exporter-1.5.0.linux-amd64.tar.gz

## Docker Compose

- https://docs.docker.com/compose/install/standalone/

## K6
- https://k6.io/docs/get-started/installation/
- k6 run --vus 100 --duration 30s script.js

## Grafana
- https://grafana.com/grafana/dashboards/1860-node-exporter-full/


