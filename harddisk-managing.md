# Some really useful commands for Managing Harddisks
# Linux

* Show a List of all Partions
  ```
    $ fdisk -l
  ```

* Check if the partion is healthy
  ```
    $ sudo fsk /dev/PARTION_NAME
    ex:
    sudo fsck /dev/sda1
  ```
* Copy all bytes from one harddisk to another
  ```
    $ sudo dd if=INPUT_FILE(PATH) of=OUTPUT_FILE(PATH) bs=4M status=progress 
    ex:
    sudo dd if=/dev/sda of=/dev/sdb bs=4M status=progress
  ```