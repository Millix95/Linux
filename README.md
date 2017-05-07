# Linux-basic-commands

Introduction

This document shows the Environment on Linux machines, and some of the inner workings of the shell and the terminal emulator program itself. 

## 13 Customizing the prompt – Some alternative prompt designs.

We are able to change the prompt to see the effect. First, we will back up the existing string, so we could restore it later. To do this, we will copy the existing string into another shell variable, what we create by ourselves:

 

We created a new variable what’s called ps1_old and assign the value of PS1 to it. 

We can verify that the string has been copied by using the echo command:

 

We can restore the original prompt at any time during our terminal session by simply reversing the process:

 

Now let’s see what happens if we have an empty prompt string:

 

We can realise we get nothing. The prompt is still there but displays nothing, just as we asked it to. We can replace it with a minimal prompt like:

 

Now we can see what we are doing. Notice the trailing space within the double quotes. This provides the space between the dollar sign and the cursor when the prompt is displayed. 



 

Adding time-of-day to our prompt will be useful if we need to keep track of when we perform certain tasks. Finally let’s create a new prompt which is similar to our original:
