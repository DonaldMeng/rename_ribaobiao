# rename_ribaobiao
# -*- coding: utf-8 -*-
# 将“生产日报表”五个汉字去除
import os
name_before1 = os.listdir(r'F:\BaiduYunDownload\examples_python\rb2017.11\rbb')
print "当前目录为: %s" %os.getcwd()
path = r'F:\BaiduYunDownload\examples_python\rb2017.11\rbb'
for i in name_before1:
	olddir = os.path.join(path,i)
	newdir = os.path.join(path,i[10:])
	os.rename (olddir,newdir)


# -*- coding: utf-8 -*-
#将如“11.1”等更改为标准的“11.01”
name_before1 = os.listdir(r'F:\BaiduYunDownload\examples_python\rb2017.11\rbb')
path = r'F:\BaiduYunDownload\examples_python\rb2017.11\rbb'
for i in name_before1:
	if i[2] =='0':
		olddir = os.path.join(path,i)
		newdir = os.path.join(path,i[0:2]+'.'+i[2:])
		os.rename (olddir,newdir)
