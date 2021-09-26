# Vagrantbox Minikube/Grafana/Loki

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Prerequisites
* Vagrant - https://www.vagrantup.com/downloads
* Virtualbox - https://www.virtualbox.org/wiki/Downloads

## How to use?

1. Clone https://github.com/spy86/minikube-grafana-loki
2. Run `vagrant up` from terminal and wait while virtual machine is installed.
3. Add the following line to the hosts file `192.168.123.123 grafana.minikube.local`
4. Get Login
```
kubectl get secret -n loki loki-grafana -o jsonpath="{.data.admin-user}" | base64 --decode ; echo
```
5. Get Password
```
kubectl get secret -n loki loki-grafana -o jsonpath="{.data.admin-password}" | base64 --decode ; echo
```
6. Open http://grafana.minikube.local in web browser and type login/password from above
7. Import two dashboards ID: (12611 and 12019)
