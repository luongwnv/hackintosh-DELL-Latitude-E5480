# Adjust DVMT
For enabling 4K60p and better graphics performance

* **Step 1:** Boot up OpenCore and choose `modGRUBShell.efi`.
* **Step 2:** Type `setup_var 0x795 0x2` to set DVMT Pre-allocated to `64M`
* **Step 3:** Type `setup_var 0x796 0x3` to set DVMT Total GFX MEM to `Max`
* **Step 4:** Remove `framebuffer-fbmem` and `framebuffer-stolenmem` in your `config.plist`

**You've done! And please do not reset the BIOS or you will have to do the process again!**
