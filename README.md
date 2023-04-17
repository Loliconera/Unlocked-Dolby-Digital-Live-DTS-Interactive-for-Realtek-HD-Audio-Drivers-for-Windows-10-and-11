### Guide to enable Dolby Digital Live and/or DTS Interactive:

1. Uninstall your existing Realtek drivers with [Display Driver Uninstaller (DDU)](https://www.guru3d.com/files-details/display-driver-uninstaller-download.html) and reboot.<br>
<img src="https://i.imgur.com/5jiAmUS.png" alt="drawing" width="600"/>

2. You will have to **disable the use of signed drivers** ([How To Disable Driver Signature Enforcement](https://www.youtube.com/watch?v=C9M2l5vp5co), [How to disable mandatory use of signed drivers](https://answers.microsoft.com/es-es/windows/forum/all/windows-10-c%C3%B3mo-deshabilito-el-uso/778da35d-deab-4a99-84fb-02a274bf5fc5))<br>
<img src="https://i.imgur.com/RKjWZOh.png" alt="drawing" width="600"/>

3. **[Option 1]** Download the **0006-Win7_Win8_Win81_Win10_R280.exe** installer and extract the installer content to a folder [Realtek HD audio drivers R2.80](https://www.techspot.com/drivers/driver/file/information/18007/) (Version is recommended **R2.80**).<br>
<img src="https://i.imgur.com/uuQeN5Q.png" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/232379499-b0720780-912d-49c0-a0f8-689ba83cdf7f.jpg" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/232379607-77662cf7-6357-4b37-be40-54852424561d.png" alt="drawing" width="600"/>

4. **[Option 2]** Download the zip file the **0007-Win7_Win8_Win81_Win10_R280.zip** [Realtek HD audio drivers R2.80](https://drivers.softpedia.com/get/SOUND-CARD/REALTEK/Realtek-High-Definition-Audio-Driver-280.shtml#download) and unzip the contents in a folder.
<img src="https://user-images.githubusercontent.com/69399372/232378035-031b56a4-4c6f-456e-a0ad-86208446c1d3.jpg" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/232380221-192710ba-1529-4656-99f0-0ae496f607af.jpg" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/232380956-501e7c18-cbd3-4917-9d62-907f52904ddc.png" alt="drawing" width="600"/>

5. Use [Pihto's patch](https://www.techpowerup.com/forums/attachments/realtek-hd-sound-driver-patch-zip.99391/) to patch the DLL files (the password is **''realtek''**). The target filenames are listed on the patcher window. They begin with **"rltkAPO64.dll, rltkAPO.dll"** and may be in "win32" and "win64" subfolders of the Realtek package. You will have to manually select each file to patch and run the patcher multiple times to patch all matching files.<br>

**Nota**: Antivirus may detect patcher.exe as a virus, so you may need to exclude patcher.exe from Antivirus.

<img src="https://i.imgur.com/0lfPjpt.png" alt="drawing" width="600"/>

- For **32 bit** versions:  

<img src="https://user-images.githubusercontent.com/69399372/232382338-c5d7cddd-7fde-4570-a2d8-2beba311ccf2.jpg" alt="drawing" width="600"/>

- For **64 bit** versions:  

<img src="https://user-images.githubusercontent.com/69399372/232381864-f7d076da-dc2e-4a01-9398-238cfc5186c8.jpg" alt="drawing" width="600"/>

6. Now run the Realtek setup program. You may be asked to install **unsigned drivers**. Choose **yes**.<br>
<img src="https://i.imgur.com/3LRw8ft.png" alt="drawing" width="600"/>

7. Do not immediately reboot. Instead, open regedit and ensure the **"DisableProtectedAudioDG"** registry fix is still present. If not, add it again. You need to create it for that, **select right click on the blank => New => DWORD (32 bit) value** and then name it **''DisableProtectedAudioDG''** with hex value **''1''**<br>

```
REGEDIT4
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Audio]
"DisableProtectedAudioDG"=dword:00000001
```
<img src="https://user-images.githubusercontent.com/69399372/154792482-039e2ef6-0ac5-449b-8ad7-6ff22f859c68.png" alt="drawing" width="600"/>

8. Reboot, and **Dolby Digital Live/DTS Interactive** should be available.<br>
<img src="https://user-images.githubusercontent.com/69399372/154792554-4750fdfe-b843-44a4-acc3-062a1530f11d.png" alt="drawing" width="600"/>

9. Working properly on **Windows 10/11** with Realtek version **R2.80**<br>
<img src="https://user-images.githubusercontent.com/69399372/232382710-438a8e06-c7c5-4c47-b145-b755a77d3cf6.png" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/154156378-87bf1406-8242-451b-8f20-5415edff27c7.png" alt="drawing" width="600"/>

This guide only works for the **S/PDIF** interface and will unlock **Dolby Digital Live** and **DTS Connect**<br>
<img src="https://user-images.githubusercontent.com/69399372/232383054-d3468541-f993-4642-8e62-e0a5ebec3d34.png" alt="drawing" width="600"/>

<img src="https://user-images.githubusercontent.com/69399372/154158010-72110b9d-54ad-41b7-9587-832424688e8b.png" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/154156422-c7e02fb7-72cd-4e69-941b-42233a3abf4f.png" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/154156457-30987569-a326-4e82-9928-8291708ba45a.png" alt="drawing" width="600"/>
<img src="https://i.imgur.com/CfO9OrD.png" alt="drawing" width="600"/>
<img src="https://i.imgur.com/ZepREz2.png" alt="drawing" width="600"/>
<img src="https://i.imgur.com/XUVR1nH.png" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/154156477-bdae5787-24ef-4ed8-8021-a7baa31c128a.png" alt="drawing" width="600"/>
<img src="https://i.imgur.com/f8yQ6vh.png" alt="drawing" width="600"/>
<img src="https://i.imgur.com/Qop9WrU.png" alt="drawing" width="600"/>
<img src="https://i.imgur.com/uoWt0OQ.png" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/154792537-2711ace8-fe95-4ffc-a27a-e88ac5f03a3b.png" alt="drawing" width="600"/>
<img src="https://i.imgur.com/ZhzpphO.png" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/154156529-f24494ca-c8ef-4ed7-97b5-e63861921f15.png" alt="drawing" width="600"/>
