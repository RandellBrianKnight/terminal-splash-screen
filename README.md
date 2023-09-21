# terminal-splash-screen
Terminal splash screen with Weather, Calendar, Time, and System Information displayed.
This information provided courtesy of user https://unix.stackexchange.com/users/200094/wineunuuchs2unix
You may see more of his work at https://www.pippim.com/

The heavy lifting is the splash component that shows something like this:

$ now

Save the `~/.bashrc" file changes.
To display the Ubuntu information (or other distro) you need screenfetch:

sudo apt install screenfetch

There are similar display packages to screenfetch, like neofetch, so shop around!

If you want the same command prompt with "─────────" dividing line between commands, change these lines:

if [ "$color_prompt" = yes ]; then
    PS1='───────────────────────────────────────────────────────────────────────────────────────────
${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '
else
    PS1='───────────────────────────────────────────────────────────────────────────────────────────
${debian_chroot:+($debian_chroot)}\u@\h:\w\$ '
fi

unset color_prompt force_color_prompt

For more information about PS1 see https://www.warp.dev/blog/whats-so-special-about-ps1

Note the length of the separator line coincides with width of screenfetch output. In this case it is 92 characters wide and gnome-terminal preferences are set accordingly.
