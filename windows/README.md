# How to reuse windows key

### 1. Check if the key is reusable
- On original PC: `slmgr -dli`
  - `RETAIL channel` - reusable
  - `OEM_DM` - not reusable.
  - 
### 2. Find current windows key:
- I recommend doing both *just in case*.
  
### Option A:
- Type `regedit` in the windows search bar
- Navigate to `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\SoftwareProtectionPlatform`
- The key is labed `BackupProductKeyDefault`
### Option B:
- Download and run `ShowKeyPlus`
 
### 3. Record the product key.

### 4. Deactivate current key (Run both commands):
- `slmgr.vbs /upk`
- `slmgr.vbs /cpky`

### 5. Activate windows on new PC: 
- `slmgr.vbs /ipk YOUR_KEY_HERE`
