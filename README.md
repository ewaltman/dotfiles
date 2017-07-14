dotfiles
========
Evan's dotfiles for OS X


Install
-------

1. Install dependencies:
  * [oh-my-zsh][1]
  * [Powerline][2]

2. Run

  ```sh
  cd ~
  git clone https://github.com/ewaltman/dotfiles.git ~/dotfiles
  cd ~/dotfiles
  rake install
  ```

3. In the `.zshrc`, set `DOTFILES=~/path/to/this/repo>` (i.e. `~/dotfiles`).

  - `zsh/zshrc.symlink` and `globalenv.symlink`: set up path variables
  - `aliases.symlink`: create aliases
  - `git/gitconfig.symlink`: configure git


Components
----------

All `*.symlink` files get symlinked into your `$HOME` when you run `rake
install`. This is so you can keep everything versioned in the repo.

### Shell ###

* I use `zsh` (rather than `bash`), with [oh-my-zsh][1].

* Every `*.zsh` file gets sourced into `zsh`. The idea is to split `zsh`
  configuration into separate files and categories, rather than having a
  monolithic `.zshrc`.

* The prompt is supplied by [Powerline][2] (default theme).

* Aliases are defined in `aliases.symlink`.

* For a shell app, I use iTerm.

  - In order for the `zsh` prompt to render properly, you need to set up your
    terminal to use a powerline-enabled. Install one of the fonts
    [here][3] and then set it as the font in `iTerm > Preferences > Profiles > Text`.
    One such font is included in `./assets/fonts/Inconsolata-dz-Powerline.otf`.

Thank You
------

The structure and content of this repo is inspired by @holman's [dotfiles](https://github.com/holman/dotfiles);
the Rakefile is entirely his, and so are parts of this README.

[1]: https://github.com/spf13/spf13-vi://github.com/robbyrussell/oh-my-zsh "oh-my-zsh"
[2]: https://github.com/powerline/powerline "Powerline"
[3]: https://gist.github.com/qrush/1595572 "powerline-fonts"
