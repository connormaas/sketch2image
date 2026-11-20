# Sketch2Image

Draw a rough sketch and get back a realistic image. **Live:** [sketch2image.netlify.app](https://sketch2image.netlify.app)

> ☹️ This service has been shut down, so image generation no longer works on the live site.

## How It Works

1. **Sketch** on a canvas with brush color, size, eraser, undo, and clear.
2. **Steer** the result with optional keywords like a style or mood.
3. **Generate:** an image captioning model describes the sketch, the caption and keywords become a prompt, and RealVisXL (Stable Diffusion XL) renders the image.

## Stack

- **Frontend:** React and [react-canvas-draw](https://github.com/embiem/react-canvas-draw)
- **Backend:** Netlify Functions calling the models through RapidAPI, so keys never reach the browser
- **Hosting:** Netlify

## Run It

```bash
git clone https://github.com/connormaas/sketch2image.git
cd sketch2image
npm install
npx netlify dev
```

Set your RapidAPI key as `API_KEY` in a local `.env` or in Netlify's environment settings.
