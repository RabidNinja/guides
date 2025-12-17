# How to reuse windows key

### 1. Check if the key is reusable
- On original PC: `slmgr -dli`
  - `RETAIL channel` - reusable
  - `OEM_DM` - not reusable.
### 2. Find current windows key:
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


---

## 2. Retrieve the Windows Product Key

### Option A: Registry Method

1. Press Win + R, type regedit, and press Enter
2. Navigate to:
   Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\SoftwareProtectionPlatform
3. Copy the value named:
   BackupProductKeyDefault

### Option B: ShowKeyPlus (Recommended)

1. Download and run ShowKeyPlus
2. Copy the displayed product key

---

## 3. Save the Product Key

Store the product key in a secure location before continuing.

---

## 4. Remove the Product Key From the Original System

On the original PC, open Command Prompt (Admin) and run:

slmgr.vbs /upk
slmgr.vbs /cpky

---

## 5. Activate Windows on the New System

On the new PC, open Command Prompt (Admin) and run:

slmgr.vbs /ipk YOUR-PRODUCT-KEY-HERE
slmgr.vbs /ato

---

## Troubleshooting

- Ensure the Windows edition matches the original system
- Use Settings → System → Activation → Troubleshoot if activation fails
- Contact Microsoft Support for retail licenses

---

## Disclaimer

This guide is provided for educational purposes. License transfer eligibility is subject to Microsoft’s licensing terms.
