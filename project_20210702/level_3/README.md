## 你真的很棒！
完成了前兩個關卡的你真的很厲害！
最後還有兩個問題要解決，現在再讓我們花點耐心來看看最完整的程式。

現在先點開 index.html 試玩一次了解這個專案的操作流程。

試玩後我們來看看程式是怎麼設計的，
在程式中我們新增了一個 data.js 檔案，我們把所有題目的資料寫在裡面，
接著在網頁中用 script 標籤把該檔案載入，在後面的 js 程式就可以透過 data 這個變數去取得題目資料，
試著點開檔案觀察看看吧！

接著看到 index.js 程式，
我們可以直接滑到最下面，這裡寫了所有要「點擊」互動的程式，清楚的告訴電腦什麼元素被點擊就要執行什麼程式，
如果要找出程式問題，就可以從這裡開始查找！

# 任務1 - BUG done
當來到第 10 題最後一題時，點擊下一題預期要跳出警告「已經是最後一題！」但沒有，
網頁右按鍵「查看」，打開主控台出現了紅色的錯誤訊息：
index.js:12 Uncaught TypeError: Cannot read property 'title' of undefined
at renderQuiz (index.js:12)

提示：
似乎是下一題的程式中條件判斷寫錯了，請試著修改這個 bug 吧！


# 任務2 - 防止作弊
使用者提交考卷後就會進入檢討模式，但在檢討模式下仍然可以修改答案，為了避免這個問題我們必須在按下選項後，
判斷是不是仍在作答，是的話才能會去更新 myAnswer 裡的紀錄並切換按鈕顏色。

提示：
你需要一個條件判斷防止在檢討模式還能修改答案。