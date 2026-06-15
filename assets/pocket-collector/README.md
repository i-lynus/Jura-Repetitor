# Pocket Collector — Asset Library

Komplette SVG-Asset-Bibliothek für die **Pocket Collector** App.
Alle Assets: transparenter Hintergrund, einheitliche Designsprache
(dunkles Vintage/Fantasy-Pixel-Art mit Gold-Akzenten, `Courier New` Typo).

> **Hinweis:** Alle Kreaturen sind eigene, generische Designs
> (z.B. „Flammarion" Flammen-Drache) — keine markenrechtlich
> geschützten Figuren. So bleibt die App rechtlich unabhängig.

## Design-Token (für konsistente Erweiterung)

| Token | Hex |
|---|---|
| Gold hell | `#F5D060` |
| Gold | `#C8922A` |
| Gold dunkel | `#9A6810` / `#7A5010` |
| BG dunkel | `#1A1208` → `#0D0A04` |
| Header-Band | `#241808` |
| Grün | `#6DBF4A` / `#4A9B30` / `#2D6B1A` / `#A8E060` |
| Blau | `#7BBFEE` / `#3A5A88` |
| Scan-Grün | `#40E0A0` |
| Rot | `#E84040` / `#C83020` |
| Lila | `#C080FF` / `#8060D0` |
| Rahmen subtil | `#5A4030` |

## Inhalt

### Branding & Kern
- `logo-wordmark.svg` — Gold-Pixel-Wordmark
- `app-icon.svg` — 512px App-Icon
- `badge-sync-safe-local.svg` — Sync/Safe/Local Badge
- `nav-icons.svg` — Navigations-Icons (einzeln)
- `pixel-garden-scene.svg` — Garten-Illustration
- `rarity-badges.svg` — C/U/R/SR/UR Badges
- `ui-card-frame-gold.svg` — Karten-Rahmen Template
- `scan-lens-ui-frame.svg` — Scan-Interface

### Module
| Ordner | Inhalt |
|---|---|
| `currencies/` | Gold Coin, Gem, Ticket |
| `packs/` | Basis/Jungle/Premium Packs + Booster Box |
| `achievements/` | 5-Tier Badges, Quest-UI |
| `card-variants/` | Holo/FullArt/Gold/Rainbow/Sketch, Binder-Varianten |
| `garden-objects/` | Wege, Pflanzen, Bäume, Deko, Spezial-Objekte |
| `ui-elements/` | Buttons, Toggles, Bars, Tabs, **Bottom-Nav-Bar** |
| `profile/` | Sammler-Profil-Karte |
| `effects/` | Karten-Labels, **Interaktions-Icons**, **Status-Icons** |
| `shop/` | Shop-Kategorie-Icons + Preis-Tags |
| `battle/` | Duell/Kampf UI-Mockup |
| `loading/` | Loading-/Transition-Screen |
| `tutorial/` | Tutorial-Overlay + Hilfe-Icons |
| `accessories/` | Kartenhüllen, Toploader, Spielmatte |
| `detail-view/` | Codex/Detail-Ansicht (aufgeschlagenes Buch) |
| `sound/` | SFX-Icons + Musik-Stimmungs-Icons |
| `animations/` | 7 animierte SVGs (SMIL, loopen nativ) |

### Animationen (`animations/`)
| Datei | Effekt |
|---|---|
| `lantern-glow-pulse.svg` | Flammen-Flackern + Lichtpartikel |
| `coin-spin.svg` | Münz-3D-Drehung + `+1` Pop |
| `card-reveal.svg` | Karten-Flip → Holo → Vorderseite |
| `scan-sweep.svg` | Scan-Linie + Corner-Lock + Ergebnis |
| `garden-grow.svg` | Samen → Baum + Wiegen |
| `xp-progress-fill.svg` | XP-Balken + LEVEL UP Burst |
| `achievement-unlock.svg` | Schild-Drop + Strahlen + Konfetti |

## Verwendung
SVGs sind direkt in Web/React-Native/Flutter einbettbar. Für native
Apps bei Bedarf zu PNG/WebP rastern (z.B. mehrere `@1x/@2x/@3x` Größen).
Animierte SVGs funktionieren im Browser/WebView; für native Engines
ggf. als Lottie/Sprite-Sheet umsetzen — die Frame-Logik ist in den
SMIL-`values` dokumentiert.
