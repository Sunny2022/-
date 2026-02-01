安装  MINGW64 ，然后按照： https://www.qemu.org/download/#windows
执行
pacman -S mingw-w64-x86_64-qemu
<img width="1044" height="138" alt="image" src="https://github.com/user-attachments/assets/389e30d5-7709-487c-a781-13fbd271fede" />

但是直接执行 qemu-system-x86_64 命令运行的是 seabios?
<img width="1744" height="972" alt="image" src="https://github.com/user-attachments/assets/a8a98a6d-a2cf-4d07-a5f0-8ad066b20c9c" />

找到UEFI的fd文件在 /d/Program\ Files/msys64/mingw64/share/qemu/
<img width="2816" height="431" alt="image" src="https://github.com/user-attachments/assets/32b1c3f1-9376-4c5c-b346-cb4bd959359d" />

$ ls /d/Program\ Files/msys64/mingw64/share/qemu/
<img width="2825" height="437" alt="image" src="https://github.com/user-attachments/assets/515b62e3-b9e5-4901-ad40-9dffb7e061a4" />

不识别？未解决
