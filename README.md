# Project Hamster - The Gnome Time Tracker

Project Hamster is time tracking for individuals. It helps you to keep track of
how much time you have spent during the day on activities you choose to track.

# Installation

**Bleeding edge warning**: Project Hamster right now is undergoing bit of
reshuffling and might not be fit for everyday use. For stable versions check out
[releases](https://github.com/projecthamster/hamster/releases).

## Dependencies

**Requires recent GTK+:** Version of GTK+ required is 3.10 because of the use of
HeaderBar and other bits. Sorry and get up to date!

Debian-based: `apt-get install git-core gettext intltool python-gconf python-xdg`
RPM-based: `yum install git-core gettext intltool gnome-python2-gconf`

## Installing

```bash
./waf configure build --prefix=/usr/local
sudo ./waf install
```

If you upgraded from an existing installation make sure to kill the running
daemons:

```bash
killall hamster-service hamster-windows-service
```

Now restart your panels/docks and you should be able to add Hamster!


### Migrating from hamster-applet

Previously Hamster was installed everywhere under `hamster-applet`. As
the applet is long gone, the paths and file names have changed to
`hamster-time-tracker`. To clean up previous installs follow these steps:

```bash
git checkout d140d45f105d4ca07d4e33bcec1fae30143959fe
./waf configure build --prefix=/usr
sudo ./waf uninstall
```

# Contributing

1. [Fork](http://help.github.com/forking/) Hamster
1. Create a topic branch - `git checkout -b my_branch`
1. Push to your branch - `git push origin my_branch`
1. Submit a [Pull Request](https://github.com/projecthamster/hamster/pulls) with your branch
1. That's it!
