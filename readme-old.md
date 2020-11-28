# Linux cheat sheet
<!-- markdown-toc start - Don't edit this section. Run M-x markdown-toc-refresh-toc -->
**Table of Contents**

- [System](#system)
  - [Apt](#apt)
  - [Synaptic package manager](#synaptic-package-manager)
  - [Connect to eduroam](#connect-to-eduroam)
  - [Hardware/software info](#hardwaresoftware-info)
- [Basic software](#basic-software)
  - [Desktop environment](#desktop-environment)
  - [Email](#email)
  - [Music player](#music-player)
- [Audio](#audio)
  - [KXStudio](#kxstudio)
  - [Reaper](#reaper)
  - [SuperCollider](#supercollider)

<!-- markdown-toc end -->

## System

![screenfetch](images/screenfetch.png)

I'm running [Ubuntu studio](https://ubuntustudio.org/) on a ThinkPad X201.

Ubuntu Studio comes with a bunch of audio software, like [Pure Data](https://puredata.info/), [Ardour](https://ardour.org/) and many more. 

The feature that got me interested, though, was that it ships with a low-latency kernel.

### Apt
`apt` is the package manager for Debian-based systems (Ubuntu being one of them). To install most software, the user types: 

```
$ sudo apt install <name-of-package>
```

The "sudo" part is to run the command as root, so the user will be prompted to input their password.

If the user wants to add other software than is supported on the standard repositories (the Ubuntu servers), the user can use the command `apt-add-repository`. Often times when you search for a piece of software for Ubuntu on a web browser, you'll find a website for that repository -- then you usually do this:

```
$ sudo apt-add-repository <name-of-repo>
$ sudo apt update
$ sudo apt install <name-of-package>
```

To list the repositories that has been added to `apt`, run this command:

```
$ ls /etc/apt/sources.list.d/
```

Sometimes, as is the case with the KXStudios repositories later mentioned in this README, the repos are installed via a `.deb` file. This can get messy sometimes, and I had to remove the sources file to get it up and running. I'll get to that later.

#### Synaptic package manager

...is a graphic frontend to `apt`. Here you can search for packages and install them, and it's quite user-friendly.

### Connect to eduroam

Super important for me, du to studying at a university. 

[Guide](https://www.sheffield.ac.uk/cics/wireless/linux)

Here are the settings I use:

__Security:__ 

WPA & WPA2 Enterprise

__Authentication:__ 

Protected EAP (PEAP)

__Anonymous Identity:__ 

Blank

__Domain:__ 

Blank

__No CA certificate is required:__ 

Checked

__PEAP version:__ 

Version 0

__Inner authentication:__ 

MSCHAPv2

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

__Check OS version__

```
$ cat /etc/os-release
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

#### Spell checking in Geary
To get Swedish spell checking to work in Geary, i installed two packages: `hunspell-sv` and `ispell-sv`. It works now.

### Music player

I use Lollypop as my music player. To install, you have to add the Lollypop repositories to `apt`:

```
$ sudo add-apt-repository ppa:gnumdk/lollypop
$ sudo apt update
$ sudo apt install lollypop
```

It finds all the album art and stuff for you.
	
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
