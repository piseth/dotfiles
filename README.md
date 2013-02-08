# Overview

These are my dotfiles. *Use at your own risk.*

Hope you find them inspiring – Feedback welcome :)

# Usage

Make sure you have install zsh and oh-my-zsh first
<pre>
git clone https://github.com/visay/dotfiles.git /var/www/dotfiles
</pre>
Now activate the files you want ([re]move if exist):
<pre>
ln -s /var/www/dotfiles/zshrc ~/.zshrc
ln -s /var/www/dotfiles/bashrc ~/.bashrc
ln -s /var/www/dotfiles/gemrc ~/.gemrc
ln -s /var/www/dotfiles/ackrc ~/.ackrc
ln -s /var/www/dotfiles/profile ~/.profile
ln -s /var/www/dotfiles/siegerc ~/.siegerc
ln -s /var/www/dotfiles/tmux/tmux-panes ~/.tmux-panes
ln -s /var/www/dotfiles/tmux/tmux.conf ~/.tmux.conf
ln -s /var/www/dotfiles/git/gitconfig ~/.gitconfig               # Make sure you customize your author
ln -s /var/www/dotfiles/git/gitignore_global ~/.gitignore_global
ln -s /var/www/dotfiles/hg/hgrc ~/.hgrc                          # Make sure you customize your author
ln -s /var/www/dotfiles/hg/hgignore_global ~/.hgignore_global
ln -s /var/www/dotfiles/vimrc.after ~/.vimrc.after
ln -s /var/www/dotfiles/vimrc.before ~/.vimrc.before
ln -s /var/www/dotfiles/tmuxinator ~/.tmuxinator

# Ubuntu only
ln -s /var/www/dotfiles/terminator ~/.config/terminator/config

# Maven only
ln -s /var/www/dotfiles/m2/settings.xml ~/.m2/settings.xml
</pre>

# Other goodies

## Create folder for janus plugins

See https://github.com/carlhuda/janus#customization for details
<pre>
mkdir ~/.janus
cd !$
git clone git://github.com/vim-scripts/Auto-Pairs.git
git clone git://github.com/vim-scripts/Align.git
</pre>

## Install Rubies

See
Mac: http://stackoverflow.com/questions/11664835/mountain-lion-rvm-install-1-8-7-x11-error/11666019#11666019
for details
Ubuntu: https://www.digitalocean.com/community/articles/how-to-install-ruby-on-rails-on-ubuntu-12-04-lts-precise-pangolin-with-rvm
<pre>
export CPPFLAGS=-I/opt/X11/include
CC=/usr/local/bin/gcc-4.2 rvm reinstall 1.8.7
rvm install jruby
</pre>
After that you might want to install Gems:
<pre>
rvm use 1.9.3
gem install bundler --no-ri --no-rdoc
</pre>

# Kudos

1. These files are heavily inspired by https://peepcode.com/products/advanced-command-line.
If you're new to CLI, I highly recommend watching the screencast.
2. The tmux config file is a modified version of http://media.pragprog.com/titles/bhtmux/code/workflows/tmux.conf
tmux is awesome - This book helped me getting used to it and it's fun to read: http://pragprog.com/book/bhtmux/tmux
3. My vim config is based on https://github.com/carlhuda/janus.
4. My zsh config is based on https://github.com/robbyrussell/oh-my-zsh.

# TODO

* Make it a one liner
Provide installation routine e.g. with chef