### [Pixiv 标签](https://github.com/DowneyRem/PixivSource/blob/main/PixivRemark.md) 替换规则
不知道为什么 [Pixiv 标签替换规则](https://raw.githubusercontent.com/DowneyRem/PixivSource/main/replace_source.json) 不能一键导入，所以只好这样一条条列出来了

### 去P站标记
去除 [newpage] 
[chapter:本章标题] 
[pixivimage:作品ID] 
[jump:链接目标的页面编号]  

查找正则，替换为空
```
(\[(newpage|chapter|pixivimage)\:*)|([0-9]{1,10})|(\])
```

### 去P站网页标记
去除 [[jumpuri:标题 > 链接目标的URL]] 
[[rb:汉字 > 假名]]   
查找正则，替换为空
```
(\[+(jumpuri|rb)\:)|(\s*>\s*)|(\]+)
```

### 去网址
查找正则，替换为空
```
(?i)(https?://)?([wｗＷ]{3}\.)[\w\?&=\/\.]+|(https?://)?[\w\?&=\/]+\.[\w\?&=\/\.]+
```
