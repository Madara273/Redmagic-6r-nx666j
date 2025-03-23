# Redmagic-6r-nx666j

METOD1

**Disclaimer:** I am not liable for any damage to your device, so proceed at your own risk. These instructions will only work if you have the necessary skills and experience with adb fastboot and edl mode.

**Instructions:**

1. Download the unlocking tool

2. Launch the unlocking tool program.

3. The next step is to put your RedMagic 6R device into EDL mode.

4. To do this, you need to install adb fastboot and the QUALCOMM HS-USB QDLoader 9008 driver on your computer.

5. Connect the device and enter the command -- adb reboot edl --

6. In the unlocking tool window of connected ports, you will see COM (port number) QUALCOMM HS-USB QDLoader 9008.

7. Select the UFS type in the firehose parameter, navigate to the directory where the firehoseRM6R.elf file is located, select it, and press READ GPT or BOOT DEVICE - depends on the version of the unlocking tool

8. Then, you will see general information about the device and the partitions that can be flashed.

9. Find LUN4 and select boot_b, right-click and choose "write (boot_b.img)". Find the corrected boot.img in the file manager and press "download".

11. Do the same with vbmeta_b in LUN4, but with the corresponding corrected vbmeta.img.

12. That's it! Your RedMagic 6R device is now rooted. Press "reboot" in the unlocking tool and wait for your phone to boot up.

--------------------------------------------------------------------------------------------------------------------------

METOD2

--Warning--

  don't use this if you are a newbie, I am not responsible for your broken devices.  This app is dangerous for small users which can cause your device to crash completely, in that case only unbrick tool and jtag programmer will help you.

  1_step -- install [ Unofficial Qualcomm Firehose / Sahara / Streaming / Diag Tools :) ]

  --note -- just copy this text -- (Unofficial Qualcomm Firehose / Sahara / Streaming / Diag Tools :)) -- and paste into the search engine - go to github developer and install the program depending on your OS.

  2_step -- connect the device to your computer or other phone in edl mode and run the command --lsusb-- you see something in the device image ******* 9008. then put your device into edl mode by typing the command adb reboot edl
  If you see it, go to step 3.

  3_step -- execute a series of commands:

  edl w boot_b kitsune_patched.img --loader=firehoseRM6R.elf --memory=ufs --lun=4

  edl w vbmeta_b patch-vbmeta.img --loader=firehoseRM6R.elf --memory=ufs --lun=4

  Step 4 -- Unplug the device from usb and restart your device by holding the power button until you hear a vibration.

  that's all your device is rooted.

-- note -- all files must be in one folder for ease of entering commands, if you change the location of files from the archive, then specify the path to each file accordingly!
