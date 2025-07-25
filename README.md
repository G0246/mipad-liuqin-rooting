# Liuqin Rooting
**No files are required for the tutorial below from this repository; this is only used to store my configurations and other customizations.**

# Unlocking the bootloader
> [!WARNING]
> The steps provided below are relatively straightforward, however if you're still not sure how to proceed, I advise you to use your device normally and avoid unlocking the bootloader.
>
> A computer is needed for rooting or bootloader unlocking; please get one ready.
---
## HyperOS bypass / MIUI method
> [!NOTE]
> Unlock bootloader will factory reset and clear all your data, backup before you do so.

1. If you are on HyperOS, then you need an extra step and follow the instructions to bypass the bootloader using another [tool](https://github.com/MlgmXyysd/Xiaomi-HyperOS-BootLoader-Bypass?tab=readme-ov-file#%EF%B8%8F-how-to-use). (Skip this step if you are on MIUI.)
2. Assuming you have followed the instructions above correctly and binded your Xiaomi account to your device, you can then use the official [Mi Unlock tool](https://en.miui.com/unlock/index.html) to check remaining time.
3. Reboot your device to bootloader and connect it to your computer. **(Make sure you have the necessary drivers!)**
4. Open the Mi Unlock tool and log in with your Xiaomi account, follow the on-screen instructions to unlock the bootloader.
---
## Upgrading / Downgrading system version
> [!TIP]
> I don't like using the official MiFlash tool because the default settings will lock your bootloader and just waste you more time. To minimize human error, you can avoid using it by following the steps below.

1. Download the official fastboot ROM you want to use from [xiaomirom](https://xiaomirom.com/en/) or other simillar firmware websites.
2. Extract it twice until you see the contents.
3. Download [SDK Platform Tools](https://developer.android.com/tools/releases/platform-tools) from Google and extract the contents.
4. Put the SDK platform tools file into the firmware folder you just extracted.
5. Reboot your device to bootloader and connect it to your computer. **(Make sure you have the necessary drivers!)**
6. Run `flash_all.bat` that comes with it from Command Prompt and wait patiently for it to finish.
7. The device should automatically reboot to the new system.

## Rooting the device
> [!IMPORTANT]
> **PLEASE** make sure the firmware you downloaded is correct for your device model, making this mistake can brick it!

1. Download the official fastboot ROM you want to use from [xiaomirom](https://xiaomirom.com/en/) or other simillar firmware websites.
2. Extract it twice until you see the contents.
3. Copy `boot.img` and move it to your device.
4. Download [Magisk](https://github.com/topjohnwu/Magisk/releases) and patch the image, it should look like `magisk_patched-00000_XXXXX.img`.
5. Move it back to your computer.
5. Reboot your device to bootloader.
6. Patch the image using the command `fastboot flash boot magisk_patched-00000_XXXXX.img`, this will flash the patched boot image into boot sector.
7. Reboot.
8. Now your device is rooted!

## Disclaimer
**By following this tutorial, I am not responsible for any damages caused to your device or data. Please have basic common sense and do more research if you are unsure about something.**
