# Steps to run on RPi Ubuntu
---

- Install [Ubuntu Desktop for Raspberry Pi4](https://ubuntu.com/download/raspberry-pi)
- Remove bloatware 
  ```
  sudo apt-get remove --purge ‘libreoffice*’
  sudo apt-get clean
  sudo apt-get autoremove
  ```

- Set up virtual keyboard using Accessibility and `Improved OSK`
  - https://ubuntuhandbook.org/index.php/2022/05/enable-on-screen-keyboard-ubuntu-22-04/
  - https://www.youtube.com/watch?v=nyz6JEACIGM&t=204s
  - https://github.com/nick-shmyrev/improved-osk-gnome-ext
  - Notes:
    - Increase `Landscape Height in Percent` in settings of Improved OSK to see the Keyboard arrow, ctrl keys
  - Additional Resources:    
    - https://www.industrialshields.com/blog/raspberry-pi-for-industry-26/top-3-on-screen-virtual-keyboards-for-raspberry-plc-panel-pc-401

 - Setup rclone
    - `sudo -v ; curl https://rclone.org/install.sh | sudo bash`
    - https://rclone.org/dropbox/
    - `rclone copy SOURCE_PATH remote:/DESTINATION_PATH -P --dropbox-batch-mode=async --dropbox-batch-size 1000 --dropbox-batch-timeout 10s --checkers 28 --transfers 28 --tpslimit 12`
- Addional Resources
    - https://forum.rclone.org/t/suggestion-on-rclone-copy-terabytes-of-small-files-to-dropbox/24041/4
    - https://rclone.org/commands/rclone_rcat/
