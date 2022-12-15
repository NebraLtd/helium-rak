# Helium RAK - Open Source Firmware for RAKwireless / MNTD Helium Miners

Balena OpenFleet for RAK v1.5, v2 and MNTD Miners

**Key features:**

- local IP diagnostics dashboard
- updated regularly (our automated system means this will get updates at the same time as the entire Nebra fleet)
- automatic updates (if installed via [balenaHub](#balena-hub-installation-preferred---includes-auto-updates)) or option to fork and manage your own fleet
- powered by [balenaOS](https://balena.io/os) which is optimised for edge devices and very secure
- access to new features as added to the core Nebra software
- fully open source software stack (the only one in the Helium community!)
- COMING SOON: access to [remote management dashboard](https://dashboard.nebra.com) (paid extra)

**Please note: this repo and the [issues section](https://github.com/NebraLtd/helium-rak/issues) here are not monitored actively, so if you have an issue with this software we would ask that you email [support@nebra.com](mailto:support@nebra.com) or start an issue in our [main helium software repo](https://github.com/NebraLtd/helium-miner-software/issues). We do not provide support or feature requests for this free software at this time so this should only be used for bug reports.**

## How to use this firmware

There are two ways you can deploy this firmware to your RAKwireless / MNTD Helium Miner - [either using the Balena Hub installation](#balena-hub-installation-preferred---includes-auto-updates) (which gives you auto-updates), or by [forking the fleet and starting your own personal fleet](#forking-fleet-installation-requires-updating-manually--setting-up-own-automations) (in this instance you will have direct control over your devices but will not get automatic updates).

#### What you will need

- microSD card reader for laptop/computer
- OS image file specifically of your RAK or MNTD Hotspot (link in step 4 below)
- computer or laptop (Windows or Mac)
- RAK v1.5, v2 or MNTD Hotspot

**Do not follow this guide if you have a different manufacturer of hotspot**

### Balena Hub Installation (preferred - includes auto-updates)

**Step 1** - First of all you will need to remove the current microSD card that is inserted into your RAK Hotspot miner. You will need to follow [the instructions from RAK wireless](https://support.getmntd.com/hc/en-us/articles/6832177438999-Replacing-the-SD-card) in order to see how to do this. Here is a quick video to show you how to remove the microSD card (skip to 3:21):

[![RAK microSD access video](https://img.youtube.com/vi/CzMwnpkjob4/0.jpg)](https://www.youtube.com/watch?v=CzMwnpkjob4&t=201)

**Step 2** - Insert the microSD card either into an SD adaptor or if your memory card reader takes microSD directly then insert that and connect it to your computer or laptop.

![microSD card and SD size adaptor](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/24118876135/original/MArAqX-4wpkD-tNIMPj99bvek0W9iYxlDA.jpg?1656517242)

![SD to USB-C adapter](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/24118876190/original/mGpbmAEFF4L57-h-iFGePZmYIjccEdC3zw.jpg?1656517265)

**Step 3** - On your computer download and install Balena Etcher from - https://www.balena.io/etcher/

![balenaEtcher website screenshot](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/24118876349/original/OQRatg5WEfyNCaNeAxRyhEeApg-xsujp5g.png?1656517382)

Once downloaded go ahead and open up the balenaEtcher program on your computer or laptop.

![balenaEtcher application](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/24118876425/original/ce_O3wGulB3CeKAwRnlpzZ4DTQ4fxxpTkw.png?1656517437)

**Step 4** - Before we move to the next step you will need to download the latest OpenFleet software for your hotspot from balenaHub, which you can find here - https://nebra.io/rak

Click on the link and you will be redirected to the balenaHub page for your hotspot. Click on `Get Started` and select your preferred network connection (Ethernet required on first boot). If you have balenaEtcher already installed you can select Flash, otherwise you can select Download from the drop-down box by clicking the arrow.

**Important: do not click on `Fork this fleet`**

![balenaHub page for Helium RAK](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/24118876816/original/zCffeV40Wq9Xr2erSSSr_u8B3r--purIOQ.png?1656517776)

![Add new device popup screen on balenaHub](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/24118876877/original/LjeNNTCDF7Vs5ngRDS1WZd_qj2Mv0zARMQ.png?1656517851)

**Step 5** - Click on the `Flash from file` button in balenaEtcher and navigate to where you saved your downloaded firmware file. Select it to be installed.

In the middle section of balenaEtcher click `Select target` to select your SD card to install the OS (it may be selected automatically).

![Select a drive popup on balenaEtcher application](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/24118877083/original/0pbHblepnrSaHlkBgJpjmg5xgui03PvYIQ.png?1656518092)

Finally, click on the `Flash!` button to begin installing the firmware to your microSD card (you may need to type your login password here).

**Step 6** - Once it has finished you can now remove the SD card from its adaptor and card reader and then insert it back into the RAK or MNTD hotspot.

**Step 7** - Finally, connect your Ethernet cabe to the hotspot and then the power cable. The hotspot should now boot up with your new firmware installed. It may take up to 30 minutes to do all the updates.

**Note: We recommend that you use Ethernet for the first boot of the hotspot, at which point you can configure WiFi using the hotspot app.**

This guide is also available [on our support site here](https://support.nebra.com/support/solutions/articles/24000078640-getting-started-with-rak-mntd).

### Forking Fleet Installation (requires updating manually / setting up own automations)

[![balena deploy button](https://www.balena.io/deploy.svg)](https://dashboard.balena-cloud.com/deploy?repoUrl=https://github.com/NebraLtd/helium-rak)

## Branches

In this repo there are two main branches:

* [master](https://github.com/NebraLtd/helium-rak/tree/master) - the main software branch with production tested docker-compose.yml.
* [testnet](https://github.com/NebraLtd/helium-rak/tree/testnet) - the testnet branch with bleeding-edge software. As this software can be untested and/or not working we do not recommend you use this in a production environment.
