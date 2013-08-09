                                    Instructions for burning Xboot and complete Android Image via Micro SD Card
                                    ===========================================================================

   a. Insert a 2G or 8G Micro SD card into PC;

   b. $ cd $TOP/device/ingenic/npm801/burner;

   c. Run burn.sh followed the path of your TF card as argument. 
      For example: sudo ./burn.sh /dev/sdc. 
      Be careful of the device node, this step will
      format the Micro SD card!!!

   d. Eject the Micro SD card and reinsert into PC;

   e. cp config.txt /media/XXX/;

   f. Choose one of the following steps (1 or 2):

      1. To just flash XBoot:
         -------------------
         cp burning_list_forxboot.txt /media/XXX/burning_list.txt;

      2. To flash XBoot, system, and boot images:
         ---------------------------------------
         cp burning_list_forall.txt                     /media/XXX/burning_list.txt;
         cp $TOP/out/target/product/npm801/boot.img     /media/XXX/
         cp $TOP/out/target/product/npm801/system.img   /media/XXX/

      NOTE: Be careful and make sure in the above cp that the file name 
      ====  is changed to burning_list.txt. 

            It's a common mistake to do something like:
                    cp burning_list_forall.txt   /media/XXX/

            and end up with the incorrect file name on the Micro SD Card.

   g. cp x-boot-nand.bin /media/XXX;

   h. Unmount it;

   i. Insert the TF card into device;

   j. Press vol- and do a reset.

NOTE: Keep vol- pressed until you see the boot logo(A green Android robot).



