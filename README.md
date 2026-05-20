# MakeCode 技能地圖範例

這是一份範例技能地圖,包含三條獨立的學習路徑。你可以在這裡瀏覽內容:
https://arcade.makecode.com/skillmap#github:orangeapple-lloyd/pxt-skillmap-tw/skillmap.md

託管在 GitHub 上的技能地圖,載入方式與一般教學相同,使用以下格式的 URL 片段:

`#github:[組織名稱]/[儲存庫名稱]/[markdown 檔名]`

## 語法

技能地圖的定義位於 `skillmap.md` 檔案中。技能地圖本身的中繼資料(metadata)寫在最上層的標題下方:

- `id`:標題後方的字串(例如 `# sample`)。不可包含空白。
- `name`:技能地圖的標題,會顯示在頁面上的橫幅中。
- `description`:技能地圖內容的描述,也會顯示在橫幅中。
- `infoUrl`(選填):指向教師端額外資訊頁面的網址。

### 學習路徑(Learning Paths)

一份技能地圖由一或多條「路徑」組成,每條路徑都是一連串依序排列的活動。每條路徑中的第一個活動會預設解鎖,完成後會自動解鎖下一個活動。

學習路徑以二級標題(`##`)定義,具有下列屬性:

- `id`:標題後方的字串(例如 `## interface`)。必須在這份技能地圖中唯一。
- `name`:路徑的標題,顯示在所連結活動的上方。
- `description`:額外的說明文字(目前不會顯示)。
- `completionUrl`:完成整條路徑時顯示的證書 URL。

### 活動(Activities)

每條學習路徑有多個活動,以三級標題(`###`)定義。目前「活動」就是一份 MakeCode 教學,具有下列屬性:

- `id`:標題後方的字串(例如 `### space-activity1`)。必須在這份技能地圖中唯一。
- `name`:活動的標題,顯示在活動卡片上。
- `type`:活動類型。目前必須是 `tutorial`。
- `description`:活動的詳細說明,顯示在卡片背面。
- `tags`:活動卡片底部顯示的描述性標籤。
- `url`:教學的連結。教學撰寫與連結格式的細節,請見 [MakeCode 教學文件](https://makecode.com/writing-docs/user-tutorials)。
- `imageUrl`:活動卡片正面顯示的圖片 URL。

## Fork 自己用

如果你 fork 了這個 repo,請務必把所有指向 https://github.com/orangeapple-lloyd/pxt-skillmap-tw 的 URL 改成你自己 fork 後的 repo 網址,否則你的修改不會生效。

## 貢獻

本專案歡迎貢獻與建議。多數貢獻需要你同意 Contributor License Agreement(CLA),宣告你有權利並確實授予我們使用你貢獻內容的權利。詳情請見 https://cla.opensource.microsoft.com 。

當你提交 pull request 時,CLA 機器人會自動判斷你是否需要提供 CLA,並會在 PR 上加註相對應的狀態(例如狀態檢查、留言)。依照機器人提供的指示操作即可。在所有使用此 CLA 的 repo 中,你只需要做一次。

本專案採用 [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/)。更多資訊請見 [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) 或聯絡 [opencode@microsoft.com](mailto:opencode@microsoft.com)。

## 商標

本專案可能包含專案、產品或服務的商標或 logo。Microsoft 商標或 logo 的授權使用須遵循 [Microsoft 商標與品牌規範](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general)。在修改版本中使用 Microsoft 商標或 logo 不得引起混淆或暗示獲得 Microsoft 贊助。任何第三方商標或 logo 的使用須遵循該第三方的政策。
