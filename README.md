cm-umts-yangtze
===============
This is the private porting of CyanogenMod 10.1 for "umts-yangtze". The "umts-yangtze" mentioned here is the 
code name for Motorola Razr V serials including XT885/XT887/XT889.
The initial code release is based on the official branch of CM for XT910 which has a same CPU and platform.
Basic test only performs on XT885.

CyanogenMod
===========

Submitting Patches
------------------
Patches are always welcome!  Please submit your patches via CyanogenMod Gerrit!
You can do this by using these commands:

    (From root android directory)
    . build/envsetup.sh
    (Go to repo you are patching, make your changes and commit)
    cmgerrit <for(new)/changes(patch set)> <branch/change-id> 

    repo start cm-10.1 .
    (Make your changes and commit)
    repo upload .
Note: "." meaning current directory
For more help on using this tool, use this command: repo help upload

Make your changes and commit with a detailed message, starting with what you are working with (i.e. vision: Update Kernel)
Commit your patches in a single commit. Squash multiple commit using this command: git rebase -i HEAD~<# of commits>

To view the status of your and others' patches, visit [CyanogenMod Code Review](http://review.cyanogenmod.org/)


Getting Started
---------------

To get started with Android/CyanogenMod, you'll need to get
familiar with [Git and Repo](http://source.android.com/source/using-repo.html).

To initialize your local repository using the CyanogenMod trees, use a command like this:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-10.1

Then to sync up:

    repo sync

Please see the [CyanogenMod Wiki](http://wiki.cyanogenmod.org/) for building instructions.

For more information on this Github Organization and how it is structured, 
please [read the wiki article](http://wiki.cyanogenmod.org/w/Github_Organization)

Buildbot
--------

All supported devices are built nightly and periodically as changes are committed to ensure the source trees remain buildable.

You can view the current build statuses at [CyanogenMod Jenkins](http://jenkins.cyanogenmod.org/)
