# terminal-splash-screen
Terminal splash screen with Weather, Calendar, Time, and System Information displayed.
This information provided courtesy of user https://unix.stackexchange.com/users/200094/wineunuuchs2unix
You may see more of his work at https://www.pippim.com/

The heavy lifting is the splash component that shows something like this:

$ now
 
Weather report: Edmonton               March 2018            ┌────────────────────────────┐
                                  Su Mo Tu We Th Fr Sa       │   ┏━┓╺┓  ┏━┓┏━┓   ┏━┓┏┳┓   │
     \   /     Sunny                           1  2  3       │   ┃┃┃ ┃ ╹┏━┛┗━┫   ┣━┛┃┃┃   │
      .-.      -23--14 °C          4  5  6  7  8  9 10       │   ┗━┛╺┻╸╹┗━╸┗━┛   ╹  ╹ ╹   │
   ― (   ) ―   ↘ 22 km/h          11 12 13 14 15 16 17       └────────────────────────────┘
      `-’      14 km              18 19 20 21 22 23 24  
     /   \     0.9 mm             25 26 27 28 29 30 31  

Save the `~/.bashrc" file changes.
To display the Ubuntu information you need screenfetch:

sudo apt install screenfetch

There are similar display packages to screenfetch so shop around!
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
