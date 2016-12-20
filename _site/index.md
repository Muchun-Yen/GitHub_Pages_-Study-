# 利用GitHub Pages來放置Web Page


## **Step1 建立此project site reposity 名稱為[GitHub_Pages_-Study-]**
這裡有個地方要留意，明明我本來的命名是GitHub_Pages_\[Study\]
系統在Reposity建立的時候，自行的將**\[** 與 **\]**字元變成了**\-**

### 這個原因...先擱置(╯-_-)╯ ~╩╩


## **Step2 進入GitHub_Pages_-Study- 的Setting頁面找到GitHub Pages選項。**
按下Theme chooser選項裡的Choose a theme按鈕。選擇**Midnight theme**...原因是我個人喜歡這款。
GitHub會自動帶出GitHub_Pages_-Study-/index.md的編輯頁。
我們不修改任何文字，只在下方的Commit changes選項的Update欄位填入 **the original version commit** ...內容是描述你這次commit是為何。
選擇Create a new branch for this commit and start a pull request.我們要新增名稱為**gh-pages**的branch
因為GitHub pages雖然可以使用master為branch,但是建議還是使用gh-pages。原因來自Jekyll 網頁中提到的Project pages通常是使用gh-pages來作為branch，
或者是使用master branch 而去搭配使用/doc這個folder。
[https://jekyllrb.com/docs/github-pages/](https://jekyllrb.com/docs/github-pages/)

### 背後的原因...先擱置(╯-_-)╯ ~╩╩ ]。先當個照本宣科的門外漢先！

完成之後將會看到一個新的branch；名為gh-pages被建立。
然後我們在進入到Reposity的Setting頁面在左邊的選單中選擇Branch選項我們要將Default Branch改為gh-pages。
在Default branch的選項的下拉式選單裡面選到gh-pages之後然後按下在它旁邊的Update button。就完成Default branch的設定了。
然後我們在Setting 裡面GitHub Pages選項也要將Source 由master branch改為gh-pages branch後按下在它旁邊的Save button
我們可以在網頁中開啟GitHub Page所建立的這個Project Page網頁。**https://muchun-yen.github.io/GitHub_Pages_-Study-/**

然後我們就可在本機端利用**git clone https://github.com/Muchun-Yen/GitHub_Pages_-Study-.git** 去fork這個reposity了。


## **Step3 Test in the local machine **

在本地端機器下載這個Project page的reposity後我們可以看到幾個重點
1. _config.yml 這是用來儲存Jekyll的一些configuration data。
	裡面只有一行 **theme: jekyll-theme-midnight** 告知使用的Jekyll theme 是midnight
2. index.md 這個是makedown形式的網頁本體。我們要自行修改。
3. 我們要自己建立README.md
4. 我們應該要可以在本地端以Jekyll來查看我們的網頁設計

我們直接來看在本地端以Jekyll來查看我們的網頁設計

我的另外一篇Jekyll安裝是設定在Ubuntu 14.04LTS上面安裝。請依照步驟完成Jekyll的環境設定。
再來是我們要在目前的git clone下來的folder裡面新增加一個檔案-**Gemfile**
裡面的內容為 gem 'github-pages', group: :jekyll_plugins

然後我們執行

```
$ jekyll server
```

我們就可以在本機端的瀏覽器localhost:4000上面看到index.md的內容了。
