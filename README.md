![Isagi Celebrating](isagi.png)

# Realme C21Y (RMX3261 / RMX3263) Kernel – **RED8D1**

Custom kernel source for the **Realme C21Y**, built from the official **RED8D1** tree.  

---

### Important  
This is **not** the Kaiju Kernel Source.  
For the newer source with kernelsu-next visit:  
[**RealmeC21Y-kernelSU-Next**](https://github.com/fanu96/RealmeC21Y-kernelSU-Next.git)

---

## Overview of Changes  

### Build & Stability  
- Removed YAML dependency from DTC (prevents `libyaml` compilation errors).  
- Fixed the boot warning:  
  *"There is an internal problem with your device. Please contact your manufacturer."*  
- Applied several minor stability and compatibility improvements (some undocumented).  

---

### SELinux  
- Default mode: **Permissive**.  
- If enforcing mode is preferred:  
  - Replace `hooks.c` and `selinuxfs.c` with versions from the stock Realme source.

---

### Module and Config Adjustments  
- Kernel module signature verification disabled.  
- `CONFIG_MODVERSIONS` disabled (allows easy loading of custom modules).  
- Stock defconfig provided as `config/stock_defconfig`.  
  - For reference only — not directly compatible.  
  - Use `realme3263_defconfig` for actual kernel builds.  

---

## Compiler Requirements  
- **Clang:** use `clang-r383902b`.  
- **GCC:**  
  - Android GCC 4.9 supported.  
  - ARM GNU Toolchain 14.3 or older is recommended.  

---

## Stay Updated  
For **Kaiju Kernel** announcements and releases:  
[**Join the Telegram Channel**](https://t.me/kernelkaiju)
