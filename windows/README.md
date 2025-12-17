# How to reuse windows key

1. Check if the key is reusable:
    - On original PC: `slmgr -dli`
        - `RETAIL channel` = reusable
        - `OEM_DM` = not reusable.
2. Find current windows key:
    - Type `regedit` in the windows search bar
    - Navigate to `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\SoftwareProtectionPlatform`
    - The key is labed `BackupProductKeyDefault`
    --------- OR -----------
    - Download and run `ShowKeyPlus`
3. Record the product key.
4. Deactivate current key (Run both commands):
    - `slmgr.vbs /upk`
    - `slmgr.vbs /cpky`
5. Activate windows on new PC: `slmgr.vbs /ipk YOUR_KEY_HERE`

How to Reuse a Windows Product Key

This guide explains how to check whether your Windows key is reusable and how to activate it on a new system.

1. Check if the Key Is Reusable

On the original PC:

Open Command Prompt (Admin)

Run:

slmgr /dli

Expected Results

RETAIL channel → ✅ Key is reusable

OEM_DM → ❌ Key is tied to the original motherboard and cannot be reused

2. Find the Current Windows Product Key
Option A: Using the Registry

Press Win + R, type regedit, and press Enter

Navigate to:

Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\SoftwareProtectionPlatform


Locate:

BackupProductKeyDefault

Option B: Using a Tool (Recommended)

Download and run ShowKeyPlus

Copy the displayed Product Key

3. Record the Product Key

Save the key in a secure location before continuing.

4. Deactivate the Key on the Original PC

Run both commands in Command Prompt (Admin):

slmgr.vbs /upk
slmgr.vbs /cpky


This removes the key from the old system.

5. Activate Windows on the New PC

On the new PC, open Command Prompt (Admin) and run:

slmgr.vbs /ipk YOUR_PRODUCT_KEY_HERE


Then activate Windows:

slmgr.vbs /ato
