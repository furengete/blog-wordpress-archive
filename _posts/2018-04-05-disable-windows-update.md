---
title: "禁用 Windows update"
date: "2018-04-05"
---

禁用Windows update服务  
1、按WIN+R 打开运行，输入 services.msc 回车 然后找到 “Windows update”服务，双击后设置为禁用 应用即可;

为windows更新指定一个错误的升级服务器地址  
1、按“Win+R”组合键打开运行输入“gpedit.msc”再点“确定”;  
2、打开“本地组策略编辑器”展开“管理模版”→“Windows组件”;  
3、接着双击“Windows组件”找到“Windows Update;  
4、在“Windows Update”内找到“指定Intranet Microsoft更新服务位置”;  
5、选中“指定Intranet Microsoft更新服务位置”右键编辑;  
6、将“未配置”框选为“已启用”。在“设置检测更新的Intranet更新服务”填写127.0.0.1 (注：127.0.0.1为本机IP)
