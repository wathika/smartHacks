**Vim** is a text editor that is upwards compatible to ***Vi***. It can be used to edit all kinds of plain text. It is especially useful for editing programs.

There are a lot of enhancements above Vi: multilevel undo, multi windows and buffers, syntax highlighting, command line editing, file-name completion, on-line help, visual selection .

* To edit file : *vim filename*
* To save file : Press **Esc** then `:w` or `:wq` or `:x` to save and exit
* Save with another name : `:w new_name`
* Leave without saving : **Esc** then  `:q!`
* Set color : **Esc** then  `:syntax on`
* To set line numbers : Add `set number` to your `.vimrc` file in your home directory (always)

Another Tips :

* `:set tabstop=4` " Sets the tab size to 4 " (tabs are usually 8 spaces)
* Type `.` in normal mode to repeat last change, this is super useful when doing a receptive task.
* You can use u to undo the last change. `CTRL` + `R`  redoes a change that has been undone. U returns the current line to its original state. -

Bonus Tip :
`:x` is better for save and exit, Doesn’t actually write to the file unless it needs to