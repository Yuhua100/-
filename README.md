# RestArt-重回健康人生
<p>這是我的畢業專案內容，裡面會詳細記錄我做了什麼事以及未來待辦事項</p>

## 資料收集

目前先暫訂用Mediapipe去做收集復健動作，由於Mediapipe的收集方式通常是以正面為主，所以很難收集較為複雜或是具有角度的動作，但姑且先嘗試去收集。
總共先選定六個動作，分別如下:

| 動作名稱 | 類型 | 描述                         |
| ------- | ---- | ---------------------------- |
| 半蹲    | 下肢  | 雙腳與肩同寬站立，緩慢下蹲至大腿與地面平行，保持背部挺直，再站起來 |
| 提膝    | 下肢  | 站立時將一腿膝蓋抬至與腰同高，保持平衡，然後放下，換另一腿 |
| 弓箭步拉伸 | 全身 | 一腳向前跨步，後腿伸直，前臂伸直，向上舉起 |
| 手臂側舉   | 上肢 | 手往旁邊舉，舉到耳朵旁 |
| 肩胛擠壓/前推 | 上肢 | 抬起手肘與肩同高，肩胛往後擠在一起，維持1～3秒。手肘往前互相靠近，兩肩胛被分開 |
| 鐘擺運動 | 上肢 | 患側手懸空，手伸直畫圓圈 |

- 當初原本預計是收集十個上肢動作跟下肢動作，但後來在做Training的時候發現自身在設置參考基準點(就是人體的正規化)都固定在肩膀，但下半身的動作都基本上以髖關節的地方為基準會比較好，所以才要重新收集資料
- 自己在收集資料的時候仍有一些缺陷，發現自身收集資料的時候會無法完全照全身，因此10/22號的時候也會請林紘宇跟陳琬婷協助收集資料(順便錄製)
- 重新修改了data_collect的程式碼，將x,y,z的維度都考慮進去

## Model Training紀錄

- 使用原始SVM去Train
  感覺效果超級不好，但因為資料少之又少，可能還要想方法去做training的動作，目前已嘗試修改成使用LSTM，RCNN等Deep Learning的模型去做training且持續收集資料，並以Transfer Learning去做感覺會比較好

- 等惠下午將LSTM的程式碼也上傳上去，但這個程式碼並非最終版，還需做一些改進
  
## Model 串接 Unity
  目前已了解如何在Unity跟python相連，並已初步將自身的動作連接到Unity上，後續等待張郁華建設好AR環境，明天會去詳細了解three.js如何跟Mediapipe去相接的部分
## AR Unity 建置環境
  目前10/22號看張郁華跟凃亮伃他們建立的結果如何
## TODO
