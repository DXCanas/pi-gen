# Kolibri pi-gen adaptation



## Using Rasbperry Pi Kolibri image

1. Download the zip file from the releases page
2. Use any of the method explained at https://www.raspberrypi.org/documentation/installation/installing-images/README.md to write the image to a SD card (If using Linux, `unzip -p image_2019-12-01-Kolibri-lite.zip| dd of=/dev/sdb bs=4M conv=fsync` is the fastest method, supposing your SD card is in `/dev/sdb`)
3. Insert the SD card in the Raspberry PI
4. Power on the Rasperry Pi and wait ( The process takes less than 5 minutes in a model 4. Depending on the model it can take longer)
5. Enjoy it!



After following the above steps the Raspberry Pi will provide a wifi network named under the essid `kolibri` without any password.

After connecting a device to this wifi network provided by the Raspberry, you can open the url http://10.10.10.10 in a browser will allow you enjoy all the features of a working Kolibri server.

By default the server does not have Internet access, so an usb disk must be used to add content channels to Kolibri.

In case you want to login into the server, the user is `pi` and the password is `kolibrifly`

**VERY IMPORTANT NOTICE**: After installing the image, a ssh server is installed with a known password. **CHANGE IT** in case you want to connect it to Internet or be used by people who could mess it up.



The installed system contains a fully Raspbian image, with all the software included in the `lite` version from https://www.raspberrypi.org/downloads/raspbian/ . After login `sudo raspi-config` can be used to customize its environment, including localization, timezone, etc. if desired.



## Future steps

Using the `raspi-config` script we'll

- Add options to let it route to Internet

- Add options to change the wifi essid

- Add options to change wifi between 802.11g & 802.11ac (only g currently)

- Add options to make the wifi encrypted



## Rebuilding the Kolibri Raspberry Pi image
