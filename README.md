dotfiles
========
Evan's dotfiles for OS X


Install
-------

1. Install the external dependencies:
  * [spf13-vim][1]
  * [oh-my-zsh][2]
  * [Powerline][4]

2. Run

  ```sh
  cd ~
  git clone https://github.com/ewaltman/dotfiles.git ~/dotfiles
  cd ~/dotfiles
  rake install
  ```

3. In the `.zshrc`, set `DOTFILES=~/path/to/this/repo>`. I just use `~/dotfiles`.

Then you should be all set. Some files you'll want to personalize right away:

- `zsh/zshrc.symlink` and `globalenv.symlink`: set up your own path variables
- `aliases.symlink`: create your own aliases
- `git/gitconfig.symlink`: commit as yourself


Components
----------

All `*.symlink` files get symlinked into your `$HOME` when you run `rake
install`. This is so you can keep everything versioned in the repo.

### Shell ###

* I use `zsh` (rather than `bash`), with [oh-my-zsh][2].

* Every `*.zsh` file gets sourced into `zsh`. The idea is to split `zsh`
  configuration into separate files and categories, rather than having a
  monolithic `.zshrc`.

* The prompt is supplied by [Powerline][4] (I just use the default theme).

* Aliases are defined in `aliases.symlink`.

* For best results, use iTerm.

  - In order for the `zsh` prompt to render properly, you need to set up your
    terminal to use a powerline-enabled font. Install one of the fonts
    [here](https://github.com/Lokaltog/powerline-fonts) and then set it as the
    font in `iTerm > Preferences > Profiles > Text`.
    There's a few special files in the hierarchy.


Thanks
------

The structure and content of this repo is inspired by @holman's [dotfiles][3];
the Rakefile is entirely his, and so are parts of this README.