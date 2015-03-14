#how to prepare micro SD card

# Prepare SD card #
You can use 2G or 4G micro SD card for Beagle Fly.
A PC runs Linux is needed to create sd card. The pc need have internet connection.
Beagle Fly uses Ubuntu 13.04 from **http://elinux.org/BeagleBoardUbuntu.**

Download the image from here.
**https://rcn-ee.net/deb/rootfs/raring/ubuntu-13.04-console-armhf-2013-09-26.tar.xz**

For more detailed instructions, please visit http://elinux.org/BeagleBoardUbuntu

Extract the file to a folder. Connect SD card to computer and open console window.
Switch to the folder and run the following command to check SD card name.


sudo ./setup\_sdcard.sh --probe-mmc

Then use the following command to write the data to SD card. Replace the sdX with the correct device name found in previous command.

sudo ./setup\_sdcard.sh --mmc /dev/sdX --uboot bone

Once the card is ready. Put the sd card to beaglebone black and power beaglebone. If everything is correct, you should be able to login beaglebone through ssh.

ssh ubuntu@192.168.1.16

The user name is Ubuntu. The password is temppwd

Connect the beaglebone with internet and login beaglebone.

I recommend update the image file first to get latest patches.

sudo apt-get update

sudo apt-get upgrade

Get Beaglefly file from.
```
wget https://beagle-fly.googlecode.com/files/v0.0.2.zip
```

Install unzip
```
sudo apt-get install unzip
```
Unzip the file
```
sudo unzip v0.0.2.zip
```

Rename it as "quad"
```
sudo mv v0.0.2 quad
```

Enter the quad foler
```
cd quad
```

Run following command.
```
sudo chmod +x *.sh -R
sudo ./setupQuad.sh
```

Now we have setup everything SD card!
The program will run automatically when beaglebone boot up!