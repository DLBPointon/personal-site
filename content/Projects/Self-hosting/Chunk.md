---
description:
title: Chunk
created: 20-06-2024
tags: [project, self-hosting, Y2024, docker]
date modified: 20-06-2024
---
As of May 2024, my wife's laptop had been out of use for a little while and so it was forfeit and now mine. Although as of June 2025 I am now planning for a more long term solution [[Unnamed NAS]] as having harddives attached by USB gives me some anxiety.

So, I now have a new homelab to take over from [[The-Vault]] and oh boy does it do so much more. Chunk is an Asus TUF F15 from 2019 or 2020, sometime before COVID19 anyway, an i5 9th or 10th gen which we upgraded from 8 to 16Gb (we can't play modded Minecraft and Gears on 8Gb after all).

Once again, I'll be using OpenMediaVault 6 (6.9.16-1 (Shaitan)). I think it is a nice bit of kit, it does everything I need to and with a nice looking UI too. Admittedly, it did take a couple of installs to get working correctly, however, these were very simple things that I forgot I would need to do coming to an x86 platform from arm. That was some humble pie.

Something I really like with OMV is that to move my media from the pi4 + 2 external HHD's to Chunk, all I had to do is plug them in and add them to the file system in the web GUI. Everything was there, just fantastic.

So I began setting up my services which has ended up as:

| Old Service | New Service               | Job                                                                                                             |
| ----------- | ------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Portainer   | OMV6 compose              | For container orchestration                                                                                     |
| Emby        | Jellyfin                  | Media Server                                                                                                    |
| Airsonic    | Black Candy               | Music and Podcast server                                                                                        |
|             | Audiobook Shelf           |                                                                                                                 |
| Kavita      | Kavita                    | Comic, Book and PDF viewer                                                                                      |
|             | Tailscale                 | VPN into home network                                                                                           |
|             | Postcodes.io              | A postcodes server, this is to help my wife and because I'm proving a point to a dev who is a thorn in my side. |
|             | GrampsWeb                 | Geneology Mapping                                                                                               |
|             | Paperles-NGX              | Document storage and ok OCR                                                                                     |
|             | Diun                      | Notify discord when there is an update for containers                                                           |
|             | Immich                    | Photo manager                                                                                                   |
|             | Homepage                  | A nice homepage for all my services                                                                             |
|             | Gluetun                   | General VPN                                                                                                     |
|             | NGinx Proxy Manager       | Making select services accessible outside the house.                                                            |

I also have some other containers which Arr quite interesting, for educational reasons of course.

Moving from a RPi4 to a gaming laptop was honestly like breathing fresh air for the first time. Everything was quicker, smoother and just better. It makes sense as the computers are like comparing apples to oranges.