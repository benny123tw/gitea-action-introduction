# Scripts for my talk

## English Version (5-7 minutes)

### Introduction (30 seconds)
"Hello everyone! Today I'm excited to talk about GitHub Actions and Gitea Actions. We'll explore how to write your first action and understand the key differences between these two platforms."

### What are GitHub Actions? (1 minute)
"GitHub Actions is a powerful CI/CD service that helps automate your software workflows. It allows you to create custom workflows that automatically build, test, and deploy your code. The best part? You can run these actions locally using a tool called 'act'."

[Show the GitHub Actions image]

### Running Actions Locally (1 minute)
"Let me demonstrate how we can run GitHub Actions locally using 'act'. This is particularly useful for testing your workflows before pushing them to GitHub."

[Play the video demonstration]

### Gitea Actions Introduction (1 minute)
"Now, let's talk about Gitea Actions. Gitea has implemented its own version of Actions, which is very similar to GitHub's implementation. However, there are some key differences that make Gitea Actions unique."

### Key Differences (1 minute)
"Gitea Actions offers some advantages over GitHub Actions:
- You can write actions in pure Go
- Actions can run directly from any Git repository
- It's based on the 'act' tool but with custom additions"

### Writing Your First Action (2 minutes)
"Let's look at how to write your first action. It all starts with an 'action.yml' file. Here's what you need to know:
1. Define your inputs and outputs
2. Choose how to run your action (Docker, JavaScript, Composite, or Go)
3. Write your action code
4. Test it locally
5. Publish it to the marketplace"

[Show examples of different action types]

### Conclusion (30 seconds)
"I hope this introduction has inspired you to try writing your own actions. Whether you're using GitHub or Gitea, Actions are a powerful way to automate your workflows. Thank you for listening!"

## 繁體中文版本 (5-7 分鐘)

### 開場白 (30 秒)
「大家好！今天我很高興能和大家分享 GitHub Actions 和 Gitea Actions。我們將探討如何撰寫你的第一個 action，並了解這兩個平台之間的主要差異。」

### 什麼是 GitHub Actions？(1 分鐘)
「GitHub Actions 是一個強大的 CI/CD 服務，可以幫助你自動化軟體工作流程。它允許你創建自定義工作流程，自動構建、測試和部署你的程式碼。最棒的是，你可以使用 'act' 工具在本地運行這些 actions。」

[展示 GitHub Actions 圖片]

### 本地運行 Actions (1 分鐘)
「讓我示範如何使用 'act' 在本地運行 GitHub Actions。這對於在推送到 GitHub 之前測試你的工作流程特別有用。」

[播放視頻示範]

### Gitea Actions 介紹 (1 分鐘)
「現在，讓我們來談談 Gitea Actions。Gitea 實現了自己的 Actions 版本，與 GitHub 的實現非常相似。然而，有一些關鍵差異使 Gitea Actions 獨具特色。」

### 主要差異 (1 分鐘)
「Gitea Actions 相比 GitHub Actions 有一些優勢：
- 你可以使用純 Go 語言編寫 actions
- Actions 可以直接從任何 Git 倉庫運行
- 它基於 'act' 工具但加入了自定義功能」

### 撰寫你的第一個 Action (2 分鐘)
「讓我們看看如何撰寫你的第一個 action。這一切都從 'action.yml' 文件開始。以下是需要知道的內容：
1. 定義你的輸入和輸出
2. 選擇運行方式（Docker、JavaScript、Composite 或 Go）
3. 編寫你的 action 代碼
4. 在本地測試
5. 發布到市場」

[展示不同類型的 action 範例]

### 結論 (30 秒)
「希望這個介紹能激勵你嘗試撰寫自己的 actions。無論你使用 GitHub 還是 Gitea，Actions 都是自動化工作流程的強大工具。謝謝大家的聆聽！」