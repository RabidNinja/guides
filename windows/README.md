# How to reuse windows key

1. Check if the key is reusable:
    1. On original PC, open command prompt
    2. `slmgr -dli`
        - should show `RETAIL channel`
        - If it shows `OEM_DM`, that copy of windows is not reusable.
3. Deactivate current key: `slmgr.vbs /upk`
4. Idk what this does but it was part of the guide: `slmgr.vbs /cpky`
    - apparently, it "clears the product key from the Windows Registry to protect it from being accessed by key finder programs or malicious tools"
5. On new computer: `slmgr.vbs /ipk YOUR_KEY_HERE`
