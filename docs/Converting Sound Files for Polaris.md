---
share: true
---
# Sound File Formats
The Polaris Anima EVO uses a sound format that's different from the one used by the majority of lightsaber boards on the market. Most [[Sound Fonts]] that you'll find have their files in `.wav` format, but the Polaris requires `.RAW` files. Don't worry, though! Converting from `.wav` to `.RAW` is a little tricky, but not too difficult.

## Polaris Audio Format Specifications
For those audiophiles who are already familiar with audio files (see what I did there?), below are the detailed file requirements for Polaris sounds. Also refer to the [[#Sound File Names]] section for the proper naming scheme.

> [!tip] Polaris Audio Format Specifications
> **Format:** RAW
> **Channels:** 1 (Mono)
> **Bit Depth**: 16 bit
> **Sample Rate**: 44.1kHz
> **Total Size of All Files:** 16 MB or less

^d318ef

If the above means nothing to you, don't worry! You'll see how to do the magic step-by-step below.

# Sound File Names
In order for the Anima to recognize which file is which, they need to have specific filenames. 

In the steps below, we'll (optionally) be using some batch scripts to convert all the sounds at once. For these to work correctly, you'll need to name your `.wav` files according to the "Input Filename" columns below. There are two conversion scripts--one for CFX-formatted sound fonts, one for Proffie--and each require slightly different filenames. You can use either one, just make sure you name your files according to the appropriate column. 

If you're not using the scripts or manually converting your files, just make sure that the final `.RAW` filenames match the "Output Filename" column.

| Sound Description | Input Filename (CFX) | Input Filename (Proffie) | Output Filename |
|--------------------|----------------------|------------------------|------------------|
| Hum | `hum.wav` | `hum01.wav` | `HUM_0.RAW` |
| Power On (Ignition) | `poweron.wav` | `out01.wav` | `POWERON_0.RAW` <sup>[[#^96a336\|2]]</sup> |
| Power Off (Deactivation) | `poweroff.wav` | `in01.wav` | `POWEROFF_0.RAW` <sup>[[#^96a336\|2]]</sup> |
| Clash 1 <sup>[[#^431156\|1]]</sup> | `clash1.wav` | `clsh01.wav` | `CLASH_1_0.RAW` |
| Clash 2 | `clash2.wav` | `clsh02.wav` | `CLASH_2_0.RAW` |
| Clash 3 | `clash3.wav` | `clsh03.wav` | `CLASH_3_0.RAW` |
| Clash 4 | `clash4.wav` | `clsh04.wav` | `CLASH_4_0.RAW` |
| Clash 5 | `clash5.wav` | `clsh05.wav` | `CLASH_5_0.RAW` |
| Clash 6 | `clash6.wav` | `clsh01.wav` <sup>[[#^64849a\|3]]</sup> | `CLASH_6_0.RAW` |
| Clash 7 | `clash7.wav` | `clsh02.wav` | `CLASH_7_0.RAW` |
| Clash 8 | `clash8.wav` | `clsh03.wav` | `CLASH_8_0.RAW` |
| Clash 9 | `clash9.wav` | `clsh04.wav` | `CLASH_9_0.RAW` |
| Clash 10 | `clash10.wav` | `clsh05.wav` | `CLASH_10_0.RAW` |
| Swing 1 ([[Sound-Fonts#Standard vs. SmoothSwing|Standard]]) <sup>[[#^431156\|1]]</sup> | `swing1.wav` | `swng01.wav` | `SWING_1_0.RAW` <sup>[[#^ecf238\|4]]</sup>|
| Swing 2 (Standard) | `swing2.wav` | `swng02.wav` | `SWING_2_0.RAW` |
| Swing 3 (Standard) | `swing3.wav` | `swng03.wav` | `SWING_3_0.RAW` |
| Swing 4 (Standard) | `swing4.wav` | `swng04.wav` | `SWING_4_0.RAW` |
| Swing 5 (Standard) | `swing5.wav` | `swng05.wav` | `SWING_5_0.RAW` |
| Swing 6 (Standard) | `swing6.wav` | `swng06.wav` | `SWING_6_0.RAW` |
| Swing 7 (Standard) | `swing7.wav` | `swng07.wav` | `SWING_7_0.RAW` |
| Swing 8 (Standard) | `swing8.wav` | `swng08.wav` | `SWING_8_0.RAW` |
| [[Sound-Fonts#Standard vs. SmoothSwing|SmoothSwing]] 1 (Low) <sup>[[#^431156\|1]]</sup> | `lswing1.wav` | `swingl01.wav` | `SMOOTHSWINGL_1_0.RAW` <sup>[[#^ecf238\|4]]</sup> |
| SmoothSwing 1 (High) | `hswing1.wav` | `swingh01.wav` | `SMOOTHSWINGH_1_0.RAW` |
| SmoothSwing 2 (Low) | `lswing2.wav` | `swingl02.wav` | `SMOOTHSWINGL_2_0.RAW` |
| SmoothSwing 2 (High) | `hswing2.wav` | `swingh02.wav` | `SMOOTHSWINGH_2_0.RAW` |
| SmoothSwing 3 (Low) | `lswing3.wav` | `swingl03.wav` | `SMOOTHSWINGL_3_0.RAW` |
| SmoothSwing 3 (High) | `hswing3.wav` | `swingh03.wav` | `SMOOTHSWINGH_3_0.RAW` |
| SmoothSwing 4 (Low) | `lswing4.wav` | `swingl04.wav` | `SMOOTHSWINGL_4_0.RAW` |
| SmoothSwing 4 (High) | `hswing4.wav` | `swingh04.wav` | `SMOOTHSWINGH_4_0.RAW` |
| SmoothSwing 5 (Low) | `lswing5.wav` | `swingl05.wav` | `SMOOTHSWINGL_5_0.RAW` |
| SmoothSwing 5 (High) | `hswing5.wav` | `swingh05.wav` | `SMOOTHSWINGH_5_0.RAW` |
| SmoothSwing 6 (Low) | `lswing6.wav` | `swingl06.wav` | `SMOOTHSWINGL_6_0.RAW` |
| SmoothSwing 6 (High) | `hswing6.wav` | `swingh06.wav` | `SMOOTHSWINGH_6_0.RAW` |
| SmoothSwing 7 (Low) | `lswing7.wav` | `swingl07.wav` | `SMOOTHSWINGL_7_0.RAW` |
| SmoothSwing 7 (High) | `hswing7.wav` | `swingh07.wav` | `SMOOTHSWINGH_7_0.RAW` |
| SmoothSwing 8 (Low) | `lswing8.wav` | `swingl08.wav` | `SMOOTHSWINGL_8_0.RAW` |
| SmoothSwing 8 (High) | `hswing8.wav` | `swingh08.wav` | `SMOOTHSWINGH_8_0.RAW` |

## Notes on Filenames
Here are some notes and gotchas regarding file naming.

> [!info] Note 1: Number of Files
> Many effects have multiple files. The Anima will randomly choose between them when an event occurs. *If you have more or fewer files* in your sound font than what the firmware expects, don't worry! 
> 
> If you have fewer, you can have multiple copies of the same file with different filenames (e.g., copy `clash1.wav` and rename it `clash10.wav`). You can just leave out the ones you don't have and uncheck them in Gilthoniel.
> 
> If you have more, you can manually convert the extras and upload them to your saber. Make sure to check the extras in Gilthoniel. Note, however, that the total size of all files must be less than 16 MB.

^431156

> [!info] Note 2: Multiple Power On/Off Sounds
> By default, the firmware only expects one sound each for Power On and Off. However, it does have the ability to support multiple options! If you want multiple options for each, name them as `POWERON_1.RAW`, `POWERON_2.RAW`, etc. Make sure to check the appropriate boxes in Gilthoniel. Also keep in mind that the total size of all files must be less than 16 MB.

^96a336

> [!info] Note 3: Proffie Clash Repetition
> The Proffie conversion script expects to re-use `clsh01.wav` - `clsh05.wav` for Clashes 6 - 10. I'm not sure if that's typical for Proffie sabers, or just an odd quirk. If you have more than 5 clash files, you can manually convert them or alter the script.

^64849a

> [!info] Note 4: Standard and SmoothSwing Files
> You only need one or the other of the Standard or SmoothSwing files, not both. If you're using SmoothSwing, you can skip the Standard files, and vice versa. This can be especially useful in keeping the total file size under the 16 MB limit. If you have both, the Anima will use the SmoothSwing ones by default, and there's no harm in having the Standard ones as well. I'm hopeful that future version of the firmware will support using these as "swing accents!".

^ecf238

> [!info] Note 5: Filenames and the Firmware
> Technically, *technically*, I think you can name the `.RAW` files whatever you want. You just have to mark them under the right places in Gilthoniel and *theoretically* it will still work. However, I've heard anecdotally from people who have tried this that it tends to be hit-or-miss; sometimes alternate filenames work and sometimes they don't. In any event, I recommend using the expected filenames: it Just Works&trade;

> [!info] Note 6: Additional Sound Font Files (Pew! Pew!)
> Sound fonts created for other lightsaber boards may have additional sound files, including blaster deflections, drags, lockups, spins, etc. The Polaris Anima EVO doesn't currently support these sounds, and you can safely ignore them.

# Windows Conversion Instructions
Since most of you are using Windows, let's start there!

## Preparing for Conversion
Before we begin, we need to get everything set up properly to make the conversion as smooth as possible. 

> [!note] Working with Files and Folders
> For the purposes of these instructions, I assume you already know the basics of [working with files and folders](https://edu.gcfglobal.org/en/windowsbasics/working-with-files/1/) in Windows, including [how to extract zip files](https://www.pcworld.com/article/394871/how-to-unzip-files-in-windows-10.html). If you need a refresher on these tasks, see the links.

1. Download [[Getting Started#Software|SoX for Windows]] from the Polaris-Opencore Github Repository. Extract the `.zip` file somewhere handy, for example your Downloads folder. It should look something like this:

![Pasted image 20230516155555.png](Pasted%20image%2020230516155555.png)

2. Download your preferred [[Sound Fonts|sound font]] and extract the files to a convenient folder.
3. Locate the `.wav` sound files.

> [!note] 
> Depending on where you got your sound font, you may find that your download contains sub-folders with names like CFX, ProffieOS, Xenopixel, etc.  In each of these folders will be sets of `.wav` files, sometimes in further subfolders. These are files configured for [[Sound Fonts#Supported Saber Models (CFX, Proffie, Xeno, etc.)|various commercial lightsaber boards]]. Any one will do the job. If you're confused, I find CFX to usually be the easiest to work with, since it puts all the files in one folder.

> [!tip]
> If you don't see that your filenames all end in `.xxx` (a period followed by three characters), I recommend showing file name extensions in Windows. In File Explorer, click the View tab, then check the box next to "File name extensions". This will make it much easier to locate the right types of files and rename them appropriately!

4. Copy all the `.wav` files you want to convert to the folder where you extracted SoX. Make sure they are in the same folder as the `.cmd` files (e.g., `convert_from_CFX_to_Polaris_EVO.cmd`).

## Batch Conversion of All Files at Once (Win)
Follow these steps to use the batch conversion scripts supplied with SoX for Windows. This will convert all the files at once. If you prefer to convert the files individually, or if the batch conversion script doesn't work for you, see [[#Manually Converting Files (Win)]] below.

1. Make sure you have completed all the steps under [[#Preparing for Conversion (Win)]] above.
2. Rename the `.wav` sound files to the [[#Sound File Names|input filenames]] listed above. You can use either the CFX or Proffie naming schemes; just be consistent.
3. Double-click on either `convert_from_CFX_to_Polaris_EVO.cmd` or `convert_from_ProffieOS_to_Polaris_EVO.cmd`, depending on how you have named your files.

A window will appear similar to the one below. After a few seconds, you should see a line saying "Press any key to continue..."
![Pasted image 20230517100910.png](Pasted%20image%2020230517100910.png)

> [!note]
> In my screenshot, you may see some lines that say "No such file or directory." That's because the sound font I was using had [[#^431156|fewer files]] than the script expected.

4. Press any key. The window will close.
5. In your SoX folder, you should now also see a bunch of files ending in `.RAW`. Congratulations! These are now ready to be uploaded to your saber!

![Pasted image 20230517101335.png](Pasted%20image%2020230517101335.png)

## Manually Converting Files (Win)
If the batch script above doesn't work for you, or if you want to convert additional files, you can use the steps below to manually convert each file.

> [!note]
> This isn't the only way to convert sound files, but it has the advantages of being free and easy to write instructions for. If you already have some experience processing and converting audio, feel free to use the tool of your choice! The details of the output format are [[#^d318ef|here]].

### Install SoX and Add to Your Path
You only need to follow these steps once to install and configure SoX for system-wide use.

> [!tip]
> Technically, installing SoX to your path is optional. However, I highly recommend it as it will make your life easier and save you some typing later on. If you prefer not to install SoX, you can use the version contained in the SoX_for_Polaris_EVO; you'll just have to invoke the full path to `sox.exe` every time you type a conversion command below (e.g., `.\sox\sox.exe file.wav ...`).

1. Download and install [SoX for Windows](https://sourceforge.net/projects/sox/files/latest/download). 
2. Open the Windows Command Prompt. Click on the search box and type `command`. Click on the "Command Prompt" icon. ^1da978

![Pasted image 20230504142928.png](Pasted%20image%2020230504142928.png)

3. In the Command Prompt window, type the following command and press **Enter**:

```cmd
setx path "%path%;C:\Program Files (x86)\sox-14-4-2"
```

> [!note]
> If you installed SoX to a location different from the default, replace `C:\Program Files (x86)\sox-14-4-2` with the folder where you installed it. If you just clicked through the installer and kept the defaults, you can ignore this.

You should see a message similar to the one below.

![Pasted image 20230517112158.png](Pasted%20image%2020230517112158.png)

4. Close the Command Prompt. This is important, because the changes to the Path variable won't be recognized until the next time you open a new Command Prompt.

To test that SoX is installed properly, you ccan do the following:

1. Open a new [[#^1da978|Command Prompt]].
2. Type `sox` and press **Enter**.

You should see a bunch of text appear in the Command Prompt similar to what's show below. This means SoX is ready to go!

![Pasted image 20230517112556.png](Pasted%20image%2020230517112556.png)

### Convert Files via Command Line
Once SoX is installed, converting from the command line is pretty straightforward.

1. Open a [[#^1da978|Command Prompt]] window.
2. In the Command Prompt window, use the `cd` command to change to the folder where your `.wav` files are located. 
	- For example, if you saved them to your Downloads folder, you should be able to type `cd Downloads` and press **Enter**.
	- If you're having trouble finding the folder, see [this article](https://www.howtogeek.com/659411/how-to-change-directories-in-command-prompt-on-windows-10/) for more help.
3. For each file you want to convert, type the following command and press **Enter**:

``` cmd
sox --clobber filename.wav -t raw -b 16 -c 1 -r 44100 OUTPUT.RAW
```

> [!info]
> Replace `filename.wav` with the name of the input file you want to convert, and `OUTPUT.RAW` with the output filename. See [[#Sound File Names|the filenames list]] for the expected output filenames. If you are converting extra sounds (e.g., additional clashes), continue the naming pattern listed there by increasing the numbers.

After a very short pause, you should get a new command prompt line, like this:

![Pasted image 20230517114910.png](Pasted%20image%2020230517114910.png)

> [!tip]- Deciphering the Magic Formula
> If you're interested, here's a little more info on what exactly the above command is doing. Feel free to skip it if you want.
> 
> ``` cmd
sox --clobber filename.wav -t raw -b 16 -c 1 -r 44100 OUTPUT.RAW
>```
>
>The first word on the line is the *command name*. This tells the computer which command to run (in this case, `sox`). You can think of it as being the name of magic spell you want to cast. The rest of the line is called *arguments*; these are extra pieces of information that tell the command exactly what you want to do--sort of like setting the target, duration, and other options of the magic spell.
>
>Here's what each of the specified arguments mean:
> - `--clobber` : Overwrite (replace) the output file if it already exists
> - `filename.wav` : The input filename; the file you want to convert *from*
> - `-t raw` : Make the output file a `.RAW` type
> - `-b 16` : Give the output a 16-bit [bit depth](https://www.headphonesty.com/2019/07/sample-rate-bit-depth-bit-rate/)
> - `-c 1` : Set the output to have only one channel (i.e., mono not stereo)
> - `-r 44100` : Use a 44.1kHz [sample rate](https://www.headphonesty.com/2019/07/sample-rate-bit-depth-bit-rate/)
> - `OUTPUT.RAW` : The filename you want the output to have; the file you want to convert *to*

You should now have a new `.RAW` file in the same folder as your `.wav` file, with the output filename you specified. Congratulations! Now repeat step 3 for each additional file you want to convert.

>[!note]
>Yes, it's a pain to have to type each input and output filename manually. That's why the batch scripts are provided. Really, all the batch scripts are doing is executing the above command for each file automatically. Doing it manually just gives you a little more control of the process, and can also help if you're having file name problems.

Now you're ready to upload the new `.RAW` files to your saber!

# macOS Conversion Instructions
If you're using a Mac, the process is mostly similar to the Windows one above. However, in some ways it's actually a little easier!

## Preparing for Conversion (Mac)
Before we begin, we need to get everything set up properly to make the conversion as smooth as possible. 

> [!note] Working with Files and Folders
> For the purposes of these instructions, I assume you already know the basics of [working with files and folders](https://edu.gcfglobal.org/en/osxbasics/working-with-files/1/) in macOS, including [how to extract zip files](https://support.apple.com/guide/mac-help/zip-and-unzip-files-and-folders-on-mac-mchlp2528/mac). If you need a refresher on these tasks, see the links.

### Install SoX

First, download and install [SoX](https://sox.sourceforge.net/). The easist way to do this is using [Homebrew for Mac](https://sox.sourceforge.net/):
1. Open the Terminal app from the App Launcher (it may be in a group called "Other" or "Utilities"), or from Spotlight Search.
2. In the Terminal window, copy and paste the following command and press **Enter**:
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
3. Wait for `brew` to finish installing. This may take a few minutes, but should be automatic.
4. Type or copy/paste the following command into Terminal and press **Enter**:
```sh
brew install sox
```

This will download and install SoX as well as other programs it needs to run. You should see something like the following:

![Pasted image 20230517124208.png](Pasted%20image%2020230517124208.png)

To test that it was installed, type `sox` in the Terminal and press **Enter**. You should see a bunch of text similar to the following:

![Pasted image 20230517124330.png](Pasted%20image%2020230517124330.png)

> [!note] Other Ways to Install
> If you prefer not to use Homebrew, you can also use the Mac installer from the SoX web page. However, you'll have to manually add it to your PATH to be able to use it in Terminal. You can also build it yourself from source. I'm going to omit instructions for these, but if you need help feel free to [[README#About|reach out]].

### Prepare Sound Files
Next, let's get the actual sound files set up!

1. Download your preferred [[Sound Fonts|sound font]] and extract the files to a convenient folder.
2. Locate the `.wav` sound files.

> [!note] 
> Depending on where you got your sound font, you may find that your download contains sub-folders with names like CFX, ProffieOS, Xenopixel, etc.  In each of these folders will be sets of `.wav` files, sometimes in further subfolders. These are files configured for [[Sound Fonts#Supported Saber Models (CFX, Proffie, Xeno, etc.)|various commercial lightsaber boards]]. Any one will do the job. If you're confused, I find CFX to usually be the easiest to work with, since it puts all the files in one folder.

3. Copy all the `.wav` [[#Sound File Names|files you want to convert]] to a new folder. This is optional, but will make organization easier.

## Batch Conversion of All Files at Once (Mac)
Follow these steps to use the batch conversion scripts. This will convert all the files at once. If you prefer to convert the files individually, or if the batch conversion script doesn't work for you, see [[#Manually Converting Files (Mac)]] below.

1. Make sure you have completed all the steps under [[#Preparing for Conversion (Mac)]] above.
2. Download the [macOS conversion scripts](https://github.com/jramboz/polaris-opencore/raw/master/Utilities/mac-linux_scripts.zip) and extract the `.zip` file.
3. Copy the extracted files to the folder containing your `.wav` files.
4. Rename the `.wav` sound files to the [[#Sound File Names|input filenames]] listed above. You can use either the CFX or Proffie naming schemes; just be consistent.
5. Right-click on either `convert_from_CFX_to_Polaris_EVO` or `convert_from_ProffieOS_to_Polaris_EVO` (depending on how you have named your files) and click "Open". A message will appear similar to the one below:

![Pasted image 20230517142229.png](Pasted%20image%2020230517142229.png)

6. Click "Open".

> [!note]
> You only need to do this the first time you run a script. On future uses, you can just double-click the file in Finder.

A window will appear similar to the one below. After a few seconds, you should see a line saying "Press any key to continue..."

![Pasted image 20230517142418.png](Pasted%20image%2020230517142418.png)

> [!note]
> In my screenshot, you may see some lines that say "No such file or directory." That's because the sound font I was using had [[#^431156|fewer files]] than the script expected.

4. Press any key. The window will close.
5. In your sound file folder, you should now also see a bunch of files ending in `.RAW`. Congratulations! These are now ready to be uploaded to your saber!

![Pasted image 20230517142529.png](Pasted%20image%2020230517142529.png)

## Manually Converting Files (Mac)
If the batch script above doesn't work for you, or if you want to convert additional files, you can use the steps below to manually convert each file.

> [!note]
> This isn't the only way to convert sound files, but it has the advantages of being free and easy to write instructions for. If you already have some experience processing and converting audio, feel free to use the tool of your choice! The details of the output format are [[#^d318ef|here]].

1. Open the Terminal app from the App Launcher (it may be in a group called "Other" or "Utilities"), or from Spotlight Search.
2. 2. In the Terminal window, use the `cd` command to change to the folder where your `.wav` files are located. 
	- For example, if you saved them to your Downloads folder, you should be able to type `cd Downloads` and press **Enter**.
	- If you're having trouble finding the folder, see [this article](https://appletoolbox.com/navigate-folders-using-the-mac-terminal/) for more help.
3. For each file you want to convert, type the following command and press **Enter**:

``` bash
sox --clobber filename.wav -t raw -b 16 -c 1 -r 44100 OUTPUT.RAW
```

> [!info]
> Replace `filename.wav` with the name of the input file you want to convert, and `OUTPUT.RAW` with the output filename. See [[#Sound File Names|the filenames list]] for the expected output filenames. If you are converting extra sounds (e.g., additional clashes), continue the naming pattern listed there by increasing the numbers.

After a very short pause, you should get a new command prompt line, like this:

![Pasted image 20230517143729.png](Pasted%20image%2020230517143729.png)

> [!tip]- Deciphering the Magic Formula
> If you're interested, here's a little more info on what exactly the above command is doing. Feel free to skip it if you want.
> 
> ``` cmd
sox --clobber filename.wav -t raw -b 16 -c 1 -r 44100 OUTPUT.RAW
>```
>
>The first word on the line is the *command name*. This tells the computer which command to run (in this case, `sox`). You can think of it as being the name of magic spell you want to cast. The rest of the line is called *arguments*; these are extra pieces of information that tell the command exactly what you want to do--sort of like setting the target, duration, and other options of the magic spell.
>
>Here's what each of the specified arguments mean:
> - `--clobber` : Overwrite (replace) the output file if it already exists
> - `filename.wav` : The input filename; the file you want to convert *from*
> - `-t raw` : Make the output file a `.RAW` type
> - `-b 16` : Give the output a 16-bit [bit depth](https://www.headphonesty.com/2019/07/sample-rate-bit-depth-bit-rate/)
> - `-c 1` : Set the output to have only one channel (i.e., mono not stereo)
> - `-r 44100` : Use a 44.1kHz [sample rate](https://www.headphonesty.com/2019/07/sample-rate-bit-depth-bit-rate/)
> - `OUTPUT.RAW` : The filename you want the output to have; the file you want to convert *to*

You should now have a new `.RAW` file in the same folder as your `.wav` file, with the output filename you specified. Congratulations! Now repeat step 3 for each additional file you want to convert.

>[!note]
>Yes, it's a pain to have to type each input and output filename manually. That's why the batch scripts are provided. Really, all the batch scripts are doing is executing the above command for each file automatically. Doing it manually just gives you a little more control of the process, and can also help if you're having file name problems.

Now you're ready to upload the new `.RAW` files to your saber!

# Linux Conversion Instructions
Look, I'm gonna level with you. If you're using Linux, you can probably figure out what I'm going to tell you all on your own, especially if you've skimmed the info above. But I'm not going to let my [penguin](https://en.wikipedia.org/wiki/Tux_(mascot))-loving friends be forgotten! So here's some instructions for you, too.

For the sake of expediency, I'm going to assume you already know how to get to a command line and how to use it to navigate the directory structure. Just in case you need a refresher, you can peek [here](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview).

## Preparing for Conversion (Linux)
Just a few quick steps to get you started!

1. Install [SoX](https://sox.sourceforge.net/), either by building from source or using your distro's package manager (e.g., `apt-get install sox` or `yum install sox`).
2. Download your preferred [[Sound Fonts|sound font]] and extract the files to a convenient directory.
3. Locate the `.wav` sound files.

> [!note] 
> Depending on where you got your sound font, you may find that your download contains sub-folders with names like CFX, ProffieOS, Xenopixel, etc.  In each of these folders will be sets of `.wav` files, sometimes in further subfolders. These are files configured for [[Sound Fonts#Supported Saber Models (CFX, Proffie, Xeno, etc.)|various commercial lightsaber boards]]. Any one will do the job. If you're confused, I find CFX to usually be the easiest to work with, since it puts all the files in one folder.

4. Copy all the `.wav` [[#Sound File Names|files you want to convert]] to a new folder. This is optional, but will make organization easier.

## Batch Conversion of All Files at Once (Linux)
Follow these steps to use the batch conversion scripts. This will convert all the files at once. If you prefer to convert the files individually, or if the batch conversion script doesn't work for you, see [[#Manually Converting Files (Linux)]] below.

1. Make sure you have completed all the steps under [[#Preparing for Conversion (Linux)]] above.
2. Download the [Linux conversion scripts](https://github.com/jramboz/polaris-opencore/raw/master/Utilities/mac-linux_scripts.zip) and extract the `.zip` file.
3. Copy the extracted files to the folder containing your `.wav` files.
4. Rename the `.wav` sound files to the [[#Sound File Names|input filenames]] listed above. You can use either the CFX or Proffie naming schemes; just be consistent.
5. Run either `./convert_from_CFX_to_Polaris_EVO` or `./convert_from_ProffieOS_to_Polaris_EVO`, depending on how you have named your files.
6. You should now have a bunch of `.RAW` files in the same directory. Congratulations! These are ready to upload to your saber!

## Manually Converting Files (Linux)
If the batch script above doesn't work for you, or if you want to convert additional files, you can use the steps below to manually convert each file.

> [!note]
> This isn't the only way to convert sound files, but it has the advantages of being free and easy to write instructions for. If you already have some experience processing and converting audio, feel free to use the tool of your choice! The details of the output format are [[#^d318ef|here]].

For each file you wish to convert, use this command:
``` bash
sox --clobber filename.wav -t raw -b 16 -c 1 -r 44100 OUTPUT.RAW
```

> [!info]
> Replace `filename.wav` with the name of the input file you want to convert, and `OUTPUT.RAW` with the output filename. See [[#Sound File Names|the filenames list]] for the expected output filenames. If you are converting extra sounds (e.g., additional clashes), continue the naming pattern listed there by increasing the numbers.

You should now have a new `.RAW` file in the same folder as your `.wav` file, with the output filename you specified. Congratulations! Now repeat the command for each additional file you want to convert.

>[!note]
>Yes, it's a pain to have to type each input and output filename manually. That's why the batch scripts are provided. Really, all the batch scripts are doing is executing the above command for each file automatically. Doing it manually just gives you a little more control of the process, and can also help if you're having file name problems.

Now you're ready to upload the new `.RAW` files to your saber!