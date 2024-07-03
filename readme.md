3d printed corne keyboard
==========================
![dashboard](3dpcorne.jpg)

this is my attempt to create a 3d printed split keyboard. I was intrigued to build an ergo mech split keyboard after seeing a yt video. My main goal was to learn to type with 10 fingers instead of using 3-4 fingers while constantly looking at my keyboard. I have succeeded. I am typing this on the above keyboard.

Reading into ergo mech keyboards i realised that i find the idea of the corne keyboard layout very interesting. I would summarize that you do not skip a key ro reach a key. Due to layers and modifiers it is not necessary to have more keys i think. For designing 3d models i use an extra numpad anyways. Other than that i don't miss any functionality. One goal was to keep it as cheap as possible, since i own a 3d printer it was cheaper to print it than having pcbs made. That is also the reason I went for nice!nano clones with zmk. I also wanted to have low profile keys to save overall buildheight. I found cheap gateron switches/hotswaps and the rest is easy to source from ali express.

After the first version was build i realised that i had to lift my wrists slightly to reach the upper row. After some reasearch I decided that something like the dactyl was a bit too much, especially when trying to keep the build height low. So i only angled the upper row upwards. I am very happy how it turned out! I basically don't need to move my wrists when typing.

build
==========================
The build is not too difficult. I have printed the parts in the natural orientation. After removing the support material, i drilled the holes for the hotswaps with a 3 mm bit. Cut the M3 threads with a tap. Depending on the printquality the hotswaps should hava a tight fit. I would suggest to use glue for the hotswaps, since a few came lose when I reattached the switches. Afterwards I soldered rigid wires to the columns and rows. Adding diodes downstream of each switch before connecting the column with rigid wire. To insulate possible contact points i used heat shrink tube. Adding the switch and battery to the micro pro should be selfexplanatory. The connection for the microcontroller is the same for both sides columns and rows are connected to either side of the microcontroller seperately. The order of the colmuns is top to bottom and the rows are ordered from the inside to the outside for each half. The keycaps that i used need to be cut on the underside, I used a knife to cut a chamfers for each keycaps. Parts and links that i used:

