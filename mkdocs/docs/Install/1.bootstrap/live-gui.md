# Gentoo Live GUI


## Seting up a Bootable USB Stick

Since nobody uses CD's anymore these days the first step is to setup a bootable USB Stick
One of the easiest ways to do this is to use the **LiveGUI USB Image**

  * https://www.gentoo.org/downloads/

In order to write the iso to a USB Stick there are a few different ways to do this

  * [Rufus](https://rufus.ie/en/) is one way
  * Another is the [Universal USB Installer](https://pendrivelinux.com/universal-usb-installer-easy-as-1-2-3/)

The boot menu on a reboot can be brought up by pressing F7 on this board
This can be used to select which device to boot from

## Setting up SSH

Next to give the root user a password
```bash
sudo passwd
# Enter new password for root
```

To enable the ssh server
```
/etc/init.d/sshd start
```

From this point onwwards we can now remotely ssh into the live environment
and continue the setup from a ssh client.

One recomendation I would suggest if using Windows is Kitty
Which is basically putty but with some additional features

  * https://www.9bis.net/kitty/index.html#!index.md