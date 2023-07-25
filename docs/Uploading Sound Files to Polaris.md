---
share: true
---
# Uploading Sound Files to Polaris
Now that you've got your [sound files converted](Converting%20Sound%20Files%20for%20Polaris.md) to `.RAW` format, you're ready to send them to your saber! Again, there are a couple different ways to do this, and we'll cover multiple options. 

No matter how you do it, there are basically two steps. First, you'll send the files to the saber. Then you will assign the files to the right effects in Gilthoniel.

# Anima Files and Free Space
Before we start, here's a quick note about how the Anima EVO stores files and reports space. It works more or less like a typical computer file system, *except* when it comes to deleting files and reclaiming space.

On a computer, when you delete a file, the system removes the file more or less immediately and makes the space that the file used available for other things. In other words, it gets rid of the file and gives you the space back. When you overwrite a file (that is, save over it with a file of the same name), your computer essentially gets rid of the old file and puts the new one in the same space--so it again reuses the space that the old file was using.

When you "delete" a file from the Anima, it marks the file for deletion but it *doesn't actually free up the space.* The Anima says the file is gone, but it's still taking up the same space in memory. The same thing happens when you overwrite a file: the old file doesn't go away, so you have basically two copies taking up space, even though it's only actively "using" one. ***The Anima doesn't actually free up memory until you send it the `ERASE=ALL` command.***

Since the Anima has a very limited memory (only 16 MB), this can be very frustrating if you don't understand it. Until I figured this out, I personally got very frustrated when I kept "deleting" files only to be told that the Anima still had no free space!

> [!tip] TL;DR
> Make sure you erase the Anima before sending any new files to it.

# Uploading Files
As you've probably come to expect by now, there is (sometimes) a way to do this graphically and also a way to do this from the command line. At the moment, I recommend the command line as being the most reliable.

## Gilthoniel
In theory, you can use Gilthoniel to upload sound files to your saber. I say "in theory," because this currently doesn't work for many people for reasons that are not clear. However, if you're one of the lucky ones for whom it works, Gilthoniel makes it easy!

> [!note] Windows and Mac
> The steps are the same for this method whether you're using Windows or macOS. The screenshots below show Windows, but the steps are identical for Macs. For Linux users, Gilthoniel runs well under WINE.

### Erase Existing Files
Before uploading new files, it's always recommended to erase the existing ones. This is because of [the way the Anima reclaims storage space](#Anima%20Files%20and%20Free%20Space). You will then have to re-upload all files, but this is the best way to ensure everything is correct and stable.

> [!warning]
> This will erase all the sounds on your saber. Your saber will have NO sounds until you reload the files. Be sure your new sound files are ready before taking these steps!

