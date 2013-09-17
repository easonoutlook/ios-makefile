# iOS Makefile
The universal makefile for my iOS projects distributes IPAs in seconds. (a.k.a. OTA makefile)


## Features
* Git log as release notes
* Shorten URL with my open source shortener: goo.gl
* QRCode of URL.
* Upload to SFTP via rsync -- ```make upload```
* Send emails with Mailgun -- ```make send_email```
* Local OTA server with __Bonjour__ -- ```make serve``` and ```make stop_serve```
* Send __iMessages__ to tester's iPhone -- ```make imessage```
* Show build settings -- ```make show_settings PRODUCT_SETTINGS_PATH``` or ```make show_settings | grep FLAG.*```

## Screenshots
![screen shot 2013-07-03 at 10 59 13 pm](https://f.cloud.github.com/assets/219689/744065/8faf92da-e3f4-11e2-9b97-889543a27fd4.png)


## Install

Download the __makefile__ and the config file __makefile.cfg__ into your project home folder:
```
curl -OL http://git.io/makefile
ls makefile.cfg 2>/dev/null >/dev/null||curl -OL http://git.io/makefile.cfg
```

Install [libqrencode](http://fukuchi.org/works/qrencode/) if you need the QRCode badge -- ```brew install qrencode```.

## How to use?

* Modify makefile.cfg to match your workspace settings.
* Make sure your build path is __relative to workspace__.
* ```make``` to build & package your IPA.
* ```make upload``` to upload the package to your SFTP server.
* or ```make serve``` to serve the IPA in your local network.
* ```make send_email``` will notify your QA team via Mailgun maillist.
* But I prefer spamming my buddies with iMessage ```make imessage```.

## Credits
iOS Makefile was fork from lexrus, modified this by eason.

## Contact
Follow [@easonoutlook on Twitter](https://twitter.com/easonoutlook)

## License
This code is distributed under the terms and conditions of the MIT license.
