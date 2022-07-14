# How to implement
1) Go to '/Home' directory and find '.bashrc' file.
2) Insert the following code at the end of the file.

<div>git_branch() {</div>
<div>git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'</div>
<div>}</div>
<div>export PS1="\[\e]0;\u@\h: \w\a\]${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\] \[\033[00;91m\]\$(git_branch)\[\033[00m\]\$ "</div>

