# Switching between BitCurator and Windows

The following instructions describe the steps required to switch between BitCurator and Windows on the Digital Archives Lab computers. Both Dell computers have both BitCurator and Windows installed.

### To switch from BitCurator to Windows:

1. Click the **Settings** icon in the very top-right corner of the BitCurator desktop.
2. From the drop-down menu, select **Shut Down...**
3. Click the large **Restart** button.
4. Pay attention as the computer restarts. As soon as you see the Dell boot screen, hit **F12**. You should see the message **Preparing one-time boot menu** in yellow in the upper right hand corner.
5. Use the arrow keys to scroll to **Windows Boot Manager** and hit **enter**.
6. Windows will boot. Log-in as normal.

### To switch from Windows to BitCurator:

1. Click the **Windows** icon in the very bottom-left corner of the Windows desktop.
2. Click the **On/Off** icon and select **Restart**.
3. Pay attention as the computer restarts. As soon as you see the Dell boot screen, hit **F12**. You should see the message **Preparing one-time boot menu** in yellow in the upper right hand corner.
4. Use the arrow keys to scroll to **ubuntu** and hit **enter**.
5. Use the arrow keys to scroll to **BitCurator-1.8.12 GNU/Linux** and hit **enter**.
6. After a few minutes, you will be prompted to enter a log-in username. Type the BitCurator user name and hit **enter**.
7. You will be prompted for a password. Type the BitCurator password and hit **enter**.
8. Hit the up arrow key until you see the following command

	```sudo mount -o remount,rw '/dev/sda2' ```
	
9. Hit **enter**.
10. Hit the up arrow key until you see the following command:
	
	```sudo service lightdm start```
	
11. Hit **enter**. The BitCurator GUI will launch.

**Note**: 
On the right computer, the steps are a bit different. 

### To switch from BitCurator to Windows (right computer):

1. Click the **Settings** icon in the very top-right corner of the BitCurator desktop.
2. From the drop-down menu, select the **Power button**
3. Click the **Restart** button in the middle.
4. Pay attention as the computer restarts. As soon as you see the Dell boot screen, hit **F12**. You should see the message **Preparing one-time boot menu** in yellow in the upper right hand corner.
5. Use the arrow keys to scroll to **UEFI: SK hynix SH920 2.5 7MM 256GB** and hit **enter**.
6. Windows will boot. Log-in as normal.

### To switch from Windows to BitCurator (right computer):

1. Click the **Windows** icon in the very bottom-left corner of the Windows desktop.
2. Click the **On/Off** icon and select **Restart**.
3. Pay attention as the computer restarts. As soon as you see the Dell boot screen, hit **F12**. You should see the message **Preparing one-time boot menu** in yellow in the upper right hand corner.
4. Use the arrow keys to scroll to **ubuntu** and hit **enter**.
5. Use the arrow keys to scroll to **UEFI: Samsung SSD 850 EVO 250GB** and hit **enter**.
6. The next page will ask what system you want. Using the arrow keys, scroll to **ubuntu** and hit **enter**
7. After a few minutes, you will be prompted to choose the BitCurator profile. Hit **enter**.
8. You will be prompted for a password. Type the BitCurator password and hit **enter**. The BitCurator GUI will launch.
