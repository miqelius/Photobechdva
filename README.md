# ფერადი / Peradi — hand-painted atelier

Responsive Georgian, English and Russian concept showroom for hand-painted ceramics and T-shirts. Includes 20 original AI-generated product concepts, category filters, swipeable collections, accessible image dialogs, a custom-request text composer and a CSS animation inspired by Zidane's 2002 volley.

## Run
Serve `dist/` using any static HTTP server. There are no build dependencies.

## Publish
Vercel or another static host: output directory `dist`, no build command. Sites deployment configuration is in `.openai/hosting.json`.

## Demo boundaries
All catalog images are illustrative AI-generated concepts, not photographs of existing stock. Prices and delivery promises are deliberately omitted. The request form prepares copyable text locally and does not submit orders. Add the actual business contact before enabling order delivery. Language selection is stored in the visitor's browser. No API keys are used.

## Assets
`dist/assets/00.webp` through `19.webp`: individually generated artisan product photographs, optimized to WebP. Prompts describe each ceramic item or football/Georgia themed shirt on an ivory studio backdrop, with visible brush textures and natural light. Original asset generation used the built-in image generation tool.


## Python helper

This is a static website, not a Python web backend. `generate.py` uses only the Python standard library to write localized catalog data to `dist/data.js`. It resolves `dist/` relative to the script, so it can run from any working directory:

```bash
python3 generate.py
python3 -m http.server 8000 --directory dist
```

The generator overwrites `dist/data.js`; it does not create the HTML, styles, JavaScript application or images. No API keys, virtual environment or pip install is required for this helper. Generated catalog records remain illustrative concepts.
