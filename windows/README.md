# How to reuse windows key

1. Check if the key is reusable:
    - On original PC: `slmgr -dli`
        - Should show `RETAIL channel`
        - If it shows `OEM_DM`, that copy of windows is not reusable.
3. Deactivate current key: `slmgr.vbs /upk`
4. Clear the product key from the Windows Registry: `slmgr.vbs /cpky`
    - This protects it from being accessed by key finder programs or malicious tools.
5. On new computer: `slmgr.vbs /ipk YOUR_KEY_HERE`
