### This script emulates macOS single-instance on Linux.


When starting playback with this script, it will substitute an first running
instance of mpv. Other mpv instances are ignored.
Script takes filenames and options as arguments, and implement two special options:


`--blank`
>      Just open blank pseudo-gui window.
>      It will not write output to stdout/stderr, because this
>      will typically just fill ~/.xsession-errors with garbage.

`--add-playlist`
>      If mpv is already running, this option passed files to mpv's
>      internal playlist. If a file does not exist or is otherwise
>      not playable, mpv will skip the playlist entry when attempting
>      to play it (from the GUI perspective, it's silently ignored).


If mpv isn't running yet, this script will start mpv and let it control the
current terminal. mpv will terminate if there are no more files to play,
and running the impv script after that will start a new mpv instance.


>***Note*** that you can control the mpv instance by writing to the command fifo:
>
>      echo "cycle fullscreen" > ~/.config/mpv/.fifo
>
>***Note***:
> you can supply custom mpv path and options with the MPV environment variable.
> The environment variable will be split on whitespace, and the first item is used
> as path to mpv binary and the rest is passed as options _if_ the script starts mpv.
