# AURA ONE — Real-Time Product Configurator

Live demo: **https://aura-configurator.vercel.app**

A single-file Three.js product configurator built as a portfolio piece.

- **Model**: AI-generated (Meshy image-to-3D from a studio reference shot), then optimized
  18.9 MB → **351 KB** via glTF-Transform (Draco mesh compression + 1K WebP textures)
- **Rendering**: PBR + RoomEnvironment IBL, ACES tone mapping, soft shadows, DPR capped at 2
- **Configurator**: finish variants (tint + metalness/roughness overlays that preserve the
  PBR texture set), eased camera choreography, hotspots, X-ray view
- **Commerce mapping**: "Add to cart" prints the exact `/cart/add.js` line-item payload
  (SKU, option properties, restorable config URL) the way a Shopify theme section would send it
- **Performance**: 60 fps, 2–3 draw calls; live fps/draw-call meter ships in the corner

Everything lives in one annotated `index.html` — no build step. `aura.glb` is served via CDN.

— Marco C.
