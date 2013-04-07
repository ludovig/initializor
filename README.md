initializor
===========

Post-installation and further maintenance of a system with zsh.

Installation
------------

Copy initializor.cfg.sample into ./initializor.cfg and edit it according to your needs. Various tools are described below with theirs configurations explanations.
When you're satisfied, you can run
  zsh initializor
to complete first install.

Usage
-----
### check-system

Use gnu commands also when on darwin system

### init-all

### init-bookmarks

Show zsh bookmarks that could be guessed from traverse-tree arborescence

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
__See initializor.share.cfg.sample for an example of a share config__
* [local]
  * root_location share emplacement
  * owner First owner of the share directories
  * group_id group id of the share (only need if group doesn't exist)
  * group_name group owner of the share

### init-src
Retrieve various projects from the internet
* [src] url of the projet
* [src_destination] local path of the project guessed on labeled path from traverse-tree (optional, default to src label from traverse-tree)

### read-config

Show selected sections configurations values from intializor.cfg converted in zsh parameters.

### load-config

Load zsh parameters in current environment from read-config output.

### traverse-tree

Show current directories arborescence based on config from initializor.cfg.
* [names] to rename some nodes
* [nodes] list of nodes, with their childrens
* [local] exclude some nodes if needed
