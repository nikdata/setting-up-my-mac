WIP 🚧 🏗 

Hello! 👋🏽

Over the years, I've become accustomed to using certain applications (both work & personal) using macOS. As anyone knows, when you buy a new Mac (or any computer for that matter), you'll want to spend a little bit of time configuring it to your liking. 

Some of the apps that I frequently use:

- PyCharm
- VSCode
- Python, R
- RStudio
- Docker & Orbstack

In addition to those, I also use quite a few handy applications that help make my life a bit easier.

In this brief guide, I'll go over the basic applications I use:

- [Setting up Homebrew](https://github.com/nikdata/setting-up-my-mac?tab=readme-ov-file#homebrew)
- [Improving Terminal & Configuring](https://github.com/nikdata/setting-up-my-mac?tab=readme-ov-file#make-terminal-better)
- [Setting up git](https://github.com/nikdata/setting-up-my-mac?tab=readme-ov-file#git)
- [Configuring GitHub with SSH key](https://github.com/nikdata/setting-up-my-mac?tab=readme-ov-file#github--ssh-key)
- [Setting up Python](https://github.com/nikdata/setting-up-my-mac?tab=readme-ov-file#python)
- [Setting up R](https://github.com/nikdata/setting-up-my-mac?tab=readme-ov-file#r)
- [Key Applications](https://github.com/nikdata/setting-up-my-mac?tab=readme-ov-file#key-applications)
  - [PyCharm](https://github.com/nikdata/setting-up-my-mac?tab=readme-ov-file#pycharm)
  - [VSCode](https://github.com/nikdata/setting-up-my-mac?tab=readme-ov-file#vscode)
  - [RStudio](https://github.com/nikdata/setting-up-my-mac?tab=readme-ov-file#rstudio)
  - [Orbstack](https://github.com/nikdata/setting-up-my-mac?tab=readme-ov-file#orbstack)
- [Handy Applications](https://github.com/nikdata/setting-up-my-mac?tab=readme-ov-file#handy-applications)
  - [Itsycal](https://github.com/nikdata/setting-up-my-mac?tab=readme-ov-file#itsycal)
  - [Raycast](https://github.com/nikdata/setting-up-my-mac?tab=readme-ov-file#raycast)
  - [Maccy](https://github.com/nikdata/setting-up-my-mac?tab=readme-ov-file#maccy)

### Homebrew

[Homebrew](https://brew.sh) is a package manager for both Linux & macOS. Think of Homebrew like an app store, but primarily run through the command line. You can find thousands of applications on homebrew - including Linux-like libraries for macOS.

Homebrew can be installed by running the following line in macOS Terminal app:

``` shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
You may be required to install Command Line Tools, but Homebrew can install it for automatically.

### Make Terminal Better

Using the command line is important if you're a developer. The Terminal app in macOS is good.

![](https://i.imgflip.com/4tvuhv.jpg)

But it can be better!

#### iTerm2 - the Better Terminal app
[iTerm2](https://iterm2.com) is a command line application emulator that can really make things better for you. For example, you can have tiled windows within 1 window. Now you too can be like one of those cool developers in sci-fi movies!

You can install iTerm2 by downloading from their [website](https://iterm2.com) or use the following command in the Terminal app:

``` shell
brew install --cask iterm2
```

#### ZSH
ZSH is Z shell and it's the 'default' for macOS. You'll want to install zsh. Trust me. And now you can use iTerm2!

``` shell
brew install zsh
```

#### Oh-My-Zsh
[Oh-My-ZSH](https://ohmyz.sh) is a framework for managing zsh configuration. Why do you want it? It's a powerful tool to help make things easier while using the z-shell.

You can install Oh-My-Zsh using iTerm2:

``` shell
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

#### Powerlevel10k

One of the cool things with using Oh-my-Zsh is themeing it. I like using the [Powerlevel10K](https://github.com/romkatv/powerlevel10k) theme.

These are the [instructions](https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#oh-my-zsh) for installing it on zsh.

NOTE: This project is probably not going to last forever. I may end up switching to [starship](https://starship.rs)

The instructions/site I've linked do a great job of walking through the configuration of Powerlevel10k. It's pretty easy to configure and you pretty much only have to do it once.

### Git

There's a very good chance that the current macOS version you have on your new Mac is using an outdated version of git. Git is the "soul" behind GitHub and it's a very powerful tool for code version tracking. It doesn't matter if you use GitLab, BitBucket, or whatever - chances are git is the tool behind them.

Install the latest version of git:

``` shell
brew install git
```

#### Configure git
You can also configure git to use a default user name & email:

``` shell
git config --global user.name "<any name>"
git config --global user.email "<any.email@example.com>"
```

You can also set up the default branch. I like to use main.

``` shell
git config --global init.defaultBranch main
```

I also like to use nano instead of vim:

``` shell
git config --global core.editor "nano"
```

### GitHub & SSH Key

A more secure way to interact with GitHub is to use SSH tokens. This prevents your username & password from being used and if your token ever becomes public, just delete and create a new one.

Instructions can be found [here](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

#### Create a .ssh folder

Navigate to your home folder

``` shell
cd ~
```

Now create the .ssh folder

``` shell
mkdir .ssh
```

Create a key (replace with your email address):

``` shell
ssh-keygen -t ed25519 -C "your_email@example.com"
```

#### Add to GitHub

You can add your new key using these [instructions](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

### Python

Install the latest version of Python

``` shell
brew install python
```

Install uv (a faster way to install Python libraries as compared to pip)

``` shell
# On macOS and Linux.
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Install [micromamba](https://mamba.readthedocs.io/en/latest/installation/micromamba-installation.html):

``` shell
brew install micromamba
```

Don't bother with mamba, conda, etc. Micromamba is small, efficient, and fast.

### R

Always install R from [CRAN's website](https://cran.r-project.org).

### Key Applications

#### PyCharm

Download & install PyCharm [here](https://www.jetbrains.com/pycharm/).

#### VSCode

Download from [https://code.visualstudio.com/](https://code.visualstudio.com/)

#### RStudio

I know that [Positron](https://positron.posit.co) is the new IDE that Posit is coming out with. It's still not ready for full production use (as of 17 Feb 2025). Almost there!

For now, I still use [RStudio](https://posit.co/download/rstudio-desktop/).

#### Docker & Orbstack

[Orbstack](https://orbstack.dev) is a better version of Docker Desktop. It's more efficient and faster. And if you're on a laptop, Orbstack is just the right tool to use.

### Handy Applications

#### Itsycal

[Itsycal](https://www.mowglii.com/itsycal/) is a neat little calendar that can stay in your menu bar at the top.

``` shell
brew install --cask itsycal
```

#### Raycast

[Raycast](https://www.raycast.com) is powerful replacement for spotlight

``` shell
brew install --cask raycast
```

#### maccy

[Maccy](https://maccy.app) is a clipboard history tool.

``` shell
brew install --cask maccy
```
