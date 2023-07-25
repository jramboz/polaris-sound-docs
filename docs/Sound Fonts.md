---
share: true
---
# What is a Sound Font?
A sound font is simply a set of sounds for a lightsaber. Most of these are designed to emulate the sounds used in Star Wars, but some are completely different and unique. Part of the fun in customizing your saber is choosing the sounds that appeal to you!

# Types of Sound Font
When you start looking for custom lightsaber sound fonts, there's a lot of terminology and types that you'll run into. Below are some of the most common considerations when searching for and choosing a sound font.

## Standard vs. SmoothSwing
There are two major categories of sound fonts for lightsaber: **standard** and **smoothswing**. 

**Standard Sound Fonts** are the original type that's been around about as long as replica lightsabers. These consist of pre-recorded sounds that contain an entire swing motion from start to finish. When the saber senses a movement, it randomly selects one of the available swing sounds and plays it. *The entire sound is played, regardless of the actual motion of the saber*.

**SmoothSwing Sound Fonts** are a [newer development](http://therebelarmory.com/thread/9138/smoothswing-v2-algorithm-description) and represent a major improvement over the standard. In these sound fonts, swings are represented by a pair of sound files. The lightsaber software dynamically mixes these based on the saber's motion to create the pseudo-Doppler effect heard in films and other media. *This results in a sound that's synchronized to the actual motion of the saber in pitch and volume*.

> [!tip]- Hear it for yourself
> [This video](https://www.youtube.com/watch?v=9FdTDYCCp_4) gives a good comparison of SmoothSwing vs Standard Sound Fonts.
> <iframe width="560" height="315" src="https://www.youtube.com/embed/9FdTDYCCp_4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

The Polaris EVO supports SmoothSwing sound fonts as long as you have [[Updating the Firmware|firmware]] version 2.1.0 or later installed.

>[!note] SmoothSwing "Swing Accents"
>Some of the newest SmoothSwing sound fonts include "swing accents," which are additional files that play at the peak of a swing to give it a little extra emphasis. As of this writing, the Polaris OpenCore Firmware does not support these extra swing accents. This may change in the future!

## Supported Saber Models (CFX, Proffie, Xeno, etc.)
When looking at sound fonts created by the lightsaber community at large, you may see listings saying what models of lightsaber or sound board their files are formatted or packaged for. Some of the most common formats/boards are:

- CFX
- Proffie
- GHv3
- Xenopixel

In general, you don't have to worry about these for Polaris EVO. They refer to different ways of packaging the sound files so that the lightsaber software will recognize them. We will be converting from these to the format that the Polaris EVO uses, so you don't have to fret--any one will work.

## Free vs. Paid
Once you learn how to convert sound fonts for the Polaris, there are a lot of great choices out there! Some are available for [[#Free Sound Fonts|free]], while others are [[#Paid Sound Fonts|sold]] for a small fee by their creators. Whether free or paid, almost all sound fonts will have a demo video so you can hear what they sound like before you download.

[[#Making Your Own|Creating a sound font]] that sounds professional is hard work, so don't be afraid to pay if you can. I think the quality you get is worth it. However, if you find a free sound font that you like, that's great too! Some people just enjoy making and sharing things, and whether or not they charge for it isn't necessarily any indication of quality. Feel free to experiment and find the sound that fits you.

# Where to Find Sound Fonts
This is definitely not a comprehensive list! Google will find you tons of great sound fonts and sound font makers. Here are just a few to get you started.

## Free Sound Fonts

- [This post](https://therebelarmory.com/post/106691) has four free SmoothSwing fonts:
	- SmoothGrey
	- SmoothJedi
	- RogueCommander
	- SmoothFuzz
	- DarkKyber
- [Tythonian Crystal](https://www.dropbox.com/s/t0nmhlev4u5pwdl/Tythonian_Crystal.zip?dl=0) (SmoothSwing)
- [Original Polaris Sound Font](https://github.com/LamaDiLuce/polaris-opencore/raw/master/OEM%20Raw%20sound%20files.zip)
- [Polaris SmoothSwing Sound Font](https://github.com/LamaDiLuce/polaris-opencore/raw/master/Utilities/AnimaEVO_SmoothSwing.zip)

## Paid Sound Fonts
There are many, many excellent sound font designers out there. Here are a couple of the ones I've personally purchased from and enjoyed:

- [KSith Saber Fonts](https://www.ksithsaberfonts.com/)
- [BK Saber Sounds](https://www.bksabersounds.com/)

## Making Your Own
If you're interested in making your own sound font, [this thread](http://therebelarmory.com/thread/9176/smoothswing-font-creators-discussion-thread) has tons of info and is a great place to start.

Next: [[Sound Fonts on Polaris]]