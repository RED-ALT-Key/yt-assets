# Fix the Ubuntu Desktop Screen Resolution in Hyper-V
This fix allows one to set their Ubuntu Desktop VM to the host computer's monitor screen resolution.

## Edit grub using the Nano text editor
`sudo nano /etc/default/grub`

## Find the line that has this content
`GRUB_CMDLINE_LINUX="quiet splash"`

## Change it to the following state
`GRUB_CMDLINE_LINUX="quiet splash video=hyperv_fb:1920x1080"`

## Update Grub
`sudo update-grub`

## Restart the virtual machine
`sudo reboot now`