# How to Correct Your Previous Linux/Unix Command with thefuck App

Let's face it, we all make mistakes at the command line. Typos, wrong options, forgetting to add sudo - the list goes on. But there's a neat little app called thefuck that can help you correct your previous Linux and Unix command line errors.

## Installation

To install thefuck, you'll need Python version 2.7+ or 3.3+ along with pip and python-dev. The installation process is straightforward:

### MacOS Installation

1. Open the Terminal app
2. Install Homebrew on macOS by running `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`
3. Run the following command `brew install thefuck`

```
$ brew install thefuck

```
### Sample outputs:

```
==> Installing dependencies for thefuck: sqlite
==> Installing thefuck dependency: sqlite
==> Downloading https://homebrew.bintray.com/bottles/sqlite-3.20.1.sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring sqlite-3.20.1.sierra.bottle.tar.gz
==> Caveats
This formula is keg-only, which means it was not symlinked into /usr/local,
because macOS provides an older sqlite3.

If you need to have this software first in your PATH run:
  echo 'export PATH="/usr/local/opt/sqlite/bin:$PATH"' >> ~/.bash_profile

For compilers to find this software you may need to set:
    LDFLAGS:  -L/usr/local/opt/sqlite/lib
    CPPFLAGS: -I/usr/local/opt/sqlite/include
For pkg-config to find this software you may need to set:
    PKG_CONFIG_PATH: /usr/local/opt/sqlite/lib/pkgconfig

==> Summary
  /usr/local/Cellar/sqlite/3.20.1: 11 files, 3.0MB
==> Installing thefuck
==> Downloading https://homebrew.bintray.com/bottles/thefuck-3.23.sierra.bottle.tar.gz
######################################################################## 100.0%
==> Pouring thefuck-3.23.sierra.bottle.tar.gz
==> Caveats
Add the following to your .bash_profile, .bashrc or .zshrc:

  eval "$(thefuck --alias)"

For other shells, check https://github.com/nvbn/thefuck/wiki/Shell-aliases
==> Summary
  /usr/local/Cellar/thefuck/3.23: 711 files, 6.2MB

```

### Debian/Ubuntu Linux Installation

1. Open the terminal
2. Run the following command

```
$ sudo apt-get update
$ sudo apt-get install python3-dev python3-pip
$ sudo pip3 install thefuck

```

### Linux/Unix Installation

1. Open the terminal
2. Run the following command 

```

pip install thefuck

```

## Configuration

1. Edit your shell configuration file, such as `~/.bash_profile`, `~/.bashrc`, or `~/.zshrc`
2. Add the following line to the file: `eval $(thefuck --alias)`

```
$ echo 'eval $(thefuck --alias)' >> ~/.bashrc

```

3. Reload the changes by running `source ~/.bash_profile` (or the appropriate file for your shell) or restarting the terminal app/shell

```

$ source ~/.bashrc


```

## Usage

Using thefuck is simple. Just type the `fuck` command followed by enter after making a mistake or typo in your previous command. For example:

```

$ apt-get install nginx
E: Could not open lock file /var/lib/dpkg/lock - open (13: Permission denied)
E: Unable to lock the administration directory (/var/lib/dpkg/), are you root?

```

To add `sudo` before the `apt-get` command, run `fuck apt-get`.

```

$ fuck
sudo apt-get install nginx [enter/↑/↓/ctrl+c] [sudo] password for vivek:
Reading package lists... Done

```