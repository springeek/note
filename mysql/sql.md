##### 刷测试库专用
```sql
update users set 
name =substring(md5(rand()),1,5),
password=substring(md5(rand()),6,6),
email=CONCAT(substring(md5(rand()),15,6),"@",substring(md5(rand()),27,4),".com"),
age=round(40*rand())+20,
birthday=FROM_UNIXTIME(UNIX_TIMESTAMP()-365*86400*(14+round(30*rand())),"%Y-%m-%d")
```
