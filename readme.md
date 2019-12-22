# Linux cheat sheet

## System

![screenfetch](images/screenfetch.png)

I'm running [Ubuntu studio](https://ubuntustudio.org/) on a ThinkPad X201.

### Connect to eduroam

[Guide](https://www.sheffield.ac.uk/cics/wireless/linux)

### Hardware/software info

__List USB devices__

```
$ lsusb
```

__CPU info__

```
$ lscpu
```

__Memory info__

```
$ cat /proc/meminfo
```

__System monitor__

```
$ htop
```

__Check kernel version__

```
$ cat /proc/version
```

## Basic software
### Desktop environment
I use XFCE, that's shipped with Ubuntu Studio. Nothing fancy here.

### Email
I use [Geary](https://wiki.gnome.org/Apps/Geary) for my emails. It's quick and easy to set up, and talks to Gmail (which Thunderbird has had troubles with). To get Gmail up and running, you need to use [app-specific passwords](https://support.google.com/accounts/answer/185833?hl=sv).

## Audio

### KXStudio

Great resource for audio apps. [Link to their website](kx.studio).

### Reaper

Cockos are releasing experimental builds for Debian based systems (Ubuntu being one of them). 

[Link](http://reaper.fm/download.php).

Download the one called "Linux x86_64" (meaning that it's for a x86-based processor -- intel -- and in 64 bits).

### SuperCollider

SuperCollider can be downloaded through `apt`, via writing:

```
$ sudo apt install supercollider
```
