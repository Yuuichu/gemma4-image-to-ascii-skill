---
name: image-to-ascii
description: "Convert an image or photo to ASCII art. Trigger when the user shares an image and wants to convert it to ASCII art, text art, or character art."
---

# Image to ASCII Art

## Instructions

When the user shares an image and asks for ASCII art:

1. Extract the full base64 data URL of the shared image. It must include the prefix, formatted as: `data:image/jpeg;base64,<base64data>` or `data:image/png;base64,<base64data>`. Do NOT omit the prefix.
2. Call the run_js tool with script name `index.html` and data:
   `{"imageData": "data:image/jpeg;base64,<full base64 data here>", "width": 80, "mode": "simple"}`
3. For block/pixel style, use mode `"block"`. For wider output, increase width up to 200.
4. Display the returned result directly to the user.

If no image is provided, ask the user to share one first.
