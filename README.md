**TL;DR** - Installing Windows 11 on an unsupported CPU will have bad consequences in the future, including but not limited to: significantly degraded performance, no validation of updates for your device (or possibly no updates at all), and the very likely possibility of kernel checks against your CPU resulting in an unbootable machine. I recommend you stick with Windows 10 until 2025 or until you're able to get a new device, it is still a perfectly fine, stable & up to date OS. If you want me to validate these claims, then keep reading.

Yes, this is a wall of text, but I urge you to read all of this in order to gain a proper understanding of the situation.

## Reasons why installing Windows 11 on an unsupported CPU is a bad idea
### Virtualization-based security
Main reason why your CPU is unsupported (thank your favorite CPU manufacturer for that, not Microsoft - I elaborate on this later). Unsupported CPUs do not support MBEC. Without MBEC, the processor will have to simulate virtualization-based security in the future when Windows 11 enables it by default for everyone and you will lose massive amounts of performance[^1]. VBS being enabled is not an issue on supported CPUs and comes with a minimal performance hit, if any. On unsupported CPUs... it will be **bad**. 

By locking out CPUs who do not support VBS & MBEC from installing Windows 11, they are actively trying to avoid a Windows Vista situation where the performance was worse than desired.

A note about the 7th generation of Intel Core CPUs, codenamed "Kaby Lake" - its CPUs **do** support VBS and MBEC. However, they are still **not** on Microsoft's supported CPU list, and the generation has reached its end of life, and as such manufacturer support for these CPUs is completely halted. See [Reliability and support](#reliability-and-support) below for more information.

### Low quality updates, or the complete lack of updates
At the time of writing, unsupported machines **do** get updates. However, there is a 99.9% chance this will change in the future. There will be updates that will not be validated for old devices and they can completely brick your system on a regular basis - unsupported CPUs don't exist in Microsoft's eyes anymore. **They may even cut updates completely**[^2]. And no, not having updates is not "bliss" because you hate automatic updates. It is **extremely bad**.

### Kernel checks
There is a possibility for kernel checks against unsupported CPUs - this means that in the future you may not even be able to get past the BIOS post screen or boot into Windows at all. You are able to bypass all the hardware requirements, but you will not be able to bypass kernel checks unless you somehow gain access to the kernel and make your own modified builds, or you remain on an older build forever which... would not make sense, especially for the security of your device.

### Reliability and support
The CPU generations that are not in Microsoft's list of supported CPUs have their support halted from their manufacturers, which means that there would be a higher chance of crashing and outdated drivers. In fact, Intel's 8th generation of their Core CPUs, codenamed "Coffee Lake", is, at the time of writing, reaching its end of life. Some 8th Gen CPUs have already been discontinued. For example, the i7-8565U, a supported mobile CPU, has reached its shipment discontinuation on the date of November 19th, 2021.[^3]

## Explaining the requirements
### What's the big deal about VBS?
Regarding VBS, or virtualization-based security - Microsoft has been pushing for this specific security feature for 10 whole years. Ever since Windows 8 in 2012. And Intel & AMD only introduced them beginning with Intel 8th gen and Ryzen 2nd gen.

Windows 11 exists only to push requirements in order to introduce these much needed security features. Windows 11 began development exactly when both Intel & AMD released 8th gen & 2nd gen Ryzen, which introduced support for VBS. Microsoft finally had a way to introduce these features to the mainstream, and decided to create Windows 11 which only supports CPUs that have hardware support for VBS. This is why they abandoned the "Windows as a service" system with Windows 10, and instead started focusing on a more security oriented version of Windows. Because they finally could.[^4]

If AMD & Intel had introduced these features earlier, I guarantee you a bunch more CPUs would have been supported. I guarantee you that list of CPUs would have been much larger. I guarantee you Windows 11 would have not even existed and instead the first ever Windows 10 version would have gotten VBS, Secure Boot & TPM 2.0, because the CPUs would have supported that. If only AMD & Intel had listened. But they didn't. And the minimum requirements we have now, is what you get. They will not change - unless those unsupported CPUs somehow magically gain hardware support for features like VBS. Which, obviously, they won't.

### Can't I just turn VBS off when they enable it by default?
Absolutely. I've just explained why your CPU is unsupported in that whole spiel. But VBS isn't the only thing you should worry about. The other factors I've spoken about are still a source of concern.

### The requirements are made to push me towards buying a new device!
No, they're not. The requirements aren't cherry picked, or randomly picked by Microsoft. The minimum CPU requirements are the exact generations that first introduced support for virtualization-based security. It is not a coincidence that those generations are the minimum, it is intended. And you know who to blame for the requirements already. If not, please re-read the third paragraph in the "What's the big deal about VBS?" section.

### If we shouldn't upgrade on unsupported hardware, how come Microsoft has an article to bypass the requirements?
I guarantee you that article will magically disappear in the future, along with any mention of upgrading to Windows 11 on unsupported hardware. This will happen at around the same time when updates are either restricted or cut off, or kernel checks are implemented. They **did** mention that you follow that article **at your own risk**, so they do not care if you proceeded to follow it and that you are now struck by their restrictions.

### What should I do?
Well, if it wasn't obvious enough, just stay on Windows 10 - you are really not missing out on much, and you'll still have a perfectly fine, stable & supported OS for years to come. And who knows, maybe by 2025 (the year Windows 10 reaches the end of its life) you'll have enough for a shiny new device. And when that time comes, you'll finally be able to have Windows 11, which will be more stable, and all of the security goodies it comes with, such as VBS, TPM 2.0, Secure Boot... who knows, maybe even the Pluton chip[^5] will be mainstream by then...

But... I suppose it's easier to scream at Microsoft than seeing and accepting the bigger picture.

[^1]: [Microsoft: "Because it makes use of Mode Based Execution Control, HVCI works better with Intel Kaby Lake or AMD Zen 2 CPUs and newer. Processors without MBEC will rely on an emulation of this feature, called Restricted User Mode, which has a bigger impact on performance."](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-guard/enable-virtualization-based-protection-of-code-integrity)
[^2]: [Microsoft: "Your device might malfunction due to these compatibility or other issues. Devices that do not meet these system requirements will no longer be guaranteed to receive updates, including but not limited to security updates."](https://support.microsoft.com/en-us/windows/installing-windows-11-on-devices-that-don-t-meet-minimum-system-requirements-0b2dc4a2-5933-4ad4-9c09-ef0a331518f1)
[^3]: [Intel on the discontinuation of the Core i3-8140U CPU](https://qdms.intel.com/dm/i.aspx/ECC49A54-9E4A-4930-AE08-572B4414D498/PCN118065-00.pdf)
[^4]: [Microsoft article on the requirements (see "Why new Windows 11 minimum system requirements" section)](https://blogs.windows.com/windows-insider/2021/06/28/update-on-windows-11-minimum-system-requirements/)
[^5]: [Pluton chip](https://www.microsoft.com/security/blog/2020/11/17/meet-the-microsoft-pluton-processor-the-security-chip-designed-for-the-future-of-windows-pcs/)
