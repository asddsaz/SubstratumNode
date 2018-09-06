Ubuntu Install.md
----------------------

1. Install gdebi app:

'sudo apt install gdebi'
2. Download Substratum Node 0.4.0 GUI version for Ubuntu

Go to the official page https://substratum.net/open-beta

Locate and download SubstratumNode-v0.4.0-Linux64-deb.zip, which is around 40 MB. Note that the small link to binaries is probably not for you since it doesn't contain graphic user interface.
3. Unpack zip file

You get a deb file of the Node. Put in in your home folder, or any where you can find.
4. Install Substratum Node via gdebi

Open the GDebi Package Installer from app laucher. Click File -> Open, locate your .deb file, click Install Package, and wait until the installation is complete.

Now Substratum Node is installed to your system.
Second,

to make sure the Node runs properly, you may have to manually disable the service occupying port 53.

You can check if port 53 is occupied by running command ```ss -lntup```

To disable the service occupying port 53 on thr latest Ubuntu 18.04, do the following:
1. Run command

```sudo nano /etc/systemd/resolved.conf```

Append a new line in the text file ```- DNSStubListener=no```

Press key Ctrl-O, and then key ENTER to save the file, and then key Ctrl-X to exit.
2. Run commands

```sudo systemctl daemon-reload

sudo systemctl restart systemd-resolved.service
```
Finally,

run Substratum Node from app launcher
