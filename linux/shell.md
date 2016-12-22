##### 解压rar目录中的所有rar文件 不保持路径 强制覆盖
```bash
find ../rar -name "*.rar" |  xargs -n1 -i unrar e  -o+  "{}"
 ```
 
 ##### 修复目录中的视频文
 ```bash
 mkdir bak && cd bak && find ../avi -name "*.avi" |  xargs -n1 -i ffmpeg -i {} -codec copy /disk/data2/baidu/SSM框架视频/bak/fix-`basename "{}"`
  ```