Yes, this is a wall of text, but I urge you to read all of this in order to gain a proper understanding of the situation.

<h2>Reasons why installing Windows 11 on an unsupported CPU is a bad idea</h2>

<h3>Virtualization-based security</h3>

Main reason why your CPU is unsupported (thank your favorite CPU manufacturer for that, not Microsoft - I elaborate on this later). Unsupported CPUs do not support MBEC. Without MBEC, the processor will have to simulate virtualization-based security in the future when Windows 11 enables it by default for everyone and you will lose **massive** amounts of performance[^3]. VBS being enabled is not an issue on supported CPUs and comes with a minimal performance hit, if any. On unsupported CPUs... it will be **bad**.

<h3>Low quality updates, or the complete lack of updates</h3>

At the time of writing, unsupported machines **do** get updates. However, there is a 99.9% chance this will change in the future. There will be updates that will not be validated for old devices and they can completely brick your system on a regular basis - unsupported CPUs don't exist in Microsoft's eyes anymore. **They may even cut updates completely**[^4]. And no, not having updates is not "bliss" because you hate automatic updates. It is **extremely** bad.

<h3>Kernel checks</h3>

There is a possibility for kernel checks against unsupported CPUs - this means that in the future you may not even be able to get past the BIOS post screen or boot into Windows at all. You are able to bypass all the hardware requirements, but you will not be able to bypass kernel checks unless you somehow gain access to the kernel and make your own modified builds, or you remain on an older build forever which... would not make sense, especially for the security of your device.

<h3>What's the big deal about VBS?</h3>

Regarding VBS, or virtualization-based security - Microsoft has been pushing for this specific security feature for 10 whole years. Ever since Windows 8 in 2012. And Intel & AMD only introduced them beginning with Intel 8th gen and Ryzen 2nd gen.

Windows 11 exists only to push requirements in order to introduce these **much** needed security features. Windows 11 began development exactly when both Intel & AMD released 8th gen & 2nd gen Ryzen, which introduced support for VBS. Microsoft finally had a way to introduce these features to the mainstream, and decided to create Windows 11 which only supports CPUs that have hardware support for VBS. This is why they abandoned the "Windows as a service" system with Windows 10, and instead started focusing on a more security oriented version of Windows. Because they finally could.[^1]

If AMD & Intel had introduced these features earlier, I guarantee you a bunch more CPUs would have been supported. I guarantee you that list of CPUs would have been **much** larger. I guarantee you **Windows 11 would have not even existed** and instead the first ever Windows 10 version would have gotten VBS, Secure Boot & TPM 2.0, because the CPUs would have supported that. If only AMD & Intel had listened. But they didn't. And the minimum requirements we have now, is what you get. They will not change - unless those unsupported CPUs somehow magically gain hardware support for features like VBS. Which, obviously, they won't.

<h3>Can't I just turn VBS off when they enable it by default?</h3>

Absolutely. I've just explained why your CPU is unsupported in that whole spiel. But VBS isn't the only thing you should worry about. The other factors I've spoken about are still a source of concern.

<h3>The requirements are made to push me towards buying a new device!</h3>

No, they're not. The requirements aren't cherry picked, or randomly picked by Microsoft. The minimum CPU requirements are the exact generations that first introduced support for virtualization-based security. It is not a coincidence that those generations are the minimum, it is intended. And you know who to blame for the requirements already. If not, please re-read the third paragraph in the "What's the big deal about VBS?" section.

<h3>If we shouldn't upgrade on unsupported hardware, how come Microsoft has an article to bypass the requirements?</h3>

I guarantee you that article will magically disappear in the future, along with any mention of upgrading to Windows 11 on unsupported hardware. This will happen at around the same time when updates are either restricted or cut off, or kernel checks are implemented. They **did** mention that you follow that article **at your own risk**, so they do not care if you proceeded to follow it and that you are now struck by their restrictions.

<h3>What should I do?</h3>

Well, if it wasn't obvious enough, **just stay on Windows 10** - you are really not missing out on much, and you'll still have a perfectly fine, stable & supported OS for years to come. And who knows, maybe by 2025 (the year Windows 10 reaches the end of its life) you'll have enough for a shiny new device. And when that time comes, you'll finally be able to have 11, which will be more stable, and all of the security goodies it comes with, such as VBS, TPM 2.0, Secure Boot... who knows, maybe even the Pluton chip[^2] will be mainstream by then...

But... I suppose it's easier to scream at Microsoft than seeing and accepting the bigger picture. 

[^1]: [Microsoft article on the requirements (see "Why new Windows 11 minimum system requirements" section)](https://blogs.windows.com/windows-insider/2021/06/28/update-on-windows-11-minimum-system-requirements/)
[^2]: [Pluton chip](https://www.microsoft.com/security/blog/2020/11/17/meet-the-microsoft-pluton-processor-the-security-chip-designed-for-the-future-of-windows-pcs/)
[^3]: [Microsoft: "Because it makes use of Mode Based Execution Control, HVCI works better with Intel Kaby Lake or AMD Zen 2 CPUs and newer. Processors without MBEC will rely on an emulation of this feature, called Restricted User Mode, which has a bigger impact on performance."](https://docs.microsoft.com/en-us/windows/security/threat-protection/device-guard/enable-virtualization-based-protection-of-code-integrity)
[^4]: [Microsoft: "Your device might malfunction due to these compatibility or other issues. Devices that do not meet these system requirements will no longer be guaranteed to receive updates, including but not limited to security updates."](https://support.microsoft.com/en-us/windows/installing-windows-11-on-devices-that-don-t-meet-minimum-system-requirements-0b2dc4a2-5933-4ad4-9c09-ef0a331518f1)
