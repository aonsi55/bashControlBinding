# Bash inline script

## Description
    
The provided bash inline script is helpful to create a new keyboard bindings in linux, to increase productivity, instead of minimizing and focusing, or creating new instance of the application if it doesn't exist, the script simply search for the existence of the required window, if it does exist it would focus it, if it does exist and focused the script would minimize the window, and if it doesn't exist then the script would create a new instance for the window.
    
## Dependencies
    
You have to install xdotool, in arch linux, you can install it using the following, 
```
sudo pacman -S xdotool
```
And in ubuntu it can be installed via, 

```
sudo apt-get update
sudo apt-get install xdotool
```
check the proper way to install xdotool **if it exists** in you linux OS version. 


## Usage

We will use the bash code to make a keyboard shortcut, which upon executing create a new instance of gnome-terminal if it does not exists, and it exists, it would focus it, and if it is focused, then it would minimize it the code is provided in the bashBinding.sh in the repository. In order to use the script you need to find the ```windowname``` and the ```appname```. 


### Window Name

Instead of ```windowname``` in the bashBinding.sh script, replace it with your app's window name, you can just open a new terminal, and find your app's window name using the following code, 
```
xdotool selectwindow 
```
The mouse courser will change, then click anywhere on you app's window, the terminal would print out the clicked window's ID, say for example that the printed window ID number is 11223344, knowing the ID number you can print the window name using the following code, 
```
xdotool getwindowname 11223344
```

This will print your windowname, knowing the windowname, replace every instance of windowname with the obtained name.

### App Name

In general, for any application, the app name is the name by which you usually use to call the app via terminal, and it is usually the same name with which you have installed the app. For example, the terminal in gnome, is called via gnome-terminal, then this is the app name. We replace the appname with the required name in the bash script.

### Keybinding


Knowing the windowname and the appname, we can rewrite the bash script using both names, and then creating a custom shrotcut in keyboard, where you just copy-paste the script in the command, and select your favored keyboard bindings to execute it. 

### Illustration

Check the following videl to see how to create the binding, 


## Special Case: In case of multiple ID for the same window name

Sometimes, for apps with multiple window ID, only one ID is the true user interface, and accordingly the above method would not execute properly, in order to obtain the true ID of the user interface of some window, the bash script is edited as in RoboustBashBinding.sh script.
