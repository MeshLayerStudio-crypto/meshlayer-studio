# Changelog / 變更記錄

## 1.0.5

- Fixed: the AI installer failed at the first step on computers with an older pip (for example Python 3.12.1), with "'truststore' must be installed into pip's current environment". The installer now installs truststore first and only then turns the Windows-certificate option on.
- Before installing or running AI generation, the program now checks the graphics hardware and says so up front if the NVIDIA card has under 3 GB of memory, an NVIDIA card has no driver, or the computer only has integrated Intel/AMD graphics (AI generation needs NVIDIA/CUDA; otherwise it falls back to the CPU, which is extremely slow and untested). It suggests the "Import an existing model" mode instead.
- Small graphics cards: the layer-streaming option (borrowing system memory) now also applies to Hunyuan3D-2 and Mini on the first run (before the model is downloaded), and Mini after an out-of-memory fallback; below 3 GB the mesh resolution is lowered to 256 automatically. A card with 2 GB may still be too small: even Mini used about 2.4 GB in our test.

- 修正：舊版 pip（例如 Python 3.12.1 附的）上，AI 安裝程式第一步就失敗（「'truststore' must be installed into pip's current environment」）。現在先安裝 truststore，再啟用 Windows 憑證選項。
- 安裝或執行 AI 生成前，程式會先檢查顯示硬體，並事先告知：NVIDIA 顯卡記憶體低於 3 GB、有 NVIDIA 顯卡但沒裝驅動、或只有 Intel／AMD 內建顯示卡（AI 生成需要 NVIDIA／CUDA，否則退回 CPU，極慢且未測試），並建議改用「匯入既有模型」模式。
- 小顯卡：分層串流（借用主機記憶體）現在也適用於 Hunyuan3D-2 與 Mini 的第一次執行（模型還沒下載時），以及 Mini 因記憶體不足而重試時；低於 3 GB 時網格解析度自動降到 256。2 GB 的顯卡仍可能放不下：我們實測連 Mini 也用到約 2.4 GB。

## 1.0.4

- Fixed: in Simple mode the AMS color bar (A1/A2/... filaments) was hidden after ticking "Also export multicolor 3MF"; it is shown again, and the extra color-quality options stay in Advanced mode.
- Startup check for the Microsoft Visual C++ runtime now tests `VCRUNTIME140_1.dll` directly. Older 2015-2017 runtimes are listed as installed but lack this file and make numpy fail to load ("DLL load failed"). The startup error dialog now explains this and can open Microsoft's official download page.
- `Install_VC_Runtime.bat` and the README mention this case.

- 修正：簡易模式勾選「同時輸出多色 3MF」後，AMS 色條（A1／A2… 線材）被誤藏；現在會顯示，額外的色彩品質選項仍只在進階模式出現。
- Microsoft Visual C++ 執行庫的啟動檢查改為直接測試 `VCRUNTIME140_1.dll`。舊版（2015–2017）執行庫雖登記為已安裝，卻缺這個檔案，會讓 numpy 載入失敗（「DLL load failed」）。啟動失敗對話框現在會說明這點，並可開啟 Microsoft 官方下載頁。
- `Install_VC_Runtime.bat` 與 README 補上這種情況的說明。

## 1.0.3

- If the program cannot start (for example a missing Microsoft Visual C++ runtime or a blocked numpy file), it now shows a short readable message with the likely cause and saves the full error to `startup_error.log` (in `%LOCALAPPDATA%` under the program's folder) instead of a truncated English dialog.

- 程式無法啟動時（例如缺少 Microsoft Visual C++ 執行庫或 numpy 檔案被擋），改為顯示簡短易懂的訊息與可能原因，並把完整錯誤存到 `startup_error.log`（在 `%LOCALAPPDATA%` 的程式資料夾內），不再是被截斷的英文對話框。

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
