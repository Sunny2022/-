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

不识别？未解决，先自己编译一个ovmf.fd 吧



编译先安装nasm，然后一定要用 vs2022打开代码块执行edksetup.bat ，然后更改 Conf/target.txt
ACTIVE_PLATFORM       = MdeModulePkg/MdeModulePkg.dsc
TARGET                = DEBUG  # 调试模式
TARGET_ARCH           = X64    # 64位架构
TOOL_CHAIN_TAG        = VS2022 # 使用VS2022工具链

在build，
目前报错
<img width="2852" height="1006" alt="image" src="https://github.com/user-attachments/assets/a60ecea3-7174-4e70-b290-42ec6fc04279" />

