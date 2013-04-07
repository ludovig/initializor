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

### init-localpath

Show zsh path extended with selected projects sources

### init-share
Create a share between users with directory hierarchy from traverse-tree. Create group if needed.

*See initializor.share.cfg.sample for an example of a share config*
* [local]
  * root_location: share emplacement
  * owner: First owner of the share directories
  * group_id: group id of the share (only need if group doesn't exist)
  * group_name: group owner of the share

### init-src
Retrieve various projects from the internet
* [src] url of the projet
* [src_destination] local path of the project guessed on labeled path from traverse-tree (optional, default to src label from traverse-tree)

### load-config

Load zsh parameters in current environment from read-config output.

### read-config

Show selected sections configurations values from intializor.cfg converted in zsh parameters.

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
