# Borion
### Helps to use Steam-Proton as a normal wine

At first run, script ask you to specify a proton-directory path. It will be `steamapp` or your `localbuild`.

Also automatic creates wine prefix located in `~/.local/share/borion/wine-prefix`

WinApps user data (saves, confs) located out of prefix `~/.local/share/borion/user-appdata`

Run `borion --help` to see his extra options and how to use it.

Use .desktop files as tamplates for you custom launchers for individual games with individual params.

>***Note*** Script tries to do what a proton does without using the proton(py) and protonfixes itself.
> Since the script isn't fully ported, there may be gaps in the launch of some games or devices.
> Please write an Issue if you need port some special fixes from original proton script

# impv
### A minimal single-player instance for mpv

Use `impv` like normal `mpv` from command line or menu item.

Script pre-configured autofit for oversized and smaller video.

Also adds some extra options:

`--blank`
>      Opens an empty window.

`--add-to-playlist`
>      Append files in to current playlist.
>      If its empty, it will start with selected files.

>***Note*** Other MPV instances launched not through **impv** are completely ignored.

# How to Install

 1. clone this repository in to `you-directory`
 2. Create symlinks or copy scripts in to `~/.local/bin`
 3. Check if you `.profile` or `.bash_profile` contains an `PATH="$HOME/.local/bin:$PATH"`
 4. *Optional*: create symlinks or copy __applications/ .desktop__ files in to `~/.local/share/applications`
   for use borion from GUI menus.

---------------------------------------------------
##### Why Bash ?
 - Because Bash is a more suitable lang for working with files, folders, env-vars, run subprocess and pipes in a unix-like systems.


