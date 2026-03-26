# SOLID Review — Game District

A Unity Editor tool that scans your C# scripts for SOLID principle violations and generates AI-powered fixes.

## Installation via UPM (Unity Package Manager)

### Option A — Git URL (recommended)
1. Open Unity → **Window → Package Manager**
2. Click **+** (top left) → **Add package from git URL**
3. Paste your git URL and click **Add**

### Option B — Local folder
1. Open Unity → **Window → Package Manager**
2. Click **+** → **Add package from disk**
3. Navigate to the `solid-review` folder and select `package.json`

## Requirements
- Unity 2021.3 or later
- `com.unity.nuget.newtonsoft-json` 3.0.2 (auto-installed via UPM)

## Usage
1. Open via **Tools → SOLID Review**
2. (Optional) Select a specific folder to scan in Settings
3. Click **Start SOLID Review**
4. Browse violations in the sidebar
5. Click **Generate Fix** to get an AI-powered refactor (requires Claude API key)
6. Review the **Behavioral Contract Check** before applying
7. Click **⬇ File PDF** to export a detailed report for any file

## API Key
Get a Claude API key at [console.anthropic.com](https://console.anthropic.com).  
Enter it in the tool's home screen or Settings panel.  
The key is stored in `EditorPrefs` only — never committed to version control.

## Features
- Detects **SRP**, **OCP**, **LSP**, **ISP** violations (DIP excluded — casual games)
- Rates each principle **1–5** based on the SOLID Easy Rating Guide
- AI-generated fixes via Claude API
- **Behavioral Contract Check** — verifies public methods are preserved before applying
- **PDF export** — full project summary + per-file detailed reports
- Skips SDK files (Adjust, AppMetrica, MaxSdk, Firebase, etc.)
- Folder-scoped scanning

---
*ESTD. 2016 · STAY HUNGRY · STAY FOOLISH*
