##### 解压rar目录中的所有rar文件 不保持路径 强制覆盖
```bash
find ../rar -name "*.rar" |  xargs -n1 -i unrar e  -o+  "{}"
 ```
 ##### 修复目录中的视频文
 ```bash
 find ../avi -name "*.avi" |  xargs -n1 -i echo ' ffmpeg -i "{}" -codec copy `basename "{}"`' >ff.sh && sh ff.sh 
  ```