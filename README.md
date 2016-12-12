# Shell Marks
Shell Marks is a collection of shell functions that allow tracking directories
as bookmarks.  This implementation should work on many shells.

## Installation
Download shell marks:
```
git clone https://github.com/M1Sports20/shell_marks $HOME/.marks
```

Add the following line to your .bashrc or .zshrc.
```
source $HOME/.marks/marksrc
```

Restart any shells and you should be ready to go.

## Usage
Using marks only requires learning a few commands all of which are listed
below.

### mark
Marks the current directory as a marks.  Argument mark_name is optional and if
not specified the directory name being marked is used as the mark name.
```
Usage: mark [mark_name]
Example: mark
Example: mark wd
```

### unmark
Removes a mark.
```
Usage: unmark <mark_name>
Example: unmark wd
```

### marks
Lists currently available marks
```
Usage: marks
$> marks
wd        -> /home/user/my_project
kyle      -> /home/kyle/project
```

### readmark
Prints the location of a mark.  This is often used with arguments to another
shell command.
```
Usage: readmark wd
Example: du -sh $(readmark wd)
```

### jump
Jumps to the mark directory specified.
```
Usage: jump <mark_name>
Example: jump wd
```

### jumpd
Jumps to the mark directory specified.  Also saves the current directory on the
directory stack similar to pushd.
```
Usage: jumpd <mark_name>`
Example: jumpd wd
```

## Customization
The bookmarks project can be located anywhere.  To relocate this project to
somewhere other than the default put the following in your rc file.
```
export MARKSPATH="mymarkspath"
source $HOME/.marks/marksrc
```
