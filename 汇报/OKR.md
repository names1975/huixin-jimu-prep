# OKR 工作汇报

## O：在 10 月 1 日前具备具身智能竞赛基础工程能力

### KR1：完成 Ubuntu 双系统安装
- 进度：1.忙了半天，终于装好了（2个小时
- 证据：<img width="4064" height="3048" alt="IMG_20260924_232355" src="https://github.com/user-attachments/assets/608f8916-5c7a-4295-8b2f-27ff90920ccb" />
2.系统升级，内核从 6.8.0-38 变成了 6.8.0-138，网卡驱动错位了。WiFi驱动没了，查了一坨东西，但USB不支持，又没法连网线，没办法。只能用 U 盘离线强装 Linux firmware 和内核模块，最后又切回 6.8.0-40 内核恢复网络，修复了 apt 源（3个小时
<img width="1455" height="341" alt="wx_camera_1790254808062" src="https://github.com/user-attachments/assets/a15e7598-f75e-45db-bb92-a8d8352a475d" />
<img width="1080" height="1920" alt="wx_camera_1790254614225" src="https://github.com/user-attachments/assets/f78bbaea-1027-40b6-8ef9-1177ad085560" />
<img width="1920" height="1080" alt="wx_camera_1790254682142" src="https://github.com/user-attachments/assets/5deb1a55-34d6-4ec8-ac5f-8e320249a3f8" />
<img width="1920" height="1080" alt="wx_camera_1790254473356" src="https://github.com/user-attachments/assets/78cabb44-d910-4d2c-b915-0dc397d5588a" />
<img width="1920" height="1080" alt="wx_camera_1790254484885" src="https://github.com/user-attachments/assets/66267d32-5f59-4a5f-a378-9c9538261df7" />
<img width="4064" height="3048" alt="IMG_20260924_232404" src="https://github.com/user-attachments/assets/2df8332a-d63d-4afa-96be-21dc036070ed" />
<img width="1455" height="341" alt="mmexport1790254840211" src="https://github.com/user-attachments/assets/299c539f-b5f2-41db-aa2d-572a651eba04" />
3.在试图给蓝牙装开机自启，以及试图无需密码登录的时候，乌班图系统崩了，反反复复修了几次，结果进去之后网卡驱动没了。又试了 USB 连接，以及试图用 U 盘重装驱动，但是不知道为什么这次驱动与乌班图系统又不兼容，导致现在网卡驱动还是装不好。只能重装系统，导致数据丢失。
  <img width="4064" height="3048" alt="IMG_20260930_165641" src="https://github.com/user-attachments/assets/4bae0737-b538-4a53-9e19-8ca33b6cca58" />
<img width="4064" height="3048" alt="IMG_20260930_153821" src="https://github.com/user-attachments/assets/1e93eb36-f616-41bf-a6d7-3853b0d6bd29" />
<img width="4064" height="3048" alt="IMG_20260930_154840" src="https://github.com/user-attachments/assets/00601c31-34bf-4a8a-8495-1aa657414be6" />
<img width="4000" height="3000" alt="IMG_20260930_154433" src="https://github.com/user-attachments/assets/d0aba44b-9db6-4d59-8e4d-24dcdcd05c51" />
<img width="4064" height="3048" alt="IMG_20260930_153352" src="https://github.com/user-attachments/assets/58a9783f-3c58-4f27-87d8-198ab4dc72f3" />



### KR2：完成 Linux 基本使用
- 进度：学了一些基础命令，包括目录、文件等 Linux 必备的知识
- 证据：<img width="1080" height="2382" alt="1790333109374" src="https://github.com/user-attachments/assets/e86409db-13dd-4e65-a8c6-83021a2747ef" />
<img width="1080" height="2382" alt="1790333101308" src="https://github.com/user-attachments/assets/bc7ca2af-6461-4b51-be8d-8b501c55748b" />


### KR3：完成 SolidWorks 草图+特征练习
- 进度：学了基础的草图操作
- 证据：(好像不支持文件类型，怎么上传呢?)


### KR4：完成 GitHub 仓库与每日更新
- 进度：
- 证据：嗯，你都进来了，就不需要给你证据了吧。

### KR5：完成 YOLO 塑料瓶训练
    O（目标）：在 Ubuntu 22.04 环境下，独立完成基于 YOLOv11 的塑料瓶数据集训练与推理。

    KR1（环境配置与硬件排障）：

        完成双系统 Ubuntu 安装及 Miniconda 虚拟环境搭建。

        踩坑记录1：RTX 5060 驱动安装失败（nvidia-smi 报 No devices were found）。

            排查过程：查阅日志发现需要 open 内核模块，安装 610-open 后依旧报错。

            解决方案：修改 GRUB 启动参数 acpi_osi=Linux 绕过联想 SBIOS 兼容性问题，成功加载 GPU。

        踩坑记录2：训练中断与防休眠设置。

            问题：离开电脑后系统自动休眠导致训练进程被杀。

            解决：配置系统电源选项，以及使用 nohup 命令让训练在后台抗干扰运行。

    KR2（数据准备）：

        从 Kaggle 下载 8000 张塑料瓶数据集，修改 data.yaml 指定绝对路径，并将文件夹重命名为纯英文无空格路径。

    KR3（模型训练与效果验证）：

        使用 yolo train 成功跑完 50 轮

        成果展示：<img width="2560" height="1600" alt="截图 2026-09-27 16-34-16" src="https://github.com/user-attachments/assets/9772d6f9-130e-4c36-a593-9d28f31f50d3" />
<img width="2560" height="1600" alt="截图 2026-09-27 16-33-54" src="https://github.com/user-attachments/assets/bd4399c9-8692-42a4-bb6d-39986517a45c" />
<img width="2560" height="1600" alt="截图 2026-09-27 16-33-29" src="https://github.com/user-attachments/assets/2891fcf4-a662-4fcc-8cb0-28644d191172" />
<img width="2560" height="1600" alt="截图 2026-09-27 16-32-46" src="https://github.com/user-attachments/assets/ef377817-a0d9-4f94-b1bd-10b56a7453c5" />
<img width="2560" height="1600" alt="截图 2026-09-27 16-32-23" src="https://github.com/user-attachments/assets/170157de-c90b-4b7f-a861-19778e76b562" />
<img width="2560" height="1600" alt="截图 2026-09-27 16-30-46" src="https://github.com/user-attachments/assets/4df8d138-fc33-4724-92b3-0f8afc0f8f3d" />
<img width="739" height="671" alt="截图 2026-09-27 16-27-41" src="https://github.com/user-attachments/assets/48090bcd-2a35-4939-bc17-0aa3b69916ca" />


## 问题与解决
- 问题：
- 怎么查：
- 怎么解决：
