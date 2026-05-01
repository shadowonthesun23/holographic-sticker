# Holographic Sticker — Fork by Antonello

Fork personale di [LAWTED/holographic-sticker](https://github.com/LAWTED/holographic-sticker).

Una React component library per creare sticker olografici interattivi al passaggio del mouse.

## Installazione nel tuo progetto

```bash
npm install holographic-sticker
```

## Avviare l'editor locale

```bash
npm install
npm run dev
# → http://localhost:3000/sticker-editor
```

## Aggiungere le tue immagini

1. Metti le tue immagini in `/public/` (es. `/public/mia-immagine.png`)
2. Nell'editor, modifica il layer **Base Image** → campo `src` → `/mia-immagine.png`
3. Fai lo stesso per `maskUrl` in **Holographic Pattern** per far risplendere solo il soggetto

## Template disponibili

- **Lightning Sticker** — effetto fulmine con maschera e rifrazione
- **Lawted Sticker** — card personale con parallax e watermark
- **Antonello Sticker** — template base personalizzabile, pronto per le tue immagini

## Usare uno sticker nel tuo progetto Next.js

```tsx
// components/HoloSticker.tsx
"use client";
import HolographicSticker from "holographic-sticker";

export default function HoloSticker() {
  return (
    <HolographicSticker.Root>
      <HolographicSticker.Scene>
        <HolographicSticker.Card>
          <HolographicSticker.ImageLayer
            src="/tua-immagine.png"
            alt="Sticker"
            objectFit="contain"
            parallax
          />
          <HolographicSticker.Pattern
            maskUrl="/tua-immagine.png"
            maskSize="contain"
            textureUrl="https://assets.codepen.io/605876/figma-texture.png"
            textureSize="5cqi"
            mixBlendMode="hard-light"
            opacity={0.6}
          >
            <HolographicSticker.Refraction intensity={1.5} />
          </HolographicSticker.Pattern>
          <HolographicSticker.Spotlight intensity={0.8} />
          <HolographicSticker.Glare />
        </HolographicSticker.Card>
      </HolographicSticker.Scene>
    </HolographicSticker.Root>
  );
}
```

## Credits

Progetto originale di [@LAWTED](https://github.com/LAWTED), ispirato al design di [@jh3yy](https://x.com/jh3yy).

## Built With

- React 19
- Next.js 15
- TypeScript
- Tailwind CSS
