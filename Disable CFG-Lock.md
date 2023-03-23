# Disable CFG Lock

You will need:
* `ControlMsr32.efi` (or `VerifyMsr32.efi`) - bundled with [**OpenCorePkg**](https://github.com/acidanthera/OpenCorePkg) in your `/EFI/OC/Tools`
* `modGRUBShell.efi` - download [**here**](https://github.com/datasone/grub-mod-setup_var)

## Check if CFG Lock enabled or not
Boot up OpenCore and choose `ControlMsr32.efi`. It should show:
`This firmware has UNLOCKED MSR 0xE2 register!` - means CFG Lock is disable
`This firmware has LOCKED MSR 0xE2 register!` - means CFG Lock is enabled

If CFG Lock is disable, go into your `config.plist` and set both `AppleCpuPmCfgLock` and `AppleXcpmCfgLock` to `FALSE` then you done.

If not, please continue.

## Disabling CFG Lock
Boot up OpenCore and choose `modGRUBShell.efi`.

Next, type `setup_var 0x4ED 0x00`.

After doing the commands, **please shutdown your PC and turn it on again**. After that, boot OpenCore and select `ControlMsr32.efi` to see if your CFG Lock is disabled or not.

If it shows `This firmware has UNLOCKED MSR 0xE2 register!` , you successfully unlocked your CFG Lock! **Also please don't reset your BIOS, or your CFG Lock will be enabled again after doing so**.

Finally, open `config.plist` and set both `AppleCpuPmCfgLock` and `AppleXcpmCfgLock` to `FALSE`, then boot macOS as normal. You should have better CPU Power Management.
