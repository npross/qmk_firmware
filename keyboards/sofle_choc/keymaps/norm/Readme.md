
# Install WSL

In an administrator powershell window run: 
    
    wsl --install

## Install the latest QMK for WSL distro

https://github.com/qmk/qmk_distro_wsl 

in the start menu run the QMK WSL shortcut

## Setup ssh keys

    sudo apt install ssh
    ssh-keygen
    
Copy the contents of ~/id_rsa.pub to the clipboard and paste into the SSH key on github

## Clone the qmk_firmware
    git clone git@github.com:npross/qmk_firmware.git
    git checkout choc2

then run `qmk setup`

## Building and flashing the firmware

    qmk compile -kb sofle_choc -km norm -e CONVERT_TO=kb2040
    sudo mount -t drvfs F: /mnt/f
<<<<<<< Updated upstream
    # reset the controller (double click the resetS)
=======
    # reset the controller (double click the reset)
>>>>>>> Stashed changes
    cp sofle_choc_norm_kb2040.uf2 /mnt/f
    


Links:
* https://qmk.github.io/qmk_distro_wsl/guide.html

I