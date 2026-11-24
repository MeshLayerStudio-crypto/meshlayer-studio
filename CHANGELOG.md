# Changelog / 變更記錄

## 1.0.2

- Import mode: new "Mirror" option (left-right, front-back, up-down).
- New repair report (before/after counts of holes, non-manifold edges, duplicate faces, normals, stray shells); command line `--repair-report FILE`.
- Removed the optional TripoSR engine; AI image-to-3D uses Hunyuan3D only.

- 匯入模式新增「鏡像」選項（左右、前後、上下）。
- 新增修補報告（修補前後的破洞、非流形邊、重複面、法線方向、碎片殼對照）；命令列 `--repair-report 檔案`。
- 移除選用的 TripoSR 引擎，AI 圖片轉 3D 只使用 Hunyuan3D。

## 1.0.1

- Windows 11: no extra console window when starting the program (the app is now built as a windowed program).
- AI installer: pip and git now trust the Windows certificate store, which fixes "self-signed certificate" errors when antivirus or a proxy inspects HTTPS.
- AI installer: Hunyuan3D-2 and Hunyuan3D-2.1 are downloaded at tested versions instead of the latest upstream code.
- Failure messages now point to GitHub Issues.
- Third-party notices list the optional TripoSR engine (MIT).

- Windows 11：啟動程式時不再多開 command 視窗（程式改為無主控台的視窗版）。
- AI 安裝程式：pip 與 git 改用 Windows 憑證庫，修正防毒軟體或代理檢查 HTTPS 時出現的「self-signed certificate」錯誤。
- AI 安裝程式：Hunyuan3D-2 與 Hunyuan3D-2.1 改為下載測試過的固定版本，不再抓上游最新程式碼。
- 失敗訊息改為指向 GitHub Issues。
- 第三方聲明新增選用的 TripoSR 引擎（MIT）。

## 1.0

- First public release (Windows 10 / 11, 64-bit). See the Release page for the download and SHA-256.
- 第一個公開版本（Windows 10／11 64 位元）。下載與 SHA-256 見 Release 頁面。
