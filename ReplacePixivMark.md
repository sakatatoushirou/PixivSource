### [Pixiv 标签](https://github.com/DowneyRem/PixivSource/blob/main/PixivRemark.md) 替换规则
头一次写正则，写得不好还请见谅  
不知道为什么 [Pixiv 标签替换规则](https://raw.githubusercontent.com/DowneyRem/PixivSource/main/replace_source.json) 不能网络导入，所以只好这样一条条列出来了

### 去P站标记
去除 [newpage] 
[chapter:本章标题] 
[pixivimage:作品ID] 
[jump:链接目标的页面编号]  

查找正则`(\[(newpage|chapter|pixivimage)\:*)|([0-9]{1,10})|(\])`，替换为空  
替换范围`https://www.pixiv.net/novel/`  

### 去P站网页标记
去除 [[jumpuri:标题 > 链接目标的URL]] 
[[rb:汉字 > 假名]]   
查找正则`(\[+(jumpuri|rb)\:)|(\s*>\s*)|(\]+)`，替换为空  
替换范围`https://www.pixiv.net/novel/`  

### 去网址
这条是直接抄的，就这条能正常导入。拿来主义真好  
查找正则`(?i)(https?://)?([wｗＷ]{3}\.)[\w\?&=\/\.]+|(https?://)?[\w\?&=\/]+\.[\w\?&=\/\.]+`，替换为空  
替换范围`https://www.pixiv.net/novel/`  
