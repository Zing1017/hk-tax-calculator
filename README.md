# hk-tax-calculator

2026/27 香港薪俸稅計算機（單一 HTML 檔）。

## 放到 Blog（iframe 嵌入）

### 1) 先公開頁面（GitHub Pages）

本 repo 已內建 `.github/workflows/deploy-pages.yml`，用 GitHub Actions 自動發佈。

1. 將最新程式碼 push 到 `main`
2. 到 GitHub Repo 的 Settings → Pages
3. Source 選 `GitHub Actions`
4. 到 Actions 頁面確認 `Deploy static site to GitHub Pages` 成功
5. 成功後可用：`https://zing1017.github.io/hk-tax-calculator/`

### 2) 貼到 Blog 文章 HTML

把以下程式碼貼到文章的 HTML 區塊：

```html
<div style="width:100%;max-width:900px;margin:0 auto;">
	<iframe
		src="https://zing1017.github.io/hk-tax-calculator/"
		title="2026/27 薪俸稅計算機"
		width="100%"
		height="1700"
		style="border:0;border-radius:12px;overflow:hidden;"
		loading="lazy"
		referrerpolicy="no-referrer-when-downgrade"
		allowfullscreen>
	</iframe>
</div>
```

### 3) 高度建議

- 目前表單較長，`height` 建議先用 `1600` 到 `1800`。
- 如 blog 平台支援響應式容器，可只保留 `width="100%"`。

## 本機預覽

直接打開 `index.html` 即可使用。

## 404 排錯（你剛遇到嗰種）

- 確認已 push 包含 `.github/workflows/deploy-pages.yml` 的 commit。
- 確認 Settings → Pages 的 Source 係 `GitHub Actions`。
- 去 Actions 檢查 workflow 有冇紅色失敗；如有，先修正再重新執行。
- 首次發佈通常要 1-5 分鐘，未完成前打開網址會見到 404。