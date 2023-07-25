---
share: true
---
# What is Firmware?
"Firmware" is a technical term used to refer to software that's embedded in a hardware device. This is typically low-level software that interacts directly with the hardware to help control its functionality or serve as a bridge for higher-level software. For more information, see [this page](https://www.malwarebytes.com/cybersecurity/computer/what-is-firmware) .

# The Polaris OpenCore Firmware
The Polaris EVO Anima uses a custom firmware called [OpenCore](https://github.com/LamaDiLuce/polaris-opencore). Since 2020, OpenCore has been an open-source project maintaned on [GitHub](https://github.com), with contributors from all over the world! 

The firmware is updated periodically with new features and fixes. While not required, it is highly recommended that you keep your firmware up-to-date to enjoy features like [SmoothSwing](Sound%20Fonts.md#Standard%20vs.%20SmoothSwing) and [Quick Ignition](https://github.com/LamaDiLuce/polaris-opencore/pull/68).

## Who Created and Maintains the Firmware?
The original firmware was created by Lama di Luce, and is now maintaned as an open source project on GitHub. While the [Council](https://github.com/LamaDiLuce/polaris-opencore/wiki#council-members) oversees the development and official releases, anyone with coding knowledge can [contribute](https://github.com/LamaDiLuce/polaris-opencore/wiki#contributing)! Since it's open source, you can even [fork the repository](https://github.com/LamaDiLuce/polaris-opencore/fork) and create your own custom version, if you're so inclined.

# Downloading the Latest Firmware
The latest official release of the OpenCore firmware will always be posted on the GitHub repository [releases page](https://github.com/LamaDiLuce/polaris-opencore/releases). If necessary, you can also download all previous versions from this same page.

The most recent version will be at the top of the page, and will be marked with a "Latest" tag. The file you need to download is the one ending in `.hex`. This should be named something like `OpenCore.X.X.X_DDDDDDDD.hex`, where `X.X.X` is the version number and `DDDDDDDD` is the date it was released.

>[!info] Example Release Screenshot
>![](Pasted%20image%2020230504113002.png)

You don't need to download the source code unless you're a developer (or just curious).

# Updating the Firmware
The process for updating the firmware will vary slightly depending on which operating system you're using.

## Windows
The primary (and easiest) way to update the firmware on Windows is to use Gilthoniel. However, if you run into issues, you can also use the command line method.

### Gilthoniel
1. Download and install [Gilthoniel](Getting%20Started.md#Software), then [download the firmware update](#Downloading%20the%20Latest%20Firmware) you wish to install.
2. Turn the switch on your saber to the on position.
3. Connect the saber to your PC using a [good USB cable](Getting%20Started.md#Hardware).
4. Open Gilthoniel.

> [!warning] Error message
> ![Pasted image 20230504124514](img/Pasted%20image%2020230504124514.png)
> If you see an error message saying no sabers were detected, try the following:
> 1. Close Gilthoniel
> 2. Disconnect your saber
> 3. Turn the switch on your saber off, then back on
> 4. Reconnect your saber and try again
> 
> If you still see an error message, try a different USB cable and repeat as necessary. Animas are kind of picky about USB cables.

5. In the menu bar, click **Tools -> Update Firmware** from File.

![Pasted image 20230504140637](img/Pasted%20image%2020230504140637.png)

6. Select the `.hex` file you downloaded earlier.
7. A box will appear to confirm your choice. Click **Yes**.

![Pasted image 20230504141107](img/Pasted%20image%2020230504141107.png)

8. A command prompt window will appear. Type **Y**.

![Pasted image 20230504141329](img/Pasted%20image%2020230504141329.png)

9. Wait until the process is complete. Your saber will restart and you will see a message that says "Press any key to continue." Press any key to close the command prompt window.

Congratulations! Your firmware has been updated!

### Command Line
If for some reason the above steps don't work, or if you just want to try something different, you can also update the firmware from the command line.

> [!note]
> Functionally, this is identical to the Gilthoniel method. Gilthoniel just runs scripts that invoke the commands for you!

1. Download [tycmd.exe](Getting%20Started.md#Software), then [download the firmware update](#Downloading%20the%20Latest%20Firmware) you wish to install. Make sure they are both in the same folder (for example, your Downloads folder).
2. Open the Windows Command Prompt. Click on the search box and type `command`. Click on the "Command Prompt" icon.

![Pasted image 20230504142928](img/Pasted%20image%2020230504142928.png)

3. In the Command Prompt window, use the `cd` command to change to the folder where you downloaded the files. 
	- For example, if you saved them to your Downloads folder, you should be able to type `cd Downloads` and press **Enter**.
	- If you're having trouble finding the folder, see [this article](https://www.howtogeek.com/659411/how-to-change-directories-in-command-prompt-on-windows-10/) for more help.
4. Turn the switch on your saber to the on position.
5. Connect the saber to your PC using a [good USB cable](Getting%20Started.md#Hardware).
6. Type the following command, then press **Enter**:

```shell
tycmd.exe upload OpenCore.3.0.1_20230404.hex
```

> [!note]
> Replace `OpenCore.3.0.1_20230404.hex` with the name of the OpenCore firmware file you downloaded. In most versions of Windows, you can start typing the filename and then press **Tab** to auto-complete!

> [!warning] Error message
> If you see the message "No board available", try the following:
> 1. Disconnect your saber
> 2. Turn the switch on your saber off, then back on
> 3. Reconnect your saber and try again
> 
> If you still see an error message, try a different USB cable and repeat as necessary. Did I mention that Animas are picky about USB cables?

7. Wait for the command to finish. Your saber will restart. Don't worry if you see the "Failed to reset board" message at the end--everything is still working fine.

![Pasted image 20230504144726.png](img/Pasted%20image%2020230504144726.png)

Congratulations! Your firmware has been updated! You can close the Command Prompt now.

## MacOS
Unfortunately, Gilthoniel can't update saber firmware on Macs. Instead, we're going to have to use the Terminal. But don't worry; despite its name, it won't kill you! Probably.

1. Download [tycmd](Getting%20Started.md#Software), then [download the firmware update](#Downloading%20the%20Latest%20Firmware) you wish to install. Make sure they are both in the same folder (for example, your Downloads folder).
2. Open the Terminal app from the App Launcher (it may be in a group called "Other" or "Utilities"), or from Spotlight Search.
3. In the Terminal window, use the `cd` command to change to the folder where you downloaded the files. 
	- For example, if you saved them to your Downloads folder, you should be able to type `cd Downloads` and press **Enter**.
	- If you're having trouble finding the folder, see [this article](https://appletoolbox.com/navigate-folders-using-the-mac-terminal/) for more help.
4. Turn the switch on your saber to the on position.
5. Connect the saber to your PC using a [good USB cable](Getting%20Started.md#Hardware).
6. Type the following command, then press **Enter**:
```shell
chmod u+x tycmd
```

7. Now we have to do a little dance to tell macOS that `tycmd` is actually safe to use:
	- In Finder, open the folder where you downloaded the files.
	- Right-click on `tycmd`, then click "Open".
	- In the message box that appears (similar to the one below), click "Open".
	- You may briefly see a Terminal window flash open and then close itself. That's okay! That means it worked.

	![Pasted image 20230504152431](img/Pasted%20image%2020230504152431.png)

8. Back in the Terminal window, type the following command, then press **Enter**:
```shell
./tycmd upload OpenCore.3.0.1_20230404.hex
```

> [!note]
> Replace `OpenCore.3.0.1_20230404.hex` with the name of the OpenCore firmware file you downloaded. To save time, you can start typing the filename and then press **Tab** to auto-complete!

> [!warning] Error message
> If you see the message "No board available", try the following:
> 1. Disconnect your saber
> 2. Turn the switch on your saber off, then back on
> 3. Reconnect your saber and try again
> 
> If you still see an error message, try a different USB cable and repeat as necessary. Really, Animas are fairly picky about USB cables!

9. Wait for the command to finish. Your saber will restart. Don't worry if you see the "Failed to reset board" message at the end--everything is still working fine.

![Pasted image 20230504152738](img/Pasted%20image%2020230504152738.png)

Congratulations! Your firmware has been updated! You can close the Terminal now.

## Linux
Look, if you're using Linux, you probably already know what you're doing. But just in case, here's the quick instructions.

1. Download [tytools](https://koromix.dev/tytools) and build according to the instructions.
2. [Download the firmware update](#Downloading%20the%20Latest%20Firmware) you wish to install.
3. From the command line, `cd` to the directory where you saved the `.hex` file.
4. Turn the switch on your saber to the on position.
5. Connect the saber to your PC using a [good USB cable](Getting%20Started.md#Hardware).
6. Run this command, replacing the filename with the correct version:

```bash
tycmd upload OpenCore-XXXX.hex
```

7. Wait for the command to finish. Your saber will restart. Don't worry if you see the "Failed to reset board" message at the end--everything is still working fine.

> [!warning] Error message
> If you see the message "No board available", try the following:
> 1. Disconnect your saber
> 2. Turn the switch on your saber off, then back on
> 3. Reconnect your saber and try again
> 
> If you still see an error message, try a different USB cable and repeat as necessary. Seriously, picky picky Animas.

Congratulations! Your firmware has been updated!