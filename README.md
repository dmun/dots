# dots
Dotfile manager made in Shell.

## Quickstart
1. Installation:
```
git clone https://github.com/dmun/dots.git && sudo cp dots/dots /usr/local/bin/
```
2. Make sure your dotfiles folder satisfies the folder structure in the Requirements section of this README.
3. Set your dotfiles directory absolute path.
```
dots set <directory>
```

## Usage
`dots link [<dotfile>]` to link a dotfile to the proper config folder, leave empty to link all files.
 
`dots unlink [<dotfile>]` to unlink a dotfile, leave empty to unlink all files.

`dots status` to check the status.

`dots set <directory>` to set the dotfiles directory.

## Requirements
The script expects the dotfiles directory to be structured as follows:
```
├── .doom.d           -->  $HOME/.doom.d/
│   ├── config.el
│   ├── init.el
│   └── packages.el
├── fontconfig        -->  $HOME/.config/fontconfig/
│   └── fonts.conf
├── kitty             -->  $HOME/.config/kitty/
│   └── kitty.conf
├── keybindings.json  -->  ignored
├── .zshrc            -->  $HOME/.zshrc
└── .vimrc            -->  $HOME/.vimrc
```
For every file including directories, starting with a dot `.`, a link will be created in the `$HOME/` directory.

For every directory that does not start with a dot, a link will be created in the `$HOME/.config/` directory.

Everything else will be ignored.

## TODO
* Better colors
* Make code more compact
* More features
