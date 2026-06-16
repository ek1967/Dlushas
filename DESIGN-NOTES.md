# D'Lusha's Website — Design Notes

A first working prototype lives in **`index.html`** — open it in any browser.
It's a single, self-contained file (no build step, no dependencies) so it's
easy to preview, host anywhere, and hand to a developer later. Everything is
built directly on the brand book: the colour tokens, the Playfair / Cormorant /
DM Sans type system, the voice, and the bilingual strategy from Section 09.

---

## 1. Language: English or Hebrew or Both?

**Recommendation: Both — English-first as the default, with a one-tap Hebrew toggle.**
This is exactly what the brand book's Section 09 already argues for, and it's the
right call for a Ganei Tikva audience of bilingual Israelis.

The split we built into the site:

| Layer | Language | Why |
|---|---|---|
| Brand layer — logo, tagline, **menu item names** ("Berry Smooth"), section headlines | **English always** | Carries the premium, Le Cordon Bleu positioning. Never translate menu names — they're part of the identity. |
| Community layer — descriptions, hours, "Ask the Chef", community posts, nutrition | **Hebrew available** | This is where D'Lusha's is a *neighbour*, not a brand. Conversational, warm, real. |

How it works in the prototype:
- A small **EN / עב** toggle sits in the nav. It swaps every piece of copy and
  flips the whole page to right-to-left for Hebrew (`dir="rtl"`), and even
  switches to Hebrew-appropriate fonts so the Hebrew doesn't look like an
  afterthought.
- The choice is remembered between visits.
- **Default is English** (the brand layer), per the strategy — but a Hebrew
  speaker is one tap from feeling at home.

> Note: the Hebrew copy in the prototype is my draft and should be reviewed by
> Hila — the brand book is right that Hebrew must sound like *her*, never like
> Google Translate.

### The type system (final)

| Role | English | Hebrew |
|---|---|---|
| Big hero headline | Playfair Display (900) | **Suez One** — heavy heritage serif, extra warmth |
| Headlines / menu names | Playfair Display | **Frank Ruhl Libre** |
| Editorial / descriptions | Cormorant Garamond *(italic)* | Frank Ruhl Libre |
| Body / labels / buttons / UI | DM Sans | **Assistant** |

All are free Google Fonts. Menu item names stay in English (Playfair) in both
languages — they're part of the brand identity.

---

## 2. What we borrowed from each reference site

### 🥐 Tatte Bakery — *editorial warmth & food as the hero*
- **Full-bleed, photo-led hero** with the wordmark and a single confident line.
- **Generous whitespace** and a calm, premium rhythm between sections.
- **Menu presented editorially** — beautiful serif item names (Playfair),
  poetic descriptions (Cormorant), price as a quiet accent. Not a price list.
- Restrained palette so the *food photography* is the colour.

### 🦊 Foxy Loxy Cafe — *sense of place & community life*
- A **"Find the truck" block** with hours and a map — the cafe-as-a-place feeling,
  adapted for a mobile cart (today's hours auto-highlight).
- A **community / events strip** (sourdough club, spotlights) so the site feels
  alive and local, not static.
- An **email sign-up** to keep regulars in the loop.

### 🌱 Roots Brooklyn — *neighbourhood-first, values-forward*
- A **"Meet Hila" story section** that leads with the human and the craft —
  the brand's single biggest differentiator.
- A **community & causes** section ("Community Spotlight", "Ask the Chef")
  expressing values *through what she does*, exactly as the voice guide insists —
  not through mission-statement copy.

### Plus, essential for a food truck (and your explicit asks)
- **Google reviews** section with the 4.9★ badge and three highlight quotes,
  linking out to the full Google listing. *(Swap in real review text + count.)*
- A **values ribbon** (Organic · Vegan · Gluten Free · No Added Sugar) so the
  dietary promise is impossible to miss.

---

## 3. The imagined ordering system (next step)

The brand book notes there's no shop yet, so we **sketched the vision** as a
"Coming soon" section rather than a real checkout. It shows a phone mockup and a
simple three-step flow: *pick your order → choose a pickup time → pay & collect*,
with Bit/card payment and an SMS-when-ready. No app to download.

When you're ready to make it real, the lightest paths are:
- **Order-ahead / pickup:** a hosted ordering tool that already handles menus,
  time slots and payments (and integrates with a cart's reality of "ready in
  X minutes"). Embeds cleanly into this same page.
- **Simple shop** (beans, granola, merch, gift cards): a hosted store, embedded.

Both can drop straight into the existing `#order` section without redesigning
anything.

---

## 4. What to swap in before going live

Everything below is clearly placeholdered in the file:
- **Photography** — every coloured block marked as a photo note is a spot for
  Hila's real images (hero, each menu item, Hila's portrait, community shots).
  The brand book is strict: real food, real people, real place — no stock.
- **Real Google reviews** + the actual rating and review count.
- **Real hours, location, and a Google Maps embed** for the promenade.
- **Real links** — Instagram, WhatsApp, maps, the menu PDF.
- **Hebrew copy review** by Hila.

---

## 5. Running / hosting it

It's just one HTML file. Double-click to open locally, or host it free on
GitHub Pages, Netlify, or Vercel. No build step required.
