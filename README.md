![Moleculer logo](http://moleculer.services/images/banner.png)

[![Moleculer](https://badgen.net/badge/Powered%20by/Moleculer/0e83cd)](https://moleculer.services)

# kubernetes-demo
Kubernetes demo for Moleculer microservices framework

[For testing & prototyping install a Kubernetes cluster locally with Minikube.](INSTALL.md)

# Monolith mode
In this case all services executes in one Pod without transporter.

```bash
kubectl apply -f monolith.yaml
```
In browser open the http://192.168.99.100:30000 URL.


# Microservices mode
In this case all services executes in a separated and scaled Pod with NATS transporter.

```bash
kubectl apply -f monolith.yaml
```
In browser open the http://192.168.99.100:30000 URL.

## CLI connection
To connect to the deployed app install `moleculer-cli` & `nats` globally with `npm i -g moleculer-cli nats` command.

```bash
moleculer connect nats://192.168.99.100:32222
```

![Screenshot](https://user-images.githubusercontent.com/306521/59964682-fb981780-9503-11e9-8f56-6c66af244a13.png)

# License
Moleculer is available under the [MIT license](https://tldrlegal.com/license/mit-license).

# Contact
Copyright (c) 2016-2019 MoleculerJS

[![@moleculerjs](https://img.shields.io/badge/github-moleculerjs-green.svg)](https://github.com/moleculerjs) [![@MoleculerJS](https://img.shields.io/badge/twitter-MoleculerJS-blue.svg)](https://twitter.com/MoleculerJS)
