# Lost root password in Ubuntu

An issue with root's lost password - 
Solution:
 - Reboot your computer
 - Hold Shift during boot to start GRUB menu
 - Highlight your image and press E to edit
 - Find the line starting with "linux" and append rw init=/bin/bash at the end of that line
 - Press Ctrl+X to boot.
 - Type in passwd username
 - Set your password.
 - Type in reboot. If that doesn't work, hit Ctrl+Alt+Del


Bonus: to add yourself in sudoers you need root password and add yourself in visudo
