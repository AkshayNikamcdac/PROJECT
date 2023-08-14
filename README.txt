1. Divide packages among yourselves. Don't build packages marked as noarch

2. Do NOT build packages that are already provided (GCC, glibc, binutils). Check if package already exists within shared Fedora_RV64G_RPMS directory. A clear indicator would be the version in the NVRA naming scheme,for eg, 13.1 for gcc related packages, 2.37 on glibc related packages.

3. Follow the procedure to download the Fedora Rawhide image as shared on Github. Before booting though, make sure to resize the image. The current instructions are relevant on Fedora only, so one of you could boot into Fedora, resize the image to about 60GB, and share that image with everyone else.

4. After booting scp the Fedora_RV64G_RPMS directory to the image, and force update:

sudo rpm -Uvh --force *.rpm

5. Check gcc target with 

gcc -Q --help=target

6. Start building


You may want to initiate a screen session first before even booting the image.

Open terminal and execute screen 

$ screen 

Now under the session, boot the image and follow as instructed above.

While not necessary, it would advantageous in case you accidently close the terminal or terminal crashes.

You may check the functionality by closing the terminal, reopening it and executing :

$ screen -r

KEEP THE PC TURNED ON AT ALL TIMES DURING THE BUILD

TURN OFF SLEEP FROM SETTINGS

screen won't save you from a CPU going to sleep or turning off