1. Turn the switch on your saber to the on position.
2. Connect the saber to your PC using a [](Getting%20Started.md#Hardware%7Cgood%20USB%20cable).
3. Open [](Getting%20Started.md#Software%7CGilthoniel).

> [!warning] Error message
> ![Pasted image 20230504124514](Pasted%20image%2020230504124514.png)
> If you see an error message saying no sabers were detected, try the following:
> 1. Close Gilthoniel
> 2. Disconnect your saber
> 3. Turn the switch on your saber off, then back on
> 4. Reconnect your saber and try again
> 
> If you still see an error message, try a different USB cable and repeat as necessary. Animas are kind of picky about USB cables.

4. Click on the **Sounds** tab, then click the **Delete Files** button.

![Pasted image 20230718120454](Pasted%20image%2020230718120454.png)

5. A confirmation dialog will appear. Click **Yes**.

![Pasted image 20230718120625](Pasted%20image%2020230718120625.png)

6. ANOTHER confirmation dialog will appear. Click **Yes** again.

![Pasted image 20230718120722](Pasted%20image%2020230718120722.png)

The debug panel on the right will show the progress. It will take a couple minutes.

![Pasted image 20230718120903](Pasted%20image%2020230718120903.png)

Eventually, you will see two lines saying, "OK, Now re-load your sound files," and "OK, Serial Flash Erased.":

![Pasted image 20230718121008](Pasted%20image%2020230718121008.png)

Congratulations! You're ready to upload your new files!

### Upload New Files
As mentioned above, this option does not work for many people in Gilthoniel. The reasons are unknown at this time. I've never been able to get it to work, personally, but maybe you'll be lucky!

To upload files, click the **Sounds** tab, then the **Upload Files** button.

![Pasted image 20230718121739](Pasted%20image%2020230718121739.png)

> [!error]
> If your **Upload Files** button is greyed out (as is mine in the screenshot), this method won't work. You'll have to use the command line instructions below.

Sadly, I can't give you step-by-step instructions or screeenshots from here, since I can't get it to work! But if it works for you, it should be relatively straightforward to follow the prompts.

After the files are uploaded, make sure you assign them to the right effects.

## Command Line
It's your old pal the command line! The steps here are slightly different depending on your OS.

> [!note]
> These instructions use the `py2saber` command, which is my own re-implementation of Nuntis' `sendtosaber`. I've deliberately designed `py2saber` to be interoperable with `sendtosaber`. This means that, if you prefer, you can mostly replace `py2saber` in the instructions with `sendtosaber`. The main difference is that `sendtosaber` only lets you upload one file at a time; you'll have to issue a separate command for each file or use a batch script.

### Windows
It's command line time! Hooray!

1. Download [](Getting%20Started.md#Software%7Cpy2saber.exe). Place the file in the same folder as your `.RAW` [sound files](Converting%20Sound%20Files%20for%20Polaris.md).
2. Open the Windows Command Prompt. Click on the search box and type `command`. Click on the "Command Prompt" icon.

![Pasted image 20230504142928](Pasted%20image%2020230504142928.png)

3. In the Command Prompt window, use the `cd` command to change to the folder where you downloaded the files. 
	- For example, if you saved them to your Downloads folder, you should be able to type `cd Downloads` and press **Enter**.
	- If you're having trouble finding the folder, see [this article](https://www.howtogeek.com/659411/how-to-change-directories-in-command-prompt-on-windows-10/) for more help.
4. Turn the switch on your saber to the on position.
5. Connect the saber to your PC using a [](Getting%20Started.md#Hardware%7Cgood%20USB%20cable).

First, we need to erase the existing files on the saber.

> [!warning]
> This will erase all the sounds on your saber. Your saber will have NO sounds until you reload the files. Be sure your new sound files are ready before taking this step!

6. Type the following command, then press **Enter**:

```shell
py2saber.exe --erase-all
```

You will see the following message:

![Pasted image 20230718150318](Pasted%20image%2020230718150318.png)

7. Type **Y** and press **Enter**. The saber will begin to erase. 

You will see several rows of # signs appear as the program progresses. When the process is complete, you will see the following:

![Pasted image 20230718150546](Pasted%20image%2020230718150546.png)

Your saber is erased and ready for your new sound files!

7. Type the following command, then press **Enter**:

```shell
py2saber.exe *.RAW
```

>[!note]
>This will copy all `.RAW` files in the current folder to your saber. If you only want to upload certain files, you can specify one or more filenames (separated by spaces) instead of `*.RAW`. 
>
>For example: `py2saber.exe HUM_0.RAW POWERON_0.RAW POWEROFF_0.RAW`

Your files will begin copying to the saber. You will see a screen similar to the following:

![Pasted image 20230718161858](Pasted%20image%2020230718161858.png)

Once the command completes, your new files will be ready! Make sure you assign them to the right effects in Gilthoniel.

### macOS
The process for using the command line in macOS is very similar. Here we go!

1. Download and install [](Getting%20Started.md#Software%7Cpy2saber).
2. Open the Terminal app from the App Launcher (it may be in a group called "Other" or "Utilities"), or from Spotlight Search.
3. In the Terminal window, use the `cd` command to change to the folder where your `.wav` files are located. 
	- For example, if you saved them to your Downloads folder, you should be able to type `cd Downloads` and press **Enter**.
	- If you're having trouble finding the folder, see [this article](https://appletoolbox.com/navigate-folders-using-the-mac-terminal/) for more help.
4. Turn the switch on your saber to the on position.
5. Connect the saber to your PC using a [](Getting%20Started.md#Hardware%7Cgood%20USB%20cable).

First, we need to erase the existing files on the saber.

> [!warning]
> This will erase all the sounds on your saber. Your saber will have NO sounds until you reload the files. Be sure your new sound files are ready before taking this step!

6. Type the following command, then press **Enter**:

```shell
py2saber --erase-all
```

You will see the following message:

![Pasted image 20230724160300](Pasted%20image%2020230724160300.png)

7. Type **Y** and press **Enter**. The saber will begin to erase. 

You will see several rows of # signs appear as the program progresses. When the process is complete, you will see the following:

![Pasted image 20230724160504](Pasted%20image%2020230724160504.png)

Your saber is erased and ready for your new sound files!
8. Type the following command and press **Enter**:

```shell
py2saber *.RAW
```

>[!note]
>This will copy all `.RAW` files in the current folder to your saber. If you only want to upload certain files, you can specify one or more filenames (separated by spaces) instead of `*.RAW`. 
>
>For example: `py2saber HUM_0.RAW POWERON_0.RAW POWEROFF_0.RAW`

Your files will begin copying to the saber. You will see a screen similar to the following:

![Pasted image 20230724160611](Pasted%20image%2020230724160611.png)

Once the command completes, your new files will be ready! Make sure you assign them to the right effects in Gilthoniel.

### Linux
You can probably figure this out from the above info, but just in case...

1. Turn the switch on your saber to the on position.
2. Connect the saber to your PC using a [](Getting%20Started.md#Hardware%7Cgood%20USB%20cable).
3. Make sure [Python 3](https://www.python.org/) is installed on your system. Refer to [the Python beginner's guide](https://wiki.python.org/moin/BeginnersGuide/Download) your distribution's documentation for instructions.

> [!warning]
> These instructions assume `pip` and `python` are symlinked to `pip3` and `python3`. This is usually the case in most modern systems. If you also have Python 2 installed, you may need to replace `pip` and `python` in these instructions with `pip3` and `python3`, respectively.

4. Get thee to a command line!
5. Clone the py2saber [Git repo](https://github.com/jramboz/py2saber) and `cd` into the directory:

```shell
git clone https://github.com/jramboz/py2saber.git
cd py2saber
```

6. Install the required libraries:

```shell
pip install -r requirements.txt
```

7. Erase all files currently on the saber:

```shell
python py2saber.py --erase-all
```

8. Upload the new files (replacing the path to the files as necessary):

```shell
python py2saber.py /path/to/sound/files/*.RAW
```

Success! Go on to the next section for assigning sounds in Gilthoniel.

# Assigning Sounds in Gilthoniel
If you used the [](Converting%20Sound%20Files%20for%20Polaris.md#Sound%20File%20Names%7Cdefault%20file%20naming%20scheme), this step is mostly optional. The default filenames should automatically be mapped to the right effects, with one exception that we'll discuss below. If you've used non-standard names or added [](Converting%20Sound%20Files%20for%20Polaris.md#^96a336%7Cadditional%20sounds%20for%20some%20effects), you will need to perform these steps for the Anima to recognize them.

> [!note]
> These instructions work the same on Windows or Mac (or Linux using WINE).

1. With your saber connected and turned on, open [](Getting%20Started.md#Software%7CGilthoniel).
2. Go to the Sounds tab. You will see a screen similar to the following:

![Pasted image 20230724170213](Pasted%20image%2020230724170213.png)

>[!question] What the heck am I looking at?
>This screen can be a little bit intimidating at first. But, as a wise man once said, don't panic! It's actually pretty straightforward.
> 
>Each box in this tab corresponds to a type of sound effect. For example, Power On sounds, Clash sounds, Swing sounds, etc. Inside the box is a list of all the files available on the saber, with a check box next to each. If the box is checked, the Anima will use that file for the corresponding sound effect. If multiple boxes are checked, then the Anima will randomly choose one each time the effect is invoked.
> 
>If a file name has a double asterisk (\*\*) next to it, that means that the Anima expects the files to be there (because it is part of the [](Converting%20Sound%20Files%20for%20Polaris.md#Sound%20File%20Names%7Cdefault%20naming%20scheme)) but no file with that name is present on the saber. This is usually because your sound font doesn't include these files. It's okay to ignore this!

3. In each box, put a check mark next to the sound files you wish to use for that effect.

>[!note] Note on SmoothSwing and Standard Swing Files
>The box labeled "Swing Sounds" is sound files for Standard Swing fonts. "Smooth Swing A" is the "high" sound for SmoothSwing fonts, while "Smooth Swing B" is the "low" sound.
>
>If you have both [](Sound%20Fonts.md#Standard%20vs.%20SmoothSwing%7CSmoothSwing%20and%20Standard) files on your saber, the Anima will by default use SmoothSwing. You can leave the "Swing Sounds" boxes checked, however; it will have no effect.

> [!tip] Double-Check SmoothSwing Files!
> Remember above when I said that this step is "mostly optional" if you've used the default names? Here's the "mostly." For some reason, the Anima seems to default to using the SmoothSwing "high" files for both Smooth Swing A and B. This of course won't give you nearly as cool a SmoothSwing effect!
>  
>  In the "Smooth Swing B" box, make sure you *uncheck* the `SMOOTHSWINGH` files and *check* the `SMOOTHSWINGL` ones!

4. When you're finished assigning the files in each box, click the **Disconnect/Save** button.

That's it! After all that, you're done! Test out your new saber sounds and see what you think. If something's not working as expected, go back and repeat these steps. If it still doesn't work, please [](Getting%20Started.md#Troubleshooting%20and%20Getting%20Help%7Creach%20out%20for%20help).

Now go out, enjoy your new sounds, and [Spread the Light](http://lludosport.net)!