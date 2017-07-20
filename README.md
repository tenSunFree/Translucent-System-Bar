# Translucent-System-Bar
如果想修改系統通知欄的顏色

步驟流程:
1. 分別在values, values-v19, values-v21的style.xml, 添加以下Theme  
原因是: 讓系統可以根據SDK的版本選擇對應的Theme進行設置

values
   
```xml
<style name="ImageTranslucentTheme" parent="AppTheme">
    <!--在Android 4.4之前的版本上運行, 直接跟隨系統主題-->
</style>
```
  
values-v19
   
```xml
<style name="ImageTranslucentTheme" parent="Theme.AppCompat.Light.DarkActionBar">
    <item name="android:windowTranslucentStatus">true</item>
    <item name="android:windowTranslucentNavigation">true</item>
</style>
``` 

values-v21
   
```xml
<style name="ImageTranslucentTheme" parent="Theme.AppCompat.NoActionBar">
    <item name="android:windowTranslucentStatus">false</item>
    <item name="android:windowTranslucentNavigation">true</item>
    <!--Android 5.x開始 需要把顏色設置透明, 否則導航欄會呈現系統默認的淺灰色-->
    <item name="android:statusBarColor">@android:color/transparent</item>
</style>
``` 
  
2. 在AndroidManifest.xml中設置Theme
   
```xml
android:theme="@style/ImageTranslucentTheme"
``` 

3. 在Activity的背景, 添加想要的顏色
   再添加android:fitsSystemWindows: true
   
![image](http://i.imgur.com/kp7xkOT.png)  