- [2* NRF52840 Pro Micro](https://www.aliexpress.com/item/1005006035267231.html?spm=a2g0o.order_list.order_list_main.90.39655c5fdYkAzp) 14,68 €
- [1* Gateron HotSwaps](https://www.aliexpress.com/item/1005006364529726.html?spm=a2g0o.order_list.order_list_main.95.39655c5fdYkAzp) 10,68 €
- Gateron KS27 20,00 €
- [1* 1N4148 Diodes](https://www.aliexpress.com/item/1005006127068810.html?spm=a2g0o.order_list.order_list_main.135.39655c5fdYkAzp) 1,43 €
- [3* Keycaps](https://www.aliexpress.com/item/1005005305167568.html?spm=a2g0o.order_list.order_list_main.35.39655c5fdYkAzp) 11,46 €
- [1* Batteries 200 mAh](https://www.aliexpress.com/item/1005006284939857.html?spm=a2g0o.order_list.order_list_main.84.39655c5fdYkAzp) 2,87 €

that adds up to 41,12 €. Additionally you may add costs for 3d printing, screws, switches, rigid cable, soldering. So you can build one split keyboard for around 50 €.

![wiring](internals.jpg)

If somebody would like to create pcb's for this version of the corne keybaord let me know! I would create a case that could mount the pcbs.

keymap
==========================

This is the keymap I am using. The basic layer is for writing with the german qwertz layout. I use urobs homerowmods and some other tweaks from him. The thump keys are for basic writing and entering the additional layers for symbols and navigation+numpad. The layers can be activated by holding the layer key, by taping the layerkey they become sticky and by double tapping you can toggle the layers on until you hit that key again.

![alt text](https://github.com/Finnitio/3dpcorne-shield-nodefree/blob/main/my_keymap.png?raw=true)

[keymap drawer by caksoylar](https://caksoylar.github.io/keymap-drawer?keymap_yaml=H4sIAAAAAAAC_51WzXLiRhC--yk6OIk2ibAM-Jf8yrKEWfOjWLIdsnGIABkoJMRKYlmKZQ855LxJqnJKVV4ghxzyBOs32SfJaHpGlrJarNoLX_NNfz09remWtkGrNxpQb0HPdrwF3I5tZwCLcTgCC55ZztwGZzyxYfXUnXQn9rLnWf6gCre2748DKVjY9my9tQ2eDyvPD0de17GW3jyswiqYOWOCoT-3RfC9RVCFigh9z5m7U2LvixCO5m6PmOV1FCKwbRiF4SyoStKQ7D_v7fQ9V-pbk8BbOpYvkd1da1Yc-NbC9qWe4_Uk1xpPpXO105T1rqGryo472MYEtlgeWwDpzPueP7W7vhdaoT1gqzznhtxpX5pdmnm38vygW4nC2H4QhRnYt9bcoRGLoBoKRfgW4RpBRbhAMBE6CJcIdYQ2go5w9ydFUz6huCK5yCKMqnBdb60h5gzKKeZFYx1zp5QzzuqaeU9qlJQbjIIawlns8DjtEFHnWYEaGTve_RGnlsqeZq3rGOa6bipnbP17hO8QWOGuEPDA0EJoxoEEURCB3A3hc-F-Z2GHkdUk-TUjP0iSRUZ2E6TRadLkgnDcnyzpeugNh46dcImO_38nxZoFcO35A_S7UM3YvyVftS43RjV0WVFj_xNDV6jLqUorGixdvFBQ-LHAjK-48RE3PuTGx9zYZsYP7P8nfGHNjRtuCNz4iRvfcOMLZtz9hfjm57_Zykvu8ikzJIRHjF7x9SfMEAoCY17_y6h3_RZecPHrf97l-ja9CpczuwojMp7I5IgKiJc8WWvY8Du1nk3nrNiCkIQ3v_wKeo2bFPUaMX-PV6_aDRTssEMeIhwhHCN8li4Zix71Dgv0iiEP_BtFEjzm-AbRVdl7u0X3s1r0IKNFC8VCukeljHOftZt4MZU2tp_aOk2uwy5CCaGMUKFQ-LKQETENeZ5YUnFLhnTQYwOWNgt2orCb6GHOlTK4cgZXyeD2hNTmWgmPpuFT1fCpascPHnATaCUsm7aHsI9wkOF6YoLSuHgwoqpDW9NY8F2GCCz_St7kVjmextByx9Nh-m3H30-b3nr5S8RmP73OSMgIBgJeRtDe7wHEfZd5f9nr5z3C3c_z-8Qfrif5kul55DOiCLMqPCmTRi4f3JDFCencyyiIQ2j2hSFGbwWRDawbLjlMStp6J4_miGgOmUaXDVPNIzomoiMmIvMjt5DMq0pChuPtIRH5IiynRK9yiEgpEgkqOVWkGMdpVZ4ES7silEpMp52TCUX6Nc_BonLsM11NbpIv7Nom2X_3DMMliAsAAA%3D%3D)

Thanks
==========================
To the ergo mech keyboard community. Did not know keyboards could be that much fun!

- [caksoylar](https://github.com/caksoylar) for being very helfpfull setting up the zmk config for this board and for his great tool [keymap-drawer](https://github.com/caksoylar/keymap-drawer) that I used to create the graphics for the keymap.

- [urob](https://github.com/urob) for [node free config](https://github.com/urob/zmk-helpers) and his zmk config which was great to take some ideas from.

- [Joel Spadin](https://github.com/joelspadin) for [zmk locale generator](https://github.com/joelspadin/zmk-locale-generator) which made it possible to use the keyboard with windows locale set to german.

- [joric](https://github.com/joric) for his great [wiki](https://github.com/joric/nrfmicro/wiki/Alternatives) on the NRF52840 boards.

- The [zmk](https://zmk.dev/) Team & Community

- [www.keybr.com](https://www.keybr.com/) for being so great to learn typing with the keyboard.
