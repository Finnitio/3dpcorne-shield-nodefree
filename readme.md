3d printed corne keyboard
==========================
![dashboard](3dpcorne.jpg)

this is my attempt to create a 3d printed split keyboard. I was intrigued to build an ergo mech split keyboard after seeing a yt video. My main goal was to learn to type with 10 fingers instead of using 3-4 fingers while constantly looking at my keyboard. I have succeeded. I am typing this on the above keyboard.

Reading into ergo mech keyboards i realised that i find the idea of the corne keyboard layout very interesting. I would summarize that you do not skip a key ro reach a key. Due to layers and modifiers it is not necessary to have more keys i think. For designing 3d models i use an extra numpad anyways. Other than that i don't miss any functionality. One goal was to keep it as cheap as possible, since i own a 3d printer it was cheaper to print it than having pcbs made. That is also the reason I went for nice!nano clones with zmk. I also wanted to have low profile keys to save overall buildheight. I found cheap gateron switches/hotswaps and the rest is easy to source from ali express.

After the first version was build i realised that i had to lift my wrists slightly to reach the upper row. After some reasearch I decided that something like the dactyl was a bit too much, especially when trying to keep the build height low. So i only angled the upper row upwards. I am very happy how it turned out! I basically don't need to move my wrists when typing.

build
==========================
The build is not too difficult. I have printed the parts in the natural orientation. After removing the support material, i drilled the holes for the hotswaps with a 3 mm bit. Cut the M3 threads with a tap. Depending on the printquality the hotswaps should hava a tight fit. I would suggest to use glue for the hotswaps, since a few came lose when I reattached the switches. Afterwards I soldered rigid wires to the columns and rows. Don't forget to add diodes downstream of each switch before connecting the columns with rigid wire. To insulate possible contact points i used heat shrink tube. Adding the switch and battery to the micro pro should be selfexplanatory. The connection for the microcontroller is the same for both sides. Columns and rows are connected to either side of the microcontroller seperately. The order of the columns is from top to bottom and the rows are ordered from the inside to the outside for each half. The keycaps that i used need to be cut on the under-/inside, I used a knife to cut chamfers into each keycap. Parts and links that i used:

