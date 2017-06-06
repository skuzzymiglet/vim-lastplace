# vim-lastplace v3.1.1

Intelligently reopen files at your last edit position. By default git,
svn, and mercurial commit messages are ignored because you
probably want to type a new message and not re-edit the previous
one.

## Advantages
Advantages over the snippets that can be found around the net include:
* Maximizes Available Context
    - Center the cursor vertically after restoring last edit position.
    - Keep as much of the file on screen as possible when last edit position is at the end of the file.
* Commit messages automatically start beginning of the file. This is important because many version control systems re-use the same file for commit message editing.
* Opens folds if the last edit position is inside a fold.

## Installation
Thanks to [David Rabel](https://github.com/NoreSoft)'s hard work, you can install vim-lastplace from debian-testing:

    apt-get install vim-lastplace
    
You can also use [pathogen.vim](https://github.com/tpope/vim-pathogen) or other plugin managers to install and use vim-lastplace.

    cd ~/.vim/bundle
    git clone git://github.com/farmergreg/vim-lastplace.git


## Configuration
You can configure what file types to ignore by setting
g:lastplace_ignore in your vimrc. This is a comma separated list.
By default it is set to:

        let g:lastplace_ignore = "gitcommit,gitrebase,svn,hgcommit"

You can configure buffer types to ignore by setting
g:lastplace_ignore_buftype in your vimrc. This is a comma separated list.
By default it is set to:

        let g:lastplace_ignore_buftype = "quickfix"

Folds are automatically opened when jumping to the last edit position. If you
do not like this behavior you can disable it by putting this in your vimrc:

        let g:lastplace_open_folds = 0

## Miscellaneous
This plugin is complete and stable. Please do not be afraid to try it even
if there is very little recent activity in this repository. If you do find
a bug, please submit a pull request that fixes whatever problem you're having.

## Version History

### 3.1.1
- Do not jump when a new file is created (Issue [#15](https://github.com/farmergreg/vim-lastplace/issues/15))

### 3.1.0
- Add g:lastplace_ignore_buftype setting.
- Update github links from username dietsche to farmergreg.

### 3.0.4
- Add g:lastplace_open_folds option.

### 3.0.3
- Point release for Debian packaging. Changes all http links to https. No code changes.

### 3.0.2
- A fix for files that are smaller than the current screen size (issue #8)

### 3.0.1
- A fix for files with modelines.

### 3.0.0

- Open folds if the last edited area is inside a closed fold.

### 2.0.1

- Add gitrebase filetype to the ignore list.

### 2.0.0

- Center the screen when restoring the cursor position.
- When at the end of a file, keep as much of it on screen as possible.

### 1.0.0

- Initial version.

## About

- Author  :  Greg Dietsche
- Web Page: https://www.gregd.org/

Get the latest version, submit pull requests, and file bug reports
on GitHub:
- https://github.com/farmergreg/vim-lastplace

If you like this plugin, please star and rate it on these sites:

- [GitHub](https://github.com/farmergreg/vim-lastplace)
- [Vim.org](http://www.vim.org/scripts/script.php?script_id=5090)
