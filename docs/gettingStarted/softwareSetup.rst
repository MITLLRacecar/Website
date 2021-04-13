.. _software_setup:

RACECAR-MN Software Setup
============================================

This page will walk you through the steps needed to set up the operating system of a RACECAR-MN. You can view the full instructions `here <https://docs.google.com/document/d/1M99XklgR7pGS7_aW9fb94www9bNnznq7wxQn7z4suWw/edit>`_.

===========
Image Setup
===========

1. Download the latest version of the `image file <https://drive.google.com/file/d/1IHVibBQPwZXG4859diX54QEqpK2CyXrO/view?usp=sharing>`_.
2. Unzip the file (the extension should be ``.img`` not ``.gz``).
3. Find a computer that has an SD port, and plug in the micro-SD card in the SD adapter.

The operating system of your computer has will determine your next steps.

Linux
"""""

(These instructions have not been recently tested.)

1. Find the device name for your SD card. This can be done by using the ``lsblk`` command before and after plugging in the SD card; the new device is the card. It will look something like ``/dev/name``.
2. Unmount it with ``umount /dev/name_of_sd``.
3. Open a terminal and navigate to the folder containing your image (it is probably in downloads, so on a fresh terminal ``cd Downloads`` should work).
4. Finally, begin the copy process with ``sudo dd bs=1M if=name_of_image.img of=/dev/name_of_sd status=progress``. The image is 128 GB.

Mac
"""

Follow instructions `here <https://docs.google.com/document/d/1M99XklgR7pGS7_aW9fb94www9bNnznq7wxQn7z4suWw/edit#bookmark=id.54lelevfrxsl>`_.

Windows
"""""""
(This section has not been completed yet).


============
Router Setup
============

Creating an Account
"""""""""""""""""""

1. Once you plug in your router and turn it on, go into a browser and type into the address bar ``192.168.1.1``
2. This should present you with a login page, type in the default username and password for the router. If you are not sure, try "admin" for both.
3. Set a new username and password for the router login, and make sure to set a password for the Wi-Fi.

Connecting a RACECAR-MN
"""""""""""""""""""""""

For each car you want on this network, you must do the following:

1. On the car, connect to your newly created network.
2. Under network settings on the car, click the checkbox enabling the "allow for all users" connection option, this will ensure the car connects without needing you to login first.
3. Also make sure to tell the car to connect to your network automatically.
4. Once connected, type ``ifconfig``, find the entry for Wi-Fi (it should be "wlan0" or "wlo1" or something else starting with a w), and after that find a 12-digit alpha-numeric code delimited by colons (it should look like ``d0:53:7a:bf:01:a6`` or something similar, not ``ff:ff:ff:ff:ff:ff``). This is called the MAC address.
5. On the router’s online portal, navigate to the DHCP settings page.
6. Add a reserved address for the car of ``192.168.1.###`` where ``###`` is your chosen 3 digit car number. Put the MAC address mentioned before where prompted, and make sure you click enable and apply.
