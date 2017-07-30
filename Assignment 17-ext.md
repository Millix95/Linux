# Linux-basic-commands

Introduction

This site shows the Environment on Linux machines, and some of the inner workings of the shell and the terminal emulator program itself. 
## Customizing the prompt – Some alternative prompt designs.

We are able to change the prompt to see the effect. First, we will back up the existing string, so we could restore it later. To do this, we will copy the existing string into another shell variable, what we create by ourselves:

```
user@ubuntu:~$ ps1_old="$PS1"
```
 
We created a new variable what’s called ps1_old and assign the value of PS1 to it. 


We can verify that the string has been copied by using the echo command:
```
user@ubuntu:~$ echo $ps1_old
\[\e]0;\u@\h: \w\a\]${debian_chroot:+($debian_chroot)}\u@\h:\w\$
 ```

We can restore the original prompt at any time during our terminal session by simply reversing the process:
```
user@ubuntu:~$ PS1="$ps1_old"
 ```

Now let’s see what happens if we have an empty prompt string:
```
user@ubuntu:~$ PS1=
 ```

We can realise we get nothing. The prompt is still there but displays nothing, just as we asked it to. We can replace it with a minimal prompt like:
```
PS1="\$ "
 ```

Now we can see what we are oing. Notice the trailing space within the double quotes. This provides the space between the dollar sign and the cursor when the prompt is displayed. 
```
$ PS1="\A \h \$ "
```


 

Adding time-of-day to our prompt will be useful if we need to keep track of when we perform certain tasks. Finally let’s create a new prompt which is similar to our original:
```
08:06 ubuntu $ PS1="<\u@\h \W>$"
<user@ubuntu ~>$
```
