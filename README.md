#gitchg
---

##Introduction 

gitchg is a tool to view git code changes by commit id.For example, when studying
linux kernel source code, we often need to browse the detailed changes of a certain
version. The current git difftool is not very readable, and the gitchg tool can be
used to compare and view. 

gitchg is based on git difftool and vimdiff, so you need to configure git and vimdiff
before use.

##git config

- git config --global diff.tool vimdiff
- git config --global difftool.prompt false
- git config --global alias.d difftool

##vim diff

Configure vimdiff by configuring ~/.vimrc file, For easy viewing and comparison,
it is recommended to use the peaksea vim color plug-in.
	
~/.vimrc configurtion:

	if &diff
		colors peaksea
		set t_Co=256
	endif