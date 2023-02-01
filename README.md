# How to Correct Your Previous Linux/Unix Command with thefuck App

Let's face it, we all make mistakes at the command line. Typos, wrong options, forgetting to add sudo - the list goes on. But there's a neat little app called thefuck that can help you correct your previous Linux and Unix command line errors.

## Installation

To install thefuck, you'll need Python version 2.7+ or 3.3+ along with pip and python-dev. The installation process is straightforward:

### macOS Installation

1. Open the Terminal app
2. Install Homebrew on macOS by running `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`
3. Run the following command `brew install thefuck`

### Debian/Ubuntu Linux Installation

1. Open the terminal
2. Run the following command `sudo apt install thefuck`

### Linux/Unix Installation

1. Open the terminal
2. Run the following command `pip install thefuck`

## Configuration

1. Edit your shell configuration file, such as `~/.bash_profile`, `~/.bashrc`, or `~/.zshrc`
2. Add the following line to the file: `eval $(thefuck --alias)`
3. Reload the changes by running `source ~/.bash_profile` (or the appropriate file for your shell) or restarting the terminal app/shell

## Usage

Using thefuck is simple. Just type the `fuck` command followed by enter after making a mistake or typo in your previous command. For example:

To add `sudo` before the `apt-get` command, run `fuck apt-get`.