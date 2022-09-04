### Guide to enable Dolby Digital Live and/or DTS Interactive:

1. Uninstall your existing Realtek drivers with [Display Driver Uninstaller (DDU)](https://www.guru3d.com/files-details/display-driver-uninstaller-download.html) and reboot.<br>
<img src="https://i.imgur.com/5jiAmUS.png" alt="drawing" width="600"/>

2. You will have to **disable the use of signed drivers** ([How To Disable Driver Signature Enforcement](https://www.youtube.com/watch?v=C9M2l5vp5co), [How to disable mandatory use of signed drivers](https://answers.microsoft.com/es-es/windows/forum/all/windows-10-c%C3%B3mo-deshabilito-el-uso/778da35d-deab-4a99-84fb-02a274bf5fc5))<br>
<img src="https://i.imgur.com/RKjWZOh.png" alt="drawing" width="600"/>

3. Download and extract zip file containing original [Realtek HD audio drivers R2.80](https://www.techspot.com/drivers/driver/file/information/18007/) (In my case I use the version **R2.80**).<br>
<img src="https://i.imgur.com/uuQeN5Q.png" alt="drawing" width="600"/>

4. Use [Pihto's patch](https://www.techpowerup.com/forums/attachments/realtek-hd-sound-driver-patch-zip.99391/) to patch the DLL files (the password is **''realtek''**). The target filenames are listed on the patcher window. They begin with **"rltkAPO64.dll, rltkAPO.dll"** and may be in "win32" and "win64" subfolders of the Realtek package. You will have to manually select each file to patch and run the patcher multiple times to patch all matching files.<br>
<img src="https://i.imgur.com/0lfPjpt.png" alt="drawing" width="600"/>

5. Now run the Realtek setup program. You may be asked to install **unsigned drivers**. Choose **yes**.<br>
<img src="https://i.imgur.com/3LRw8ft.png" alt="drawing" width="600"/>

6. Do not immediately reboot. Instead, open regedit and ensure the **"DisableProtectedAudioDG"** registry fix is still present. If not, add it again. You need to create it for that, **select right click on the blank => New => DWORD (32 bit) value** and then name it **''DisableProtectedAudioDG''** with hex value **''1''**<br>

```
REGEDIT4
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Audio]
"DisableProtectedAudioDG"=dword:00000001
```
<img src="https://user-images.githubusercontent.com/69399372/154792482-039e2ef6-0ac5-449b-8ad7-6ff22f859c68.png" alt="drawing" width="600"/>

7. Reboot, and **Dolby Digital Live/DTS Interactive** should be available.<br>
<img src="https://user-images.githubusercontent.com/69399372/154792554-4750fdfe-b843-44a4-acc3-062a1530f11d.png" alt="drawing" width="600"/>

8. Working properly on **Windows 10/11** with Realtek version **R2.80**<br>

This guide only works for the **S/PDIF** interface and will unlock **Dolby Digital Live** and **DTS Connect**<br>

<img src="https://user-images.githubusercontent.com/69399372/154156378-87bf1406-8242-451b-8f20-5415edff27c7.png" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/154158010-72110b9d-54ad-41b7-9587-832424688e8b.png" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/154156422-c7e02fb7-72cd-4e69-941b-42233a3abf4f.png" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/154156457-30987569-a326-4e82-9928-8291708ba45a.png" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/154156477-bdae5787-24ef-4ed8-8021-a7baa31c128a.png" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/154156529-f24494ca-c8ef-4ed7-97b5-e63861921f15.png" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/154792537-2711ace8-fe95-4ffc-a27a-e88ac5f03a3b.png" alt="drawing" width="600"/>
<img src="https://user-images.githubusercontent.com/69399372/154792554-4750fdfe-b843-44a4-acc3-062a1530f11d.png" alt="drawing" width="600"/>
