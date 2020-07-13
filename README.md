### This is a minimal single-player implementation for \*nix using only the built-in MPV features.


>***Note*** Other MPV instances launched not through **impv** are completely ignored.


You can use `impv` instead of the `mpv` from command line and .desktop shortcuts.
It can takes any options and supported files / protocols same as original `mpv` program.


#### `impv` features:


Play's video with a single player instance.
 - If window holded `ontop` or expanded to the fullscreen, player just update playback.
 - If not - player restarts with new params, for pop up himself above other windows.


Configured autofit params for smaller and larger video.


Implements some special options:

`--blank`
>      Just opens a blank window for drag and drop from file manager.

`--add-to-playlist`
>      This option append files to mpv's internal playlist.
>      If MPV is not running, it will start with selected files.


As well, you can add `impv-playlist.desktop` file to `/usr/local/share/applications`
 (for all users) or `~/.local/share/applications` (for personal usage), and set it as
 **Recommended Application** for add files and folders to playlist from context menu.


>
> **Script written in Python (> = 3.4) and implements an IPC-client for communicating with MPV via JSON API.**
>
