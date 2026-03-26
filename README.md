Git 基本操作指令

    這些指令主要用於您本地電腦上的檔案版本管理：

    環境設定與初始化：
    git --version：檢查電腦是否已正確安裝 Git。
    git config --global user.name "您的姓名"：設定版本紀錄中的作者姓名。
    git config --global user.email "您的 Email"：設定作者的電子郵件地址。
    git init：將目前的資料夾轉換為具有版本管理功能的 Git 儲存庫（會建立隱藏的 .git 資料夾）。
    檔案狀態與追蹤：
    git status：檢查目前目錄中每個檔案的狀態（如：未追蹤、已修改、準備提交等）。
    git add <檔案名稱>：將特定檔案加入暫存區 (Staging Area)，準備進行拍照存檔。
    git add .：將當前目錄中「所有」變更的檔案一次全部加入暫存區。
    提交版本 (拍照存檔)：
    git commit -m "訊息內容"：將暫存區的檔案正式存成一個版本（快照），-m 後方需加上該次變更的說明。
    檢視紀錄與還原：
    git log：列出詳細的提交歷史紀錄。
    git log --oneline：以簡潔的一行格式顯示提交紀錄。
    git diff <ID> <檔案名稱>：比較目前檔案與特定版本（ID）之間的內容差異。
    git checkout <ID> <檔案名稱>：將特定檔案還原到先前的某個版本（需再執行 commit 記錄此變動）。
    git reset --hard <ID>：將「所有」檔案強制還原到指定的版本點，注意此操作不可逆，之後的紀錄會被捨棄。
--------------------------------------------------------------------------------

Git 與 GitHub 互動指令

    這些指令用於將本地端的資料與 GitHub 雲端平台同步或進行多人協作：

    連結與上傳：
    git remote add origin <GitHub 網址>：建立本地儲存庫與遠端 GitHub 儲存庫的連結。
    git branch -M main：將預設的主線名稱從 master 改為 main。
    git push：將本地端的新版本推送到 GitHub 雲端。
    取得與同步：
    git clone <GitHub 網址>：將雲端的儲存庫完整複製一份到本地電腦。
    git pull：從 GitHub 下載最新的變更並合併到本地端，確保資料同步。
    分支協作：
    git checkout -b <分支名稱>：建立一個新的分支並切換過去，讓開發者可以在不影響主線的情況下嘗試新功能。
    git push origin <分支名稱>：將特定分支的變更推送到 GitHub。