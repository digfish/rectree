# RECTREE
This a python application to survey and monitor the continuous changes in a directory tree. For those all of you that use local mirrors of some cloud storage service like Dropbox, Google Drive or Box, usually they provide an application that provides the synchronization between your local host and their cloud servers, usually they sit on the system tray notifying you of changes that occur after the last changes are made to put your local host in sync with the remote servers. The Dropbox app is bloated and occupies, for what it does, more than 100 MB in memory just to provide you with the synchronization and notification of the changes. I replace the Dropbox windows application with a 3rd party (in my case, GoodSync), which provides sync with multiple cloud storage providers. In this last case, the app just syncs and I needed an app that provided me with the notifications and a menu (on the system tray, obviously!) and a menu to quick access the most recent modified files.
I used the most beautiful language in the World, Python, of course, which give you all the tools you need with the most concise and few lines of code. In this, the ingredients where already there and I used:

- pysystray (for the system tray menu)
- watchdog (to monitor the dirtree changes)
- PySimpleGui (to build easyly and quickly UIs).

The final result was this:
![Systray Menu](img/rectree-menu.png)

The configurations are stored in an ini file in which you can configure the icon file, the polling interval, and one or more sections, eache one with the path of the directory being monitored, along with the number of items to display and an exclusions pattern, separated by "|". You can configure in a friendly way by choosing the config options on the menu.
There is no limit for the directories to monitor.

To get the package you can install it:

```
pip install rectree-digfish
```

And to execute it:
```
python -m rectree.rectree
```
