# Translucent-System-Bar
如果想修改系統通知欄的顏色

步驟流程:
1. 分別在values, values-v19, values-v21的style.xml, 添加以下Theme
原因是: 讓系統可以根據SDK的版本選擇對應的Theme進行設置
