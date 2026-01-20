# UI for Spark Declarative Pipeline (SDP)

<p align="center">
  <img src="media/icon.png" alt="SDP Visualizer Icon" width="128" height="128">
</p>

<p align="center">
  <strong>Visualize Apache Spark Declarative Pipelines</strong><br>
  Tables, views, materialized views, and their dependencies from PySpark and SQL definitions.
</p>

<p align="center">
  <a href="https://marketplace.visualstudio.com/items?itemName=gszecsenyi.sdp-pipeline-visualizer">
    <img src="https://img.shields.io/visual-studio-marketplace/v/gszecsenyi.sdp-pipeline-visualizer?label=VS%20Marketplace&logo=visual-studio-code&logoColor=white&style=for-the-badge" alt="VS Marketplace">
  </a>
  <a href="https://marketplace.visualstudio.com/items?itemName=gszecsenyi.sdp-pipeline-visualizer">
    <img src="https://img.shields.io/visual-studio-marketplace/i/gszecsenyi.sdp-pipeline-visualizer?logo=visual-studio-code&logoColor=white&style=for-the-badge" alt="Installs">
  </a>
</p>

<p align="center">
  <a href="https://marketplace.visualstudio.com/items?itemName=gszecsenyi.sdp-pipeline-visualizer">🌐 View on Marketplace</a>
  &nbsp;•&nbsp;
  <a href="vscode:extension/gszecsenyi.sdp-pipeline-visualizer">⚡ Install in VS Code</a>
</p>

---

![Screenshot](media/screenshot_2.png)

## Features

- 📊 **Visualize pipeline DAGs** from YAML, Python, and SQL files
- 🔗 **Click nodes** to open source code directly in editor
- 👁️ **Preview code snippets** with syntax highlighting in sidebar
- 🔄 **Live updates** on file save

## Installation

### From VS Code Marketplace

1. Search for "**UI for Spark Declarative Pipeline**" in the Extensions view
2. Click **Install**

Or install directly: [Install Extension](vscode:extension/gszecsenyi.sdp-pipeline-visualizer)

### From VSIX

1. Download the latest `.vsix` file from the releases
2. In VS Code, run `Extensions: Install from VSIX...` and select the file

## Usage

1. Open a workspace containing a `pipeline.yml`, Python, or SQL pipeline file
2. Click the **SDP Pipeline Visualizer** icon in the Activity Bar
3. Select a pipeline from the automatically listed files in the sidebar
4. View the pipeline DAG and entity details in the sidebar and webview

## Developer

Developed by **Gergely Szécsényi**

## License

BSD 2-Clause License — see [LICENSE](LICENSE) for details.
