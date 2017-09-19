# Raspberry Pi Zero W Setup

### 1. Download and extract Raspbian image. The resulting file should have a .img extension, not .zip

Download Raspbian here:
https://www.raspberrypi.org/downloads/raspbian/

### 2. Download SD card formatter and overwrite format your SD card.

Download SD Card Formatter here:
https://www.sdcard.org/downloads/formatter_4/

### 3. Wait for raspbian to download and for SD card to format. When both are done, time to write the raspbian image to the SD card. You can use either Pi Filler (OSX only) or Etcher (OSX and WIN).

Download Pi Filler here:
http://ivanx.com/raspberrypi/

--or--

Download Etcher here:
https://etcher.io/

### 4. Put SD card into the Raspberry Pi. Attach a screen, keyboard and a mouse and let it boot to the desktop.

### 5. When desktop is up, click on the network manager icon in upper right. Select the __*ph0t0n*__ (with zeros) network. The password is __*8characters*__.

### 6. Open the terminal with the term icon in the upper left. At the shell prompt, enter the command __*ifconfig*__.

### 7. Look for the listing for __*wlan0*__, which is the wireless interface. Write down the IP address that comes after __*inet*__. It should be something like 192.168.###.### You will connect to this address via SSH from the terminal on your laptop in the next step.

### 8. From the Pi's terminal, issue the command __*sudo raspi-config*__ Use the up/down arrow keys to select option 5, __*Interfacing Options*__, then select option P2, __*SSH*__. Answer __*YES*__ to the question: Would you like the SSH server to be enabled? Use tab to select finish. Enter to exit.

### 9. Issue the command __*sudo shutdown now*__. The raspberry pi will shut down, disconnect screen, keyboard and mouse. Reconnect to power near your laptop.

### 10. Connect your laptop to the __*ph0t0n*__ network, again, the password is __*8characters*__. Search for __*terminal*__ in spotlight (OSX), or download a SSH client (WIN) like PuTTY from http://www.putty.org/.

### 11. In the terminal on your laptop, issue the command __*ssh pi@192.168.###.###*__, where the ###.### are the numbers in your IP address you wrote down earlier. Answer __*YES*__ to the question: Are you sure you want to continue connecting (yes/no)?

### 12. pi is the username you are logging in with. The default password for the pi user is __*raspberry*__.

### 13. You will be greeted with the following:

Linux raspberrypi 4.9.41+ #1023 Tue Aug 8 15:47:12 BST 2017 armv6l

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Tue Sep 19 16:18:57 2017

SSH is enabled and the default password for the 'pi' user has not been changed.
This is a security risk - please login as the 'pi' user and type 'passwd' to set a new password.

pi@raspberrypi:~ $

You're in!!!
