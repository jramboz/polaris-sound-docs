---
share: true
---

# Welcome!
Welcome to the wonderful world of customizing your Polaris EVO! While this may seem intimidating at first, it's actually fairly straightfoward once you understand some of the basic concepts. Hopefully these documents will help demystify the process and make it more accessible to all the wonderful members of the [LudoSport](http://ludosport.net) family.

## Updated documentation
For the latest version of this documentation, please see the link in the [About](Introduction.md#About) section of the [Introduction](Introduction.md) file.

## Contributing to this documentation
If you'd like to contribute to this documentation, please [Contact the Author](README.md#About) or submit a pull request to the Github repository.

# What You'll Need
Before we begin, there are a few things you'll need to gather.

## Hardware
Physical components you'll need:

- A Polaris EVO saber
- A PC running Windows, macOS, or Linux
- A micro-USB cable capable of passing data

> [!tip] Note on USB Cables
> The EVO Anima seems to be very picky about USB cables. I recommend a cable with a very thin connector on the end that connects to the Anima. This allows the cable to fully seat very close to the saber, flush with the body.

> [!info]- For Older Polaris Models
> These instructions are written for newer Polaris sabers using the Anima EVO electronics core. Older models of Anima will need to use the [legacy software and instructions](https://www.lamadiluce.it/polaris-software-and-manual-2/).

## Software
You will need:

- [Gilthoniel Saber Manager](http://sabers.amazer.uk/?p=gilthoniel)
- [Sound eXchange (SoX)](https://sox.sourceforge.net/) - Windows users download [here](https://github.com/LamaDiLuce/polaris-opencore/raw/master/Utilities/SoX_for_Polaris_EVO.zip)
- A lightsaber [sound font](Sound%20Fonts.md)
- One of the following:
	- Command-line `py2saber` (recommended) - [GitHub](https://github.com/jramboz/py2saber/releases/latest)
	- Command-line `sendtosaber` - [Win32](https://github.com/LamaDiLuce/polaris-opencore/raw/master/Utilities/sendtosaber_x32.exe), [Win64](https://github.com/LamaDiLuce/polaris-opencore/raw/master/Utilities/sendtosaber_x64.exe), [Mac](https://github.com/LamaDiLuce/polaris-opencore/raw/master/Utilities/sendtosaber)
- (Optional, for updating firmware) `tycmd` - [Mac](https://github.com/LamaDiLuce/polaris-opencore/raw/master/Utilities/flash-opencore-builder/files/tycmd), [Windows](https://github.com/LamaDiLuce/polaris-opencore/raw/master/Utilities/flash-opencore-builder/files/tycmd.exe), [Linux](https://github.com/Koromix/tytools#build-on-linux)

# Troubleshooting and Getting Help
If you run into any problems with these instructions, or anything doesn't work as planned, first try the following:

* Turn the saber switch off and on again.
* Disconnect and reconnect the saber from your PC.
* Try a different USB cable.

If you're still having problems, here are some ways you can reach out for help!

* Contact [Jason "Hawkeye" Ramboz](https://github.com/jramboz) (that's me!)
* Ask in the `#help-sabersmith` channel on the WeAreLudoSport Discord Server.
* If you suspect your Anima is damaged, not functioning properly, or otherwise has a hardware problem, contact [Lama di Luce](https://www.lamadiluce.it/).