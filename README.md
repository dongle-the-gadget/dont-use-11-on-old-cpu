List of reasons why installing Windows 11 on an unsupported CPU is a bad idea:

1. Virtualization based security - main reason why your CPU is unsupported (thank your favorite CPU manufacturer for that, not Microsoft - I elaborate on this later), does not support MBEC (encryption part of VBS), without MBEC, it will have to simulate virtualization based security in the future when Windows 11 enables it by default for everyone and you will lose massive amounts of performance. VBS being enabled is not an issue on supported CPUs and comes with a minimal performance hit, if any. On unsupported CPUs... it will be bad.
2. There will be updates that will not be validated for old devices and they can completely brick your system on a regular basis - unsupported CPUs don't exist in Microsoft's eyes anymore. They may even cut updates completely. And no, not having updates is not "bliss" because you hate automatic updates. It is extremely bad.
3. There is a possibility for kernel checks against unsupported CPUs - this means that in the future you may not even be able to get past the BIOS post screen or boot into Windows at all.

Regarding VBS, or virtualization-based security - Microsoft has been pushing for this specific security feature for 10 whole years. Ever since Windows 8 in 2012. And Intel & AMD only introduced them beginning with Intel 8th gen and Ryzen 2nd gen.

Windows 11 exists only to push requirements in order introduce these much needed security features. 11 began development exactly when both Intel & AMD released 8th gen & 2nd gen Ryzen, which introduced support for VBS.

If they had introduced these features earlier, I guarantee you a bunch more CPUs would have been supported. But they didn't. And the minimum requirements is what you get.

They aren't cherry picked. They aren't randomly picked, or picked to make you buy a new device. They are the exact generations that first introduced support for virtualization based security, and only the manufacturers are to blame for not listening to Microsoft for a decade.

Just stay on Windows 10 - you are really not missing out on much, and you'll still have a perfectly fine, stable & supported OS for years to come. And who knows, maybe by 2025 you'll have enough for a shiny new device.

But I suppose it's easier to scream at Microsoft than seeing the bigger picture. 

--

Here is some more information about the requirements:

Direct picture to the relevant part - https://i.imgur.com/EUeLaCU.png

Whole article - https://blogs.windows.com/windows-insider/2021/06/28/update-on-windows-11-minimum-system-requirements/
