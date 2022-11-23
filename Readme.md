# Bash inline script

The following bash inline script is helpful to create a new keyboard bindings in linux, to increase prodcutivity, instead of minimizing and focusing, or creating new instance of the application if it doesn't exist, the following script simply search for the existence of the required window, if it does exist it would focus it, if it does exist and focused the script would minimize the window, and if it doesn't exist then the script would create a new instance for the window, the bash is written as follows,
```
bash -c ' [ -n "$(xdotool search --name "onsi@onsi")" ] && [ "$(xdotool getactivewindow)" = "$(xdotool search --name "onsi@onsi")" ] && xdotool windowminimize "$(xdotool search --name "onsi@onsi")" || xdotool windowactivate "$(xdotool search --name "onsi@onsi")" || "gnome-terminal" '
```

you just copy-paste the above script in your custom-shortcut, and create your favored keyboard bindings to exectue it. You have to install xdotool, in arch linux, you can install it using the following, 
```
sudo pacman -S xdotool
```
And in ubuntu it can be installed via, 

```
sudo apt-get update
sudo apt-get install xdotool
```
check the proper way to install xdotool **if it exists** in you linux OS version. 
