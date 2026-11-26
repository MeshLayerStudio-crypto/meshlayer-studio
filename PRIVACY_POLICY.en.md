# MeshLayer Studio Privacy Policy

> **Language Notice:** This document is an English translation of the Traditional Chinese Privacy Policy. In the event of any discrepancy or conflict between the two versions, the Traditional Chinese version shall prevail.

**Version:** 2.5 | **Effective Date:** 2026-10-27 | **Last Revised:** 2026-11-26 | **Provider:** MeshLayer Studio | **Contact:** meshlayer.studio@gmail.com

---

### 1. Overview
- **Local-First; Zero Telemetry:** MeshLayer Studio (the "Software") processes all images, 3D models, and parameters locally on your computer. It contains no user accounts, analytics, automatic crash reporting, or telemetry, and never uploads your files to the Provider's servers.
- **No Background Connections by Default:** All outbound network requests—including installing the AI runtime, downloading Gridfinity/OpenSCAD components, downloading color tables, installing the Visual C++ runtime, optional version checks, and opening external support links—occur solely after you **actively click a button or explicitly opt in / grant consent** (see Sections 4 and 6).

### 2. Local Data Processing and Storage
The Software reads and stores the following data solely on your local device. **None of this data is transmitted to the Provider:**

| Data Category | Local Storage Location | Purpose | Leaves Your Computer? |
| :--- | :--- | :--- | :--- |
| Input images, imported models, SVG patterns, and logos | Your chosen path; temporarily copied to `output\*_work\source.png` during processing | Generation, coloring, engraving, and inlay processing | No |
| Output files (STL / 3MF / OBJ / previews) | `output\` (inside the app folder) | Delivering finished output files | No |
| Filament library (`filaments.json`) & color overrides (`color_overrides.json`) | App folder | Remembering material and color settings (indexed by image file name and size) | No |
| Imported fonts & external path config | `fonts\user\`, `openscad_path.txt` | Loading custom fonts and your specified OpenSCAD path | No |
| Preferences (`settings.json`) | `%LOCALAPPDATA%\MeshLayerStudio\` | Storing UI preferences, printer model, build plate size, and AI environment path | No |
| Parameter files (`*_work\params.json`, `.mls.json`, etc.) | Working folder or your chosen save path | Storing text, size, color parameters, and **local file paths** of SVG/logo files and parts imported via "Combine and Pattern" (not image or model contents); **review before sharing or submitting bug reports, as engraved text and local paths (potentially containing your username) are recorded** | No |
| Font list cache (`mpl_cache\`) | `%LOCALAPPDATA%\MeshLayerStudio\mpl_cache\` | Accelerating system font scanning at startup | No |
| AI runtime & model weight cache | `%LOCALAPPDATA%\MeshLayerStudio\ai\` and `%USERPROFILE%\.cache\huggingface` | Local AI inference (approx. 4–5 GB) | No (connects to third-party sources only during download) |
| Run log (LOG) | Displayed inside the app window | Local troubleshooting | No (shared only if you manually copy and email it) |

### 3. Personal Data in User Images
Photos you process may contain faces, home interiors, license plates, or EXIF location metadata. The Software neither reads nor transmits EXIF metadata. Please do not process photos of other individuals without their consent.

### 4. Optional Network Features and Third-Party Services
When you actively trigger or consent to the following optional features, the Software connects directly to the relevant third-party services, which handle standard connection data (such as IP addresses and HTTP headers) under their own privacy policies. **The Software never sends your images or models to any third party:**
1. **Install AI Runtime:** Upon your click and consent, downloads packages and weights from PyPI, PyTorch (`download.pytorch.org`), GitHub (Hunyuan3D source code), and Hugging Face (model weights). Missing Git/Python or the optional OpenSCAD installation is handled via Microsoft's `winget`.
2. **Gridfinity Engine "Download and Set Up Automatically":** Upon your consent, connects only to `files.openscad.org` (OpenSCAD snapshot) and GitHub (`kennetek/gridfinity-rebuilt-openscad`), unpacking into `%LOCALAPPDATA%\MeshLayerStudio\` without altering system settings. Loaded third-party `.scad` files execute solely locally.
3. **Check for Component Updates (Off by Default):** Prompts once after your first automatic component download and can be toggled or run manually in the Help menu. When enabled, checks at most once per day at startup by reading `files.openscad.org` snapshot lists and GitHub release tags, without personal data and without automatic downloading or installation.
4. **Check for a New Program Version (Off by Default):** Connects only if enabled in the Help menu or triggered manually. When enabled, checks at most once per day at startup by reading the latest stable release from `api.github.com` for `MeshLayerStudio-crypto/meshlayer-studio` (sending only the Software name and version as User-Agent, with no personal data). This feature is notification-only and **never automatically downloads, installs, or replaces files**; check timestamps and skipped versions are stored only locally.
5. **Install Microsoft Visual C++ Redistributable:** Connects only if missing and with your consent; downloads the official installer from Microsoft (`aka.ms`), verifies Microsoft's digital signature, and installs it.
6. **Bambu Studio / Creality Print Color Table:** Reads local files offline first. If not installed and with your consent, downloads a single color table file from Bambu Lab's or Creality's public GitHub repository (download-only, no upload).
7. **HTTPS Certificate Verification:** If antivirus software or a corporate proxy intercepts HTTPS traffic, the AI installation environment verifies certificates via the OS certificate store (`truststore`) without sending data to the Provider.

### 5. Local Region Detection (AI Compliance)
To comply with territorial restrictions under the upstream Hunyuan3D license, the Software reads Windows' location, regional format, and system language settings **locally** at startup solely to determine whether to display AI features. **Nothing is uploaded or logged, and your location is never inferred from your IP address.**

### 6. Support Links and Payment Privacy
1. **No Background Connections; No Collection:** Clicking a platform button under "Buy Me a Coffee…" opens the external support page in your default browser; no background connection occurs beforehand. **The Software desktop client does not embed payment forms, load tracking scripts, or collect, transmit, or store your payment information.**
2. **Independent Handling by External Platforms:** Once on a third-party support platform (e.g., Ko-fi, ECPay), any personal and payment details you enter are processed independently under that platform's privacy policy.
3. **Direct Contact and Thank-You List:** If you voluntarily email us for inquiries or to join a "Supporter Thank-You List," the Provider retains your email address and chosen nickname solely to **respond to your inquiry and maintain the list**. It is never used for marketing or disclosed to unrelated third parties.
4. **Exercising Your Rights:** Under Article 3 of Taiwan's Personal Data Protection Act (PDPA), you may email `meshlayer.studio@gmail.com` at any time to request access, copies, correction, cessation of processing/use, or deletion of the above data.

### 7. Data Retention and Deletion
Except for direct correspondence under Section 6, all data resides solely on your computer. To completely remove the Software and all local data, delete the application folder (including `output\`), `%LOCALAPPDATA%\MeshLayerStudio\`, and any model weights downloaded by this Software inside `%USERPROFILE%\.cache\huggingface`.

### 8. Children's Privacy
The Software is not directed to children under 13 (or under 16 where required by local laws such as the GDPR) and does not collect personal data from children. For restrictions on voluntary support by minors, see Section 11.4 of the Terms of Use.

### 9. Future Online Features
If future versions introduce features that transmit data off your device—such as user accounts, cloud storage, online inference, crash reporting, analytics, automatic update downloads, or integrated payments—the Provider will update this Privacy Policy in advance to disclose collected data categories, legal bases, retention periods, and third-party processors, and will provide prior notice and obtain your consent before enabling them.

### 10. Governing Law, Your Rights, and Policy Changes
1. **Taiwan PDPA:** This Privacy Policy is governed by Taiwan's Personal Data Protection Act. You retain all statutory rights to access, correct, restrict, and delete any personal data held by the Provider through Section 6 or email correspondence.
2. **EU/UK (GDPR / UK GDPR) and California (CCPA / CPRA):** The Provider **does not "sell" or "share" (for cross-context behavioral advertising)** any personal information. You have the right to request access, rectification, deletion, or withdrawal of consent for any limited contact records held.
3. **Submitting a Request:** Email `meshlayer.studio@gmail.com` at any time. In most cases, you can delete all local data directly under Section 7.
4. **Governing Language and Policy Changes:** The **Traditional Chinese version** shall prevail in the event of any discrepancy with translations. Upon updates, the Provider will revise the "Last Revised" date above and announce material changes in the Software or on the official website.