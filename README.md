[![][License img]][License]

<a href="http://ami-ecosystem.in2p3.fr/" target="_blank">
	<img src="./assets/logo.svg" alt="AMI" height="64" />
</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href="http://lpsc.in2p3.fr/" target="_blank">
	<img src="./assets/logo-lpsc.svg" alt="LPSC" height="72" />
</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href="http://www.in2p3.fr/" target="_blank">
	<img src="./assets/logo-in2p3.svg" alt="IN2P3" height="72" />
</a>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<a href="http://www.univ-grenoble-alpes.fr/" target="_blank">
	<img src="./assets/logo-uga.svg" alt="UGA" height="72" />
</a>

AMI Full Stack Demo
===================

This is a "docker-compose"-based demo of the full AMI ecosystem. It was originally developed for the A Toroidal LHC ApparatuS (ATLAS) experiment, one of the two general-purpose detectors at the Large Hadron Collider (LHC).

Usage
-----

Make sure that `git` and `Docker Compose V2` are installed.

```bash
docker compose version
```
For Linux installation, create the `docker` group if it doesn't exist and add the current user to it (refer to [Docker documentation](https://docs.docker.com/engine/install/linux-postinstall/)).

```bash
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker
```

Then pull the AMI demo from Git and launch it.

```bash
git clone https://github.com/ami-team/AMIDemo.git
cd AMIDemo
docker compose up
```
Endpoints
---------

Web interfaces:
  - Metadata interfaces: http://localhost:667/ (username: admin, password demo) or (username: user, password demo)
  - Pipeline interfaces: http://localhost:664/
  - phpMyAdmin interfaces: http://localhost:661/ (username: root, password root)

Web service:
  - `http://localhost:666/AMI/FrontEnd`

MQTT service:
  - `ws://localhost:663/ws`

Issuer/Token
------------

JWT issuer for demo:
  - `AMI-Demo`

JWT secret for demo:
  - `jNAvEVLbgnjYqT8E`

JWT token for demo:
  - `eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJBTUktRGVtbyIsImlzcyI6IkFNSS1EZW1vIn0.WZ7Xs4WhO9QRL4D_vUSozyOesBbDNcnYEnfBqnPobzJKWwousQc_bhyVsgITFJ0ypxHzb4KnVg73X68qYI5ZOg`

Developers
----------

* [Jérôme ODIER](https://annuaire.in2p3.fr/4121-4467/jerome-odier) ([CNRS/LPSC](http://lpsc.in2p3.fr/))
* [Fabian Lambert](https://annuaire.in2p3.fr/3087-3350/fabian-lambert) ([CNRS/LPSC](http://lpsc.in2p3.fr/))

[License]:http://www.cecill.info/licences/Licence_CeCILL_V2.1-en.txt
[License img]:https://img.shields.io/badge/license-CeCILL-blue.svg
