# Translucent-System-Bar
如果想修改系統通知欄的顏色

步驟流程:
1. 分別在values, values-v19, values-v21的style.xml, 添加以下Theme  
原因是: 讓系統可以根據SDK的版本選擇對應的Theme進行設置

values
   
![image](http://i.imgur.com/1luqAPx.png)  
  
values-v19
   
![image](http://i.imgur.com/c2C8zYQ.png)  

values-v21
   
![image](http://i.imgur.com/R62rr2H.png) 
  
   
2. 在AndroidManifest.xml中設置Theme
   
![image](http://i.imgur.com/8eswcVK.png)  

3. 在Activity的背景, 添加想要的顏色
   再添加android:fitsSystemWindows: true
   
![image](http://i.imgur.com/kp7xkOT.png)  

