cm-umts-yangtze
-----------------------------------------------------
This is the private porting of CyanogenMod 10.1 for "umts-yangtze". The "umts-yangtze" mentioned here is the 
code name for Motorola Razr V serials including XT885/XT887/XT889.
The initial code release is based on the official branch of CM for XT910 which has a same CPU and platform.
Basic test only performs on XT885. 


Setup the working tree:
-----------------------------------------------------
Step 1:
========
On local linux box (recommand uBuntu 12.04 LTS x64):
<working_folder> is a placeholder for a folder name for your cm-umts-yangtze repo.

    cd ~
    mkdir <working_folder>
    cd cm-umts-yangtze
    repo init -u https://github.com/gopise/cm-umts-yangtze-manifests -b master
    repo init -m cm-umts-yangtze.xml
    repo sync --no-clone-bundle

Then, wait...for a long time.

Step 2:
========
Type the following command:

    cd <working_folder>/bionic/libc/kernel/tools
    ./update_all.py

The linux header file for biolic will be updated.

Step 3:
========
Download a proprietary package (actually term.apk) from the following URL:
	https://github.com/gopise/cm-term
Uncompress and copy it to <working_folder>/vendor/cm/. Final folder structure might looked like:
	<working_folder>vendor/cm/proprietary/Term.apk
	<working_folder>vendor/cm/proprietary/...
Actually this is not a must, but you may need to change the makefile (vendor/cm/config/common.mk) if you don't need it.


Build the package:
-----------------------------------------------------
Type the following commands to start the build:

    cd <working_folder>
    . build/envsetup.sh
    brunch umts_yangtze

A ZIP package will be created under <working_folder>/out/target/product/umts_yangtze folder after a successful build.
