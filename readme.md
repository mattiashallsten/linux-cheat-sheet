# Linux cheat sheet

## System

![screenfetch](images/screenfetch.png)

```
[?25l[?7l[0m[31m[1m            .-/+oossssoo+/-. 
        `:+ssssssssssssssssss+:` 
      -+ssssssssssssssssssyyssss+- 
    .ossssssssssssssssss[37m[0m[1mdMMMNy[0m[31m[1msssso. 
   /sssssssssss[37m[0m[1mhdmmNNmmyNMMMMh[0m[31m[1mssssss/ 
  +sssssssss[37m[0m[1mhm[0m[31m[1myd[37m[0m[1mMMMMMMMNddddy[0m[31m[1mssssssss+ 
 /ssssssss[37m[0m[1mhNMMM[0m[31m[1myh[37m[0m[1mhyyyyhmNMMMNh[0m[31m[1mssssssss/ 
.ssssssss[37m[0m[1mdMMMNh[0m[31m[1mssssssssss[37m[0m[1mhNMMMd[0m[31m[1mssssssss. 
+ssss[37m[0m[1mhhhyNMMNy[0m[31m[1mssssssssssss[37m[0m[1myNMMMy[0m[31m[1msssssss+ 
oss[37m[0m[1myNMMMNyMMh[0m[31m[1mssssssssssssss[37m[0m[1mhmmmh[0m[31m[1mssssssso 
oss[37m[0m[1myNMMMNyMMh[0m[31m[1msssssssssssssshmmmh[0m[31m[1mssssssso 
+ssss[37m[0m[1mhhhyNMMNy[0m[31m[1mssssssssssss[37m[0m[1myNMMMy[0m[31m[1msssssss+ 
.ssssssss[37m[0m[1mdMMMNh[0m[31m[1mssssssssss[37m[0m[1mhNMMMd[0m[31m[1mssssssss. 
 /ssssssss[37m[0m[1mhNMMM[0m[31m[1myh[37m[0m[1mhyyyyhdNMMMNh[0m[31m[1mssssssss/ 
  +sssssssss[37m[0m[1mdm[0m[31m[1myd[37m[0m[1mMMMMMMMMddddy[0m[31m[1mssssssss+ 
   /sssssssssss[37m[0m[1mhdmNNNNmyNMMMMh[0m[31m[1mssssss/ 
    .ossssssssssssssssss[37m[0m[1mdMMMNy[0m[31m[1msssso. 
      -+sssssssssssssssss[37m[0m[1myyy[0m[31m[1mssss+- 
        `:+ssssssssssssssssss+:` 
            .-/+oossssoo+/-. 
[20A[9999999D[43C[0m[1m[0m[31m[1mmattias@[0m[31m[1mm-tp[0m 
[43C[0m------------[0m 
[43C[0m[31m[1mOS[0m[0m:[0m Ubuntu 18.04.3 LTS x86_64[0m 
[43C[0m[31m[1mHost[0m[0m:[0m 3680WB5 ThinkPad X201[0m 
[43C[0m[31m[1mKernel[0m[0m:[0m 4.15.0-72-lowlatency[0m 
[43C[0m[31m[1mUptime[0m[0m:[0m 5 hours, 27 mins[0m 
[43C[0m[31m[1mPackages[0m[0m:[0m 2941[0m 
[43C[0m[31m[1mShell[0m[0m:[0m bash 4.4.20[0m 
[43C[0m[31m[1mResolution[0m[0m:[0m 1280x800[0m 
[43C[0m[31m[1mDE[0m[0m:[0m Xfce[0m 
[43C[0m[31m[1mWM[0m[0m:[0m Xfwm4[0m 
[43C[0m[31m[1mWM Theme[0m[0m:[0m Xfce-Simple-Dark[0m 
[43C[0m[31m[1mTheme[0m[0m:[0m Arc [GTK2], NumixBlue [GTK3][0m 
[43C[0m[31m[1mIcons[0m[0m:[0m Tela [GTK2], Elementary-xfce-darker [GTK3][0m 
[43C[0m[31m[1mTerminal[0m[0m:[0m panel-1-whisker[0m 
[43C[0m[31m[1mCPU[0m[0m:[0m Intel i5 M 520 (4) @ 2.400GHz[0m 
[43C[0m[31m[1mGPU[0m[0m:[0m Intel Ironlake Mobile[0m 
[43C[0m[31m[1mMemory[0m[0m:[0m 3169MiB / 7772MiB[0m 

[43C[0m[30m[40m   [0m[31m[41m   [0m[32m[42m   [0m[33m[43m   [0m[34m[44m   [0m[35m[45m   [0m[36m[46m   [0m[37m[47m   [0m


[?25h[?7h
```

I'm running [Ubuntu studio](https://ubuntustudio.org/) on a ThinkPad X201.

Ubuntu Studio comes with a bunch of audio software, like [Pure Data](https://puredata.info/), [Ardour](https://ardour.org/) and many more. 

The feature that got me interested, though, was that it ships with a low-latency kernel.

### Connect to eduroam

Super important for me, du to studying at a university. 

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

Great resource for audio apps. [Link to their website](https://kx.studio/).

To install on Debian/Ubuntu, follow these steps to add their repositories to `apt`:

```
$ sudo apt-get install apt-transport-https gpgv
$ sudo dpkg --purge kxstudio-repos-gcc5
$ wget https://launchpad.net/~kxstudio-debian/+archive/kxstudio/+files/kxstudio-repos_10.0.3_all.deb
$ sudo dpkg -i kxstudio-repos_10.0.3_all.deb
```

Then, run: 

```
$ sudo apt update
```

...and you should be able to find the packages in the Synaptic Package manager (a GUI frontend to `apt`).

In the Synaptic Package manager, you can sort the packages by repository in the lower left corner.

On of the packages is called `kxstudio-recommended-all`, which is what the name suggests. I also recommend these packages from KXStudios:

__Cadence__, a `jackd` frontend, that makes everything easier.

__Carla__, an audio plug-in host.

But there's a bunch of other stuff there.

### Reaper

Cockos are releasing experimental builds for Debian based systems (Ubuntu being one of them). 

[Link](http://reaper.fm/download.php).

Download the one called "Linux x86_64" (meaning that it's for a x86-based processor -- intel -- and in 64 bits). 

Unzip the file, and then open a terminal and go into the unzipped directory with the `cd` command. Inside the directory, run the command:

```
$ sh install-reaper.sh
```

...and you'll be prompted a couple of things. It's pretty straightforward. I've installed it locally (in the ~/opt/ repository) but I don't think it makes a difference if you install it globally (in the /opt/ repository).

I do recommend starting a Jack server before you start Reaper, though.

### SuperCollider

SuperCollider can be downloaded through `apt`, via writing:

```
$ sudo apt install supercollider
```
