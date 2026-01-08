# mbe_install : keep note on installation and change you makes

## usage

```bash
mbe_install <command>
```
## General Info

all commands are kept in ```$HOME/.config/mbe_install/mbe_install.history```
The format of the history file is the followinf : 
[command and parameters] # at=[datetime] user=[username] cwd=[working directory] backup_id=[identifier at the end of the backup file] patch=[name of the patch file with the changes]

## Editing a file
if the command is nano (or sudo nano), a backup of the file is made, and 
stored in the original directory

after editing, a patchfile is created to keep a readable, replayable 
history of the changes.

Replay history with 
'''bash
patch [file] < ~/.config/mbe_install/mbe_install_patches/[patchfile]
```
## Info or comment

The info command insert a comment in the history file. 

```bash
mbe_install info [Comments]
```

