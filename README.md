some simple code

# 1.隔一段时间打开一次浏览器
import webbrowser

import time

tb=3
bc=0


print "start"+time.ctime()

while (bc<tb):

    time.sleep(10)
    
    webbrowser.open("stackoverflow.com")
    
    bc+=1
    
    print bc

# 2.按行读取文件
file = open("d:/diaoyan.txt","r") 

while 1:

  lines = file.readlines(100000)
  
  if not lines:
  
    break
    
  for line in lines:
  
   print line   
   
file.close()


# 3.给keyword前插入内容

file = open(‘a’,'r')

content = file.read()

post = content.find(keyword)

 if post != -1:
 
     content = content[:post+len(keyword)]+str+content[post+len(keyword):]
     
     file = open(‘a’,'w')
     
     file.write(content)
     
 file.close()
