# How to reuse windows key

1. Check if the key is reusable:
    - On original PC: `slmgr -dli`
        - Should show `RETAIL channel`
        - If it shows `OEM_DM`, that copy of windows is not reusable.
2. Find current windows key:
    - Type `regedit` in the windows search bar
    - Navigate to `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\SoftwareProtectionPlatform`
    - The key is labed `BackupProductKeyDefault`
4. Deactivate current key (Run both commands):
    - `slmgr.vbs /upk`
    - `slmgr.vbs /cpky`
5. On new computer: `slmgr.vbs /ipk YOUR_KEY_HERE`
