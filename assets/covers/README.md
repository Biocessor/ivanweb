# Covers — convenzione di nomenclatura

Tutte le copertine vivono qui: `assets/covers/`. Una sola cartella, nessun
percorso annidato per cliente. I nomi dei file corrispondono allo slug del
progetto in `window.CONTENT.projects` (campo `media.cover`).

| progetto                          | file atteso                  | stato     |
|-----------------------------------|------------------------------|-----------|
| Epidemie · Fondazione Cini        | cini-01.jpg + cini-02.jpg + cini-03.jpg | ✓ presenti (carosello) |
| Memorie di un Museo · Gorizia     | gorizia.jpg                  | da inserire |
| Marco Polo · Scuola Visconti      | marco-polo.jpg               | da inserire |
| Museo Fermi · Viminale            | museo-fermi.jpg              | da inserire |
| Villa Selvatico                   | villa-selvatico.jpg          | da inserire |
| Aeterna Mente · Palazzo Maffei    | palazzo-maffei.jpg           | da inserire |
| Existence · Animastudio           | existence.jpg                | da inserire |
| Mathame · Generative Visuals      | mathame.jpg                  | da inserire |
| NEO — The Prophecy                | neo.jpg                      | da inserire |

## Specifiche tecniche

- Formato: **jpg** o **webp** (preferito webp per peso/qualità)
- Risoluzione: 1600×1000 px circa (16:10) — il modale ritaglia in `cover`
- Peso target: < 400 kB per copertina
- Spazio colore: sRGB
- Niente logo né testo sovraimpresso (li mette il sito)

## Aggiungere un carosello a un altro progetto

In `window.CONTENT.projects[i].media`:

```js
media: {
  type: "carousel",
  images: [
    "assets/covers/<slug>-01.jpg",
    "assets/covers/<slug>-02.jpg",
    "assets/covers/<slug>-03.jpg"
  ],
  alt: { it: "...", en: "..." }
}
```

## Video

I video vivono in `assets/media/<slug>.mp4`. Il `media.cover` viene usato come
poster del video — finché non si carica la prima frame, e come fallback se
il `<video>` fallisce. Quindi è utile averlo anche per le installazioni con video.
