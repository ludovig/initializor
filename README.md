initializor
===========

Great tools in zsh to setup a fine user environment.
Bookmarks, home directories arborescence, management of internet sources projects, share initialisation, and simple dotfiles installation.

Installation
------------

Copy initializor.cfg.sample into ~/.initializor.cfg and edit it according to your needs. If you need a share, you can also copy initializor.share.cfg.sample into ~/.initializor.share.cfg. Various tools are described below with theirs configurations explanations.
When you're satisfied, you can run

    zsh init-all

to complete first install.

Usage
-----
### check-system

Use gnu commands also when on darwin system.

### init-all

Init home arborescence, dotfiles links, download various projects sources, and add local files with zsh bookmarks and paths accordingly to local configuration.
If share configuration is specified with -s option, or present in dotfiles, create a new share and do all the above also inside of it.

### init-bookmarks

Show zsh bookmarks that could be guessed from traverse-tree arborescence.

### init-dirs

Create directories from traverse-tree output.

### init-links

Use it to link config files from a repository to home directory.
* [links] list of links
* [links_location] Replace dirname of links by labeled path from traverse-tree

### init-path

Show zsh path extended with selected projects sources

### init-src
Retrieve various projects from the internet
* [src] url of the projet
* [src_destination] local path of the project guessed on labeled path from traverse-tree (optional, default to src label from traverse-tree)

### load-config

Load, or show, converted zsh parameters from selected sections configurations values from any ini config.

### reset-files

Create local files with zsh bookmarks and extended path depending on current configuration. Also edit theses files with share bookmarks and path if a share config is specified with option -s or present in dotfiles.
* [localpath]
  * bookmarks_file: location of local zsh bookmarks files
  * paths_file: location of local zsh extended path files

### traverse-tree

Show current directories arborescence based on config from initializor.cfg.
* [names] to rename some nodes
* [nodes] list of nodes, with their childrens
* [local] exclude some nodes if needed
