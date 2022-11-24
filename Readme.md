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

We will use the bash code to make a keyboard shortcut, which upon executing create a new instance of gnome-terminal if it does not exists, and it exists, it would focus it, and if it is focused, then it would minimize it the code is provided in the bashBinding.sh in the repository.

Instead of username@devicename in the bashBinding.sh script, replace it with your username, and device name, you can just open a new terminal manually, and find the username and device name if you already do not know them. The above script was executed in gnome, the terminal is called via ```gnome-terminal```, check the proper name of your terminal before using the above code, and replace "gnome-terminal" accordingly. 

In general, for any application, you can simply open a new instance, and then find the name of the window and replace it in place of "username@devicename", and then you have to know how this application is called via terminal (find the proper with which the application is executed via terminal). 

you just copy-paste the above script in your custom-shortcut, and create your favored keyboard bindings to execute it. Check the following screenshot to see how to create the binding, 


## Special Case: In case of multiple ID for the same window name

Sometimes, for apps with multiple window ID, only one ID is true user interface, and accordingly the above method would not execute properly, in order to obtain the true ID of the user interface of some window, the bash script is edited as in RoboustBashBinding.sh script.
