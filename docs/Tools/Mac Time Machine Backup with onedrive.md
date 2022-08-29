
# My successful steps on Mac Pro (Late 2013), MacOS Big Sur
Created and performed: 2022-08-08
Tags: #fundamental-skill; #data-managment 

1.  Go to the “**Launchpad” -> “Disk Utility”
2. Click on the “**file**” tab from the top menu bar of Disk Utility and click on “New Image” > “Blank Image”
3.  Fill out the name for “**backup-macpro-onedrive**” and set a location for the new image.
	>![[Pasted image 20220808214539.png]] - **Name the virtual disk, set a size equivalent to the amount of storage present within your current disk.**
	 >- Set format to “Mac OS Extended (Journaled)”.
	 >-  Now set encryption to “128-bit AES encryption (recommended)”. At this point, you may be asked for a password. This will be your computer password
-   Set partition to “Single partition – Apple Partition Map”.
-   Set Image format to “sparse bundle disk image”.
-   Then click on “Save”.
 >![[Pasted image 20220808214555.png]]
 ![[Pasted image 20220808214607.png]]

15.  **Now close the utility panel and use the launcher to open “Terminal”.**
16.  **In the terminal command block type out: 

	> cd /Volumes
	> diskutil list
	> sudo diskutil enableOwnership /dev/disk3s2
	> sudo tmutil setdestination /Volumes/backup-macpro-onedrive/

9.  **Now close the terminal.**
10.  **A new virtual port has been created for your virtual TM drive.**
11.  **Now in the launcher open “System preferences”**
12.  **Click on “Time Machine”.**
13.  **Click on “Options” Your newly created virtual time machine is here,** 
14.  **Click the “+” symbol.**
15.  **From the list of applications, select “OneDrive”.**
16.  **Click on “Exclude”.**
17.  **Now click on “Save”.**

Resources:
	[How to use OneDrive to store a Time Machine backup](https://businesstechplanet.com/how-to-use-onedrive-to-store-a-time-machine-backup/)
	[Using Time Machine on unsupported volumes](http://hints.macworld.com/article.php?story=20140415132734925)