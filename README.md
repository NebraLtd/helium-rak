# Helium RAK - Open Source Firmware for RAKwireless / MNTD Helium Miners

Balena OpenFleet for RAK v1.5, v2 and MNTD Miners

*Please note: this repo and the issues here are not monitored actively, so if you have an issue with this software we would ask that you email support@nebra.com or start an issue in our [main helium software repo](https://github.com/NebraLtd/helium-miner-software/issues). Please note that we do not provide support or feature requests for this free software at this time so this should only be used for bug reports.*

## How to use this firmware

There are two ways you can deploy this firmware to your RAKwireless / MNTD Helium Miner - either using the Balena Hub installation (which gives you auto-updates), or by forking the fleet and starting your own personal fleet (in this instance you will have direct control over your devices but will not get automatic updates).

### Balena Hub (preferred)

https://hub.balena.io/organizations/nebraltd/fleets/HELIUM-RAK

https://www.balena.io/etcher/

### Forking fleet


## Branches

In this repo there are two main branches:

* [master](https://github.com/NebraLtd/helium-rak/tree/master) - the main software branch with production tested docker-compose.yml.
* [testnet](https://github.com/NebraLtd/helium-rak/tree/testnet) - the testnet branch with bleeding-edge software. As this software can be untested and/or not working we do not recommend you use this in a production environment.
