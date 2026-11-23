# MeshLayer Studio Privacy Policy

> **Language Notice:** This document is an English translation of the Traditional Chinese Privacy Policy (`docs\PRIVACY_POLICY.md`). In the event of any discrepancy or conflict between the two versions, the Traditional Chinese version shall prevail.

**Version:** 2.3 | **Effective Date:** 2026-10-27 | **Last Revised:** 2026-11-23 | **Provider:** MeshLayer Studio | **Contact:** meshlayer.studio@gmail.com

---

### 4.1 Summary
- **Local-First; Zero Telemetry:** MeshLayer Studio (the "Software") processes all images, 3D models, and parameters locally on your computer. The Software contains no user account system, analytics, automatic crash reporting, or telemetry, and never uploads your images or models to the Provider's servers.
- **No Background Connections by Default:** All outbound network requests—including installing the AI runtime, downloading Gridfinity/OpenSCAD components, downloading the Bambu Studio color table, installing the Visual C++ runtime, optional component or program version checks, and opening external support links—occur solely after you **actively click a button or explicitly opt in / grant consent** (see Sections 4.4 and 4.6-1).

### 4.2 Local Data Processing and Storage
The Software reads and stores the following data solely on your local device. **None of this data is transmitted to the Provider:**

| Data Category | Local Storage Location | Purpose | Leaves Your Computer? |
| :--- | :--- | :--- | :--- |
| Input images, imported models, SVG patterns, and logos | Your chosen path; copied temporarily to `output\*_work\source.png` during processing | Generation, coloring, engraving, and inlay processing | No |
| Output files (STL / 3MF / OBJ / previews) | `output\` (inside the app folder) | Delivering finished output files | No |
| Filament library (`filaments.json`) & color overrides (`color_overrides.json`) | App folder | Remembering material and per-image color settings (indexed by image file name and file size) | No |
| User-imported fonts & external path config | `fonts\user\`, `openscad_path.txt` | Loading custom fonts and your specified OpenSCAD executable path | No |
| Preferences (`settings.json`) | `%LOCALAPPDATA%\MeshLayerStudio\` | Storing UI preferences, printer model, build plate size, and AI environment path | No |
| Customizer parameter files (`*_work\params.json` & saved presets) | Working folder or your chosen save path | Storing text, size, color parameters, and **local file paths** of chosen SVG/logo files (not the image contents); **review before sharing, as engraved text and local paths are recorded** | No |
| Font list cache (`mpl_cache\`) | `%LOCALAPPDATA%\MeshLayerStudio\mpl_cache\` | Accelerating system font scanning at startup; contains no personal files | No |
| AI runtime & model weight cache | `%LOCALAPPDATA%\MeshLayerStudio\ai\` (`.venv_ai`, `third_party`) and `%USERPROFILE%\.cache\huggingface` | Local AI inference (approx. 4–5 GB) | No (connects to third-party sources only during download) |
| Run log (LOG) | Displayed inside the application window | Local troubleshooting | No (shared only if you manually copy and email it for support) |

### 4.3 Personal Data Contained in User Images
Photos you process may contain faces, home interiors, license plates, or EXIF location metadata. The Software neither reads nor transmits EXIF metadata. To respect others' privacy and portrait rights, we recommend not processing photos of other individuals without their consent.

### 4.4 Optional Network Features and Third-Party Services
When you actively trigger or consent to the following optional features, the Software connects directly to the relevant third-party services, which handle standard connection data (such as IP addresses and HTTP request headers) under their own privacy policies. **The Software never sends your images or models to any third party:**
1. **Install AI Runtime:** Upon your click and consent, downloads packages and weights from PyPI, PyTorch (`download.pytorch.org`), GitHub (Hunyuan3D source code), and Hugging Face (model weights). If Git or Python is missing, or if you keep the optional "Also install OpenSCAD" box checked, those packages are installed via Microsoft's `winget` repository.
2. **Gridfinity Engine "Download and Set Up Automatically":** Upon your click and consent, connects only to `files.openscad.org` (OpenSCAD development snapshot) and GitHub (`kennetek/gridfinity-rebuilt-openscad`), unpacking solely into `%LOCALAPPDATA%\MeshLayerStudio\` without running a system installer or altering system settings. Any third-party `.scad` file you load is executed locally by your OpenSCAD installation and is never uploaded.
3. **Check for Component Updates (Off by Default):** Prompts you once after your first automatic component download and can be toggled in the Help menu or run manually at any time. When enabled, checks at most once per day at startup by reading only the snapshot list on `files.openscad.org` and release tags on GitHub (never connects if no automatic component is installed). Requests carry no personal data, and nothing is downloaded or installed automatically.
4. **Check for a New Program Version (Off by Default):** Connects only if you turn it on in the Help menu or manually click "Check for a new version of the program". When enabled, it checks at most once per day at startup by reading only the latest stable release info from `api.github.com` for `MeshLayerStudio-crypto/meshlayer-studio` (the request header includes the Software's name and version as User-Agent, with no personal data or local files). This feature is notification-only and **never downloads, installs, or replaces any file automatically**. The last check time and any skipped version are stored only in your local settings.
5. **Install Microsoft Visual C++ Redistributable:** Connects only if the runtime is missing and you consent; downloads the official installer from Microsoft (`aka.ms`), verifies Microsoft's digital signature, and installs it.
6. **Bambu Studio Color Table:** Reads your locally installed Bambu Studio files first (offline). If Bambu Studio is not installed and you select a Bambu printer model, only **with your consent** does it download a single color table file from Bambu Lab's public GitHub repository into your user folder (download-only, no upload).
7. **HTTPS Certificate Verification:** If antivirus software or a corporate proxy intercepts HTTPS traffic, the AI installation environment verifies certificates via the operating system certificate store (`truststore`) and sends no data to the Provider.

### 4.5 Data Retention and Deletion
Except for the narrow exception in Section 4.6-1 (where you directly contact us), all data resides solely on your computer. To remove the Software and all local data completely, delete the application folder (including `output\`), `%LOCALAPPDATA%\MeshLayerStudio\` (settings, cache, and AI runtime), and the model weights downloaded by this program inside `%USERPROFILE%\.cache\huggingface`.

### 4.6 Children's Privacy
The Software is not directed to children under 13 (or under 16 where required by applicable local laws such as the GDPR), and the Software itself does not collect personal data from children. For restrictions on voluntary support by minors, please refer to Section 3.11(4) of the Terms of Use.

### 4.6-1 Support Links and Payment Privacy Statement
1. **No Background Connections; No Collection:** The "Buy Me a Coffee…" feature in the Software's Help menu opens an external support web page in your operating system's default browser only when you **actively click a specific platform button**; prior to clicking, the Software makes no background connection for this feature. **The Software's desktop client does not embed third-party payment forms, load third-party tracking scripts, or collect, transmit, or store your payment information.**
2. **Independent Handling by External Platforms:** Once you leave the Software and visit a third-party support platform (such as Ko-fi or ECPay), any name, email address, billing address, and payment details you enter are collected and processed independently by that platform under its own privacy policy.
3. **Exception for Thank-You List and Direct Contact:** If you voluntarily email us to be included in a "Supporter Thank-You List" or for support inquiries, the Provider will receive your email address and chosen nickname. Such data is processed and retained solely for **maintaining the thank-you list and responding to your inquiry**. It is never used for marketing or other commercial purposes and is never sold or disclosed to unrelated third parties.
4. **Exercising Your Rights:** Under Article 3 of Taiwan's Personal Data Protection Act, you may email `meshlayer.studio@gmail.com` (also listed on the "About" page) at any time to request access to, copies of, correction of, cessation of collection/processing/use of, or deletion of any personal data retained above.

### 4.6-2 Local Region Detection (AI Compliance)
To comply with territorial restrictions under the upstream Hunyuan3D model license, the Software reads Windows' location, regional format, and system language settings **locally** at startup solely to determine whether to display AI features. **Nothing is uploaded or logged, and your location is never inferred from your IP address.**

### 4.7 Future Cloud or Online Features
If future versions introduce features that transmit data off your device—such as user accounts, cloud storage, online inference, crash reporting, usage analytics, automatic downloading or installation of updates, or integrated payments—the Provider will update this Privacy Policy in advance to disclose collected data categories, legal bases, retention periods, cross-border transfers, and third-party processors, and will provide prior notice and obtain your consent before enabling such features.

### 4.8 Governing Law and Your Privacy Rights
- **Taiwan Personal Data Protection Act (PDPA):** This Privacy Policy is governed by Taiwan's PDPA. You retain all statutory rights to access, correct, restrict, and delete any personal data held by the Provider through Section 4.6-1 or email correspondence.
- **EU/UK (GDPR / UK GDPR) and California (CCPA / CPRA) Residents:** The Provider **does not "sell" or "share" (for cross-context behavioral advertising)** any personal information. With respect to any limited contact or support records held by the Provider, you have the right to request access, rectification, deletion, or withdrawal of consent.
- **How to Submit a Request:** You may email `meshlayer.studio@gmail.com` at any time. Because the Software does not store your files or usage records on remote servers, in most cases you can delete all local data directly by following Section 4.5.

### 4.9 Policy Changes
When this Privacy Policy is updated, the Provider will revise the "Last Revised" date at the top of this document and announce material changes within the Software or on the official website.