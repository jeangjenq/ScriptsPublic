# ScriptsPublic
Scripts I write for different scenarios I encounter, often for bulk operation. Most of these are written in python but can utitlize other launguages.

## AutoHotkeys
### [mouseVolumeControl.ahk](./AutoHotkeys/mouseVolumeControl)
Assign mouse button1 and button2 to volume up/down. Hold button to continuously raise/lower volume.


## Python scripts
### [deleteReparsePoints.py](./deleteReparsePoints.py)
Windows 10 started creating reparse points on all OneDrive files/folders after a fall creator's update. It's part of the feature that breaks usage of that folder in mutliple OSs, an issue I described on my [website](http://www.jeangjenq.com/windows-10-delete-reparse-points-in-subdirectories/).

This scripts deletes all reparse points in OneDrive folders by looping fsutill command below on every single files/folder.
```batch
fsutil reparsepoint delete "C:\Path\To\Folder"
```

### [terminalLauncher.py](./terminalLauncher.py)
Launch terminal via python in different linux distros.

I realized since there's no such thing as default linux launcher, and my python code that requires to launch a terminal window doesn't always work on different linux distros. This python script loop through [list](https://github.com/i3/i3/blob/next/i3-sensible-terminal) of terminals and find out which terminal is available on the machine that runs it.

### [mkvRename.py](./mkvRename.py)
Batch rename MKV title to filename with the help of mkvpropedit

This scripts renames all the mkv files' title to its filename using [mkvpropedit](https://mkvtoolnix.download/doc/mkvpropedit.html)
```batch
mkvpropedit file -e info -s title
```

### [voicemeeter_macros.xml](./voicemeeter_macros.xml)
My [Voicemeeter Banana](https://www.vb-audio.com/Voicemeeter/banana.htm) macro buttons setup
