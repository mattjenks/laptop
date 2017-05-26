Laptop
======

Laptop is a script to set up an OS X computer, and to keep
it up to date.

It can be run multiple times on the same machine safely.
It installs, upgrades, or skips packages
based on what is already installed on the machine.

Requirements
------------

We support:

* [macOS Sierra (10.12)](https://www.apple.com/osx/)
* OS X El Capitan (10.11)
* OS X Yosemite (10.10)
* OS X Mavericks (10.9)

Older versions may work but aren't regularly tested. Bug reports for older
versions are welcome.

Install
-------

Begin by opening the Terminal application on your Mac. The easiest way to open
an application in OS X is to search for it via [Spotlight]. The default
keyboard shortcut for invoking Spotlight is `command-Space`. Once Spotlight
is up, just start typing the first few letters of the app you are looking for,
and once it appears, press `return` to launch it.

In your Terminal window, copy and paste the command below, then press `return`.

```sh
bash <(curl -s https://raw.githubusercontent.com/mattjenks/laptop/basiclaptop/laptop)
```

**Once the script is done, make sure to quit and relaunch Terminal.**

It is highly recommended to run the script regularly to keep your computer
up to date. Once the script has been installed, you'll be able to run it
at your convenience by typing `laptop` and hitting `return` in your Terminal.

[Spotlight]: https://support.apple.com/en-us/HT204014

Debugging
---------

Your last Laptop run will be saved to `~/laptop.log`. Read through it to see if
you can debug the issue yourself. 

What it sets up
---------------

* [Flux] for adjusting your Mac's display color so you can sleep better
* [Homebrew] for managing operating system libraries
* [Homebrew Cask] for quickly installing Mac apps from the command , https://caskroom.github.io/
* [The Silver Searcher] for finding things in files
* [google-chrome] a good web browser


[Bundler]: http://bundler.io/
[chruby]: https://github.com/postmodern/chruby
[CloudApp]: http://getcloudapp.com/
[Cloud Foundry CLI]: https://github.com/cloudfoundry/cli
[Flux]: https://justgetflux.com/
[git-seekret]: https://github.com/18F/git-seekret
[GitHub Desktop]: https://desktop.github.com/
[Homebrew]: http://brew.sh/
[Homebrew Cask]: https://github.com/caskroom/homebrew-cask
[Homebrew Services]: https://github.com/Homebrew/homebrew-services
[hub]: https://github.com/github/hub
[MySQL]: https://www.mysql.com/
[n]: https://github.com/tj/n
[Node.js]: http://nodejs.org/
[NPM]: https://www.npmjs.org/
[PhantomJS]: http://phantomjs.org/
[Postgres]: http://www.postgresql.org/
[Python]: https://www.python.org/
[pyenv]: https://github.com/yyuu/pyenv/
[Redis]: http://redis.io/
[Ruby]: https://www.ruby-lang.org/en/
[ruby-install]: https://github.com/postmodern/ruby-install
[Slack]: https://slack.com/
[Sublime Text 3]: http://www.sublimetext.com/3
[The Silver Searcher]: https://github.com/ggreer/the_silver_searcher
[Virtualenv]: https://virtualenv.pypa.io/en/latest/
[Virtualenvwrapper]: http://virtualenvwrapper.readthedocs.org/en/latest/#
[Zsh]: http://www.zsh.org/

It should take less than 15 minutes to install (depends on your machine and
internet connection).

Customize in `~/.laptop.local` and `~/Brewfile.local`
-----------------------------------------------------

Your `~/.laptop.local` is run at the end of the `mac` script.
Put your customizations there. If you want to install additional
tools or Mac apps with Homebrew, add them to your `~/Brewfile.local`.
This repo already contains a [.laptop.local] and [Brewfile.local]
you can use to get started.

```sh
# Go to your OS X user's root directory
cd ~

# Download the sample files to your computer
curl --remote-name https://raw.githubusercontent.com/mattjenks/laptop/basiclaptop/.laptop.local
curl --remote-name https://raw.githubusercontent.com/matthjenks/laptop/basiclaptop/Brewfile.local
```

It lets you install the following tools and apps:

* [Firefox] for testing your website on a browser other than Chrome
* [iTerm2] - an awesome replacement for the OS X Terminal
* [Spectacle] - automatic window manipulation
* [1password] - password manager (for managing passowrds across devices other than apple products)
* [google-drive] - google drive for file sharing (to users other than icloud users)
* [dropbox] - dropbox for file sharing (to users other than icloud users)
* [pandora] - music
* [spotify] - music
* [kindle] - books

[.laptop.local]: https://github.com/mattjenks/laptop/blob/basiclaptop/.laptop.local
[Brewfile.local]: https://github.com/mattjenks/laptop/blob/basiclaptop/Brewfile.local
[Atom]: https://atom.io/
[Exuberant Ctags]: http://ctags.sourceforge.net/
[Firefox]: https://www.mozilla.org/en-US/firefox/new/
[iTerm2]: http://iterm2.com/
[reattach-to-user-namespace]: https://github.com/ChrisJohnsen/tmux-MacOSX-pasteboard
[Tmux]: https://tmux.github.io/
[Vim]: http://www.vim.org/
[Spectacle]: https://www.spectacleapp.com/
[1password]: https://1password.com/
[google-drive]: https://www.google.com/drive/
[google-chrome]: https://www.google.com/chrome/
[dropbox]: https://www.dropbox.com
[intellj-idea]: https://www.jetbrains.com/idea
[docker]: https://www.docker.com/
[vagrant]: https://www.vagrantup.com/
[virtualbox]: https://www.virtualbox.org/
[pandora]: https://www.pandora.com
[spotify]: https://www.spotify.com/us/
[kindle]: https://www.amazon.com/kindle-dbs/fd/kcp

Write your customizations such that they can be run safely more than once.
See the `mac` script for examples.

Laptop functions such as `fancy_echo` and `gem_install_or_update` can be used
in your `~/.laptop.local`.

Credits
-------

My script is based on the awesome [18F laptop script](https://github.com/18F/laptop). Which itself 
is based on and inspired by
[thoughtbot's laptop](https://github.com/thoughtbot/laptop) script.

### Public domain

thoughtbot's original work remains covered under an [MIT License](https://github.com/thoughtbot/laptop/blob/c997c4fb5a986b22d6c53214d8f219600a4561ee/LICENSE).

18F's work on this project is in the worldwide [public domain](LICENSE.md), as are contributions to our project. As stated in [CONTRIBUTING](CONTRIBUTING.md):

> This project is in the public domain within the United States, and copyright and related rights in the work worldwide are waived through the [CC0 1.0 Universal public domain dedication](https://creativecommons.org/publicdomain/zero/1.0/).
>
> All contributions to this project will be released under the CC0 dedication. By submitting a pull request, you are agreeing to comply with this waiver of copyright interest.