- [2* NRF52840 Pro Micro](https://www.aliexpress.com/item/1005006035267231.html?spm=a2g0o.order_list.order_list_main.90.39655c5fdYkAzp) 14,68 €
- [1* Gateron HotSwaps](https://www.aliexpress.com/item/1005006364529726.html?spm=a2g0o.order_list.order_list_main.95.39655c5fdYkAzp) 10,68 €
- Gateron KS27 20,00 €
- [1* 1N4148 Diodes](https://www.aliexpress.com/item/1005006127068810.html?spm=a2g0o.order_list.order_list_main.135.39655c5fdYkAzp) 1,43 €
- [3* Keycaps](https://www.aliexpress.com/item/1005005305167568.html?spm=a2g0o.order_list.order_list_main.35.39655c5fdYkAzp) 11,46 € (not super happy with this since i had to cut chamfers and the profile could be lower. But I could not find cheap low profile kexcaps for the mx stem.)
- [1* Batteries 200 mAh](https://www.aliexpress.com/item/1005006284939857.html?spm=a2g0o.order_list.order_list_main.84.39655c5fdYkAzp) 2,87 €

that adds up to 41,12 €. Additionally you may add costs for 3d printing, screws, switches, rigid cable, soldering. So you can build one split keyboard for around 50 €.

![wiring](internals.jpg)

If somebody would like to create pcb's for this version of the corne keyboard, let me know! I would create a case that could mount the pcbs.

keymap
==========================

This is the keymap I am using. The basic layer is for writing with the german qwertz layout. I use urobs homerowmods and some other tweaks from him. The thump keys are for basic writing and entering the additional layers for symbols and navigation+numpad. The layers can be activated by holding the layer key, by taping the layerkey they become sticky and by double tapping you can toggle the layers on until you hit that key again.

![alt text](https://github.com/Finnitio/3dpcorne-shield-nodefree/blob/main/my_keymap.png?raw=true)

[keymap drawer by caksoylar](https://caksoylar.github.io/keymap-drawer?keymap_yaml=H4sIAAAAAAAC_81Wy3LiVhDd-ys6OIkmibAM-EmeWJYMYx4aJA8hEw8RIBsKCTGSGEIRskilsp5kqmaVqvxAFlnkC8KfzJfkSt0SkpFjZpcNpzn3dt9W92ld7YJcqVahUoeuYdozuBkaZh9mQ28AOrzUzakB5nBkwOKFNeqMjHnX1p1-EW4Mxxm6gjszjMlyZxdsBxa24w3sjqnP7alXhIU7MYcMPWdq8ODYM7cIBR56tjm1xsw-5MEbTK0uM_NLP4RrGDDwvIlbFIRbdv60u9ezLaGnj1x7buqOwE639Em27-gzwxG6pt0VLH04Fi6ldq2kdFRFEves_i4msEN57AAkM-_ZztjoOLane0afVsOcq6V240rrBJl3Ct8fdQp-GMNx_TB940afmkHELEiqGCA8QWghSAhNBA2hjXCFUEFoICgIq98D1EpnAS5YLiUeBkVoVepLiDg14EStWV1G3HnAqeWKrK1JOSBLVaLgAqEcbXic3OBTl2mBqiknrt5EqSWyD7JWFAzTqmhimda_QfgagQr3FAEfGOoItSgQx3M8MG1wn3Lrk7k9Iotx8ksi34uTWSI7MVJt14LkOE-fFMH1hr3RPL7sP_rmhiCOqE9caNlOH7c3JS1yq5ee1q_uDawqJVGK9p6pihjEO5eCgvYs270jqMcIlwnRkFpWPydUQ7WrxmsHqz_i1Y4rqpWiqHJKfytpQpDuKKqEcB5t0DYVVU8L1Ew5UU0K6sn9bZzfr4WYCjfEs3oTAI4BFhr1h9KU_1tM_z_duHMLZQOZLzJkPCeD_r796c9w5cPQ-Ocvsr4l4qNwZRka12RwGY6Y78Klz0Ljq0xSau8T_3G44QMyBIRHRC_C9WehwUWZ_Z3IfvM380O4dTc0ftx02fRbePOJUYQBu9XYheMXEN-Nnn17axrL-NawObBFA8b6y_HUSo4uhxV7-8uvoFyEZoDKBTNfrzOknXCMcIJwivBJsprhBJcbNYmCviJ8TfgbplHHYWSDEaV9sDmUh2lDeZQylJlsJjmWQjx3gjs_4SJPD5hDyCMUAsh8nkkJRLAekIfbtu7QPvu9YVe826XrOWgZzeR-bFRDLpfC5VO4Qgp3QBxlLOfw6WRspozNlE_vf8YtQM5h5eQDhEOEo5StZxqI1eaDESUFGrJMwfcJESj_woMx1t8cKd3webHWUDcWdthXXNe_5rLAXnLP8kyA-aNrtjRiDld-u01G09cV77_aeBovPrgfr0PH47hjQ2lv73nCPI_JUympmrS96ylzPSFXNgnv6M7mrxBzxlHdzpV9K-cTrq-2dmWFiqUsvpMvK9Vp0nf7lHP7PORy5C1fsnlk6nzY-19gXGvXgwwAAA%3D%3D)

Thanks
==========================
To the ergo mech keyboard community. Did not know keyboards could be that much fun!

- [caksoylar](https://github.com/caksoylar) for being very helfpfull setting up the zmk config for this board and for his great tool [keymap-drawer](https://github.com/caksoylar/keymap-drawer) that I used to create the graphics for the keymap.

- [urob](https://github.com/urob) for [node free config](https://github.com/urob/zmk-helpers) and his zmk config which was great to take some ideas from.

- [Joel Spadin](https://github.com/joelspadin) for [zmk locale generator](https://github.com/joelspadin/zmk-locale-generator) which made it possible to use the keyboard with windows locale set to german.

- [joric](https://github.com/joric) for his great [wiki](https://github.com/joric/nrfmicro/wiki/Alternatives) on the NRF52840 boards.

- The [zmk](https://zmk.dev/) Team & Community

- [www.keybr.com](https://www.keybr.com/) for being so great to learn typing with the keyboard.
