# MADE BY MAYUR | Clear Frame

Browser-based 4K and 8K video upscaler with enhancement controls. Everything runs on the device. No video is uploaded.

## Files

```
clearframe-app/
├── index.html      # the app, including the Clear Frame logo
├── sw.js           # service worker: makes the app work offline
├── manifest.json   # lets the app install to the home screen
├── icon-192.png    # home-screen icon
├── icon-512.png    # home-screen icon
└── README.md
```

All files must be in the same folder. Upload all of them to the repository.

## Publish on GitHub Pages

1. Create a new **public** repository on GitHub, for example `clearframe-app`.
2. Upload every file above to the repository's main page and commit.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose branch `main` and folder `/ (root)`, then click **Save**.
5. After about a minute, the app is live at `https://<your-username>.github.io/clearframe-app/`.

To update the app, upload the changed files to the same place and commit. Pages redeploys automatically.

## Offline use

- **First visit must be online.** The first visit saves the app and the fonts to the phone or computer.
- After that, the app opens and exports with no internet connection.
- To use it like an app, tap **Add to Home Screen** (iPhone and Android) or **Install** (desktop Chrome and Edge).

## Using the app

1. Tap **Choose a video**.
2. Pick 4K or 8K, then adjust the settings:
   - **Enhance**: a preset (Natural, Restore old footage, Low light, Crisp, Film grain), or set the sliders yourself:
     - **Sharpen** brings back edges.
     - **Denoise** smooths grain and noise while keeping edges.
     - **Clarity** adds local contrast in the midtones.
     - **Film grain** adds an animated grain layer.
   - **Stabilize shake** and **Keep original audio**.
   - **Quality**: Standard, High (default) or Best. The app shows the approximate file size per minute.
   - **Colour**: brightness, contrast, saturation and warmth, with **Reset colour**. The left half of the preview shows the original.
3. Tap **Start upscale**. The clip plays at real-time speed, so a 10-minute clip takes 10 minutes. Keep the screen on. Settings lock during export.
4. Tap **Save file** when the export finishes.

**App colours** (at the bottom of the page): choose a theme or a custom accent colour. The choice is remembered on that device.

## How Clear Frame compares with AI enhancers

| Enhance option | Topaz Video AI (desktop, paid) | Clear Frame |
|---|---|---|
| Upscale to 4K / 8K | Yes, AI models per content type | Yes, GPU scaling with sharpening |
| Denoise | Yes, AI denoise for low light | Yes, edge-aware filter (not AI) |
| Sharpen and texture recovery | Yes, AI models | Sharpen and clarity filters |
| Film grain (add or remove) | Yes | Add only |
| Stabilisation | Yes, AI, with auto-crop or full-frame | Light stabilisation with a small crop |
| Colour grading | Yes | Brightness, contrast, saturation, warmth |
| Frame interpolation and slow motion | Yes | Not in this version |
| Motion deblur | Yes | Not in this version |
| De-interlacing | Yes | Not in this version |
| Rolling-shutter correction | Yes | Not in this version |
| SDR to HDR | Yes | Not in this version |
| Face enhancement | Yes (in Topaz Photo) | Not in this version |

AI enhancers can add detail that is not in the original footage. Clear Frame cannot. It improves what is already there, on the phone, with no upload.

## Known limits

- **8K depends on the device.** Many phones cannot encode 8K video. When that happens, the app says so and does not offer a file. Use 4K on those devices.
- Long clips use a lot of memory. Clips over 10 minutes may fail on phones.
- Denoise, clarity and film grain add processing work. Keep the enhancements light on 8K clips.
- Processing needs the browser to stay open and the screen on.
- **Clips with no sound track** (silent screen recordings, for example) may fail to record on some browsers. Clear Frame shows a message when this happens. If it does, try a clip that has sound.
