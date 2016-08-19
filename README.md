# dotspacemacs

My spacemacs configuration layers including the dotfile (.spacemacs).
The configuration and setting are tested with 'develop' branch of syl20bnr/spacemacs.

## Installation
Delete or backup your ~/.emacs and ~/.emacs.d/, then go to your `home` directory:

```
$ git clone https://github.com/syl20bnr/spacemacs.git .emacs.d
$ cd .emacs.d
$ git checkout -b develop -t origin/develop
$ cd ..
$ git clone https://github.com/stotok/dotspacemacs.git
$ ln -s dotspacemacs/.spacemacs .
```

## Contents

### cscope

Support c/c++ and python modes. Script indexers can be found at 
`mycontribs/ttk-cscope/local/xcscope/`. Modify them according to your code structure. 

My preference is to invoke the indexer at the root directory of your source tree from the 
command line. Include the script's path into your ${PATH} then:

```
$ cscope-indexer -r -v
```

#### Keybindings:

In c/c++ mode or python mode, place the cursor on function name or macro of your interest:

Leader key is:  `SPC m`

Available commands:
```
      "gs" 'cscope-find-this-symbol
      "gd" 'cscope-find-global-definition
      "gc" 'cscope-find-functions-calling-this-function
      "gC" 'cscope-find-called-functions
      "gi" 'cscope-find-files-including-file
      ;;
      "gb" 'cscope-display-buffer
      ;;
      "ga" 'cscope-set-initial-directory
      "gA" 'cscope-unset-initial-directory
```      

In cscope buffer, here's available commands:

```
   [return] 'cscope-select-entry-other-window
   " "      'cscope-show-entry-other-window
   "o"      'cscope-select-entry-one-window
   "q"      'cscope-bury-buffer
   "Q"      'cscope-quit
   "s"      'cscope-find-this-symbol
   "d"      'cscope-find-this-symbol
   "g"      'cscope-find-global-definition
   "c"      'cscope-find-functions-calling-this-function
   "C"      'cscope-find-called-functions
   "t"      'cscope-find-this-text-string
   "f"      'cscope-find-this-file
   "i"      'cscope-find-files-including-file
   "u"      'cscope-pop-mark
```

