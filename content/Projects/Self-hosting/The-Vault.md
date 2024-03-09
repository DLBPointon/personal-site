---
title: The Vault
created: 09/03/2024
tags:
  - project
  - self-hosting
  - docker
---
This is my self-hosting pet project and has gone through two iterations so far. The first (OpenMediaVault 5 on a Raspberry Pi 4 4GB) just kinda died, it was shutdown for a while and when I went to wake it up... nothing. That was a _great_ morning. Thankfully nothing was lost and I was able to plug the external HHD into The Vault and everything was pretty much where I left it.

Anyhow, The Vault is a Raspberry Pi 4 (4GB) running OpenMediaVault 6. OMV is pretty good and I don't know if it would really be beneficial to switch to something like TrueNAS.
## Services
This Pi will also be running:

| Service   | Job                         | Port            |
| --------- | --------------------------- | --------------- |
| Portainer | For container orchestration | 9000            |
| ~~Plex~~* | For local media provision   | ~~32400~~       |
| Emby      | ""                       "" | 8123            |
| Airsonic  | Music and Podcast server    | 4040            |
| PiHole    | Advert blocking             | Not Yet Running |
| Kavita    | Comic, Book and PDF viewer  | 5000            |
*Plex* - hit the hay after hitting what appeared to be a limit on it's internal database, apparently a few thousand entries was it's limit. I have seen people with larger libraries though so i'm going to say this was the Pi's fault, especially after finding the same error with Jellyfin. Emby is a good replacement for now but, thanks for their need to try and promote their premium service, i'll be moving to Jellyfin when iteration 3 gets off the ground!
## Hardware
Nothing massively fancy here.

| Hardware               | Specs                                       |
| ---------------------- | ------------------------------------------- |
| Ice Tower              | Tower cooler for Pi                         |
| Raspberry Pi 4         | 4GB                                         |
| sd card                | 16gb                                        |
| Seagate external drive | 10TB                                        |
| WD external drive*     | 4TB                                         |
| Netgear Wifi Extender  | 5 Port 1GB extender use for all pi projects |
*WD Drive* is something like 14 years old at this point and still runs like an absolute champ. It will need replacing though, that's a bit too long for comfort.