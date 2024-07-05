This is a flameshot watermark plugin

**Please note: This is an experimental feature in an Alpha version, so there is uncertainty and instability.**

The plugin is written in C++. You need to compile this plugin using the same Qt framework as the flameshot compiled version.

The plugin requires a meta information configuration file. The configuration file is in `plugin.yaml.example`. Copy it to the plugin directory and rename it to `plugin.yaml`.

Open this configuration file, which contains four plugin configurations for the plugin to work properly, similar to:

```
plugin:
  name: "Watermark"
  type: "qt"
  file: "libWatermark.so"
  config:
    Watermark: "WM/Watemark.png"
    Bottom: "WM/Bottom.png"
    PrintBG: "WM/PrintBG.png"
    ColorBG: "#ffffff"
    PrintBG.Frame.Width: 3344
```

- Watermark: Watermark Image
- Bottom: This is a logo or other image added to the bottom of the image.
- PrintBG: This plugin supports print templates, which are framed images for printing
- ColorBG: Background color when saving images
- PrintBG.Frame.Width: Fill in the frame width of the frame image for printing that can accommodate the image content
