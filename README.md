# Quiz 9 — Final Project Pitch

---

## Part 1: Project Direction

### Reinterpreting an Existing Artwork

**Artwork:** *Portrait of Adele Bloch-Bauer I* (1907) → *The Kiss* (1907–08)
**Artist:** Gustav Klimt

Our project uses two works by Klimt as a pair — the first painting (*Adele*) is the starting state, and the second (*The Kiss*) is the hidden destination revealed through interaction.

![Portrait of Adele Bloch-Bauer I by Gustav Klimt 1907 gold leaf oil painting](images/adele.jpg)

*Gustav Klimt, Portrait of Adele Bloch-Bauer I, 1907 — Neue Galerie, New York*

---

### Vision & Inspiration

Our team will reinterpret Gustav Klimt's *Portrait of Adele Bloch-Bauer I* as an interactive mosaic experience that gradually reveals *The Kiss* hidden beneath. The viewer begins facing Adele — still, golden, composed — and through clicking, causes the surface to fragment into mosaic tiles that dissolve the portrait and uncover the embrace beneath. The inspiration for this transformation comes from **Refik Anadol's** data-driven material explorations (*Unsupervised*, MoMA 2022), where surfaces appear to melt and reform, and from **teamLab's** touch-reactive installations where viewers physically unlock imagery through interaction. Klimt's obsession with gold, texture, and decoration makes his work uniquely suited to a tile-based, layered reveal — every mosaic piece feels like a fragment of real gold leaf being turned over.

**Inspiration Source 1 — *The Kiss*, Gustav Klimt, 1907–08**

![The Kiss by Gustav Klimt 1907 gold oil painting couple embracing in golden robes](images/kiss.png)

*Gustav Klimt, The Kiss, 1907–08 — Österreichische Galerie Belvedere, Vienna*

**Inspiration Source 2 — Refik Anadol, *Unsupervised*, MoMA 2022**

![Refik Anadol Unsupervised MoMA 2022 large scale AI data sculpture flowing colourful organic shapes](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Refik_Anadol_Machine_Hallucinations_Space_Chapter_MoMA_2022.jpg/640px-Refik_Anadol_Machine_Hallucinations_Space_Chapter_MoMA_2022.jpg)

*Refik Anadol, Unsupervised, MoMA 2022 — Wikimedia Commons*

---

## Part 2: Mechanics

### Member 1 — Perlin Noise & Randomness: Organic Tile Texture

Rather than breaking the canvas into a uniform grid of identical squares, Member 1 will use Perlin noise to control the size of each mosaic tile across the canvas. Areas of high noise value will produce larger tiles; areas of low value will produce smaller, denser ones — giving the mosaic a breathing, irregular quality that echoes Klimt's original handmade gold-leaf application. On top of this, `randomSeed` will introduce subtle colour variation within each tile: even tiles sampling the same gold region of the source painting will differ slightly in hue and saturation, simulating the way real gold leaf catches light differently across its surface. Together, these two techniques replace a mechanical grid with something that feels handcrafted and alive.

---

### Member 2 — Audio: Music-Driven Flip Rhythm

Member 2 will load a background music track — classical or ambient, chosen to match Klimt's ceremonial tone — and use FFT analysis to read the frequency content of the audio in real time. Low-frequency energy (bass) will control the timing of large tile flips, triggering them on heavy beats. High-frequency energy will cause small tiles to flicker and shimmer, resembling gold leaf trembling in light. During loud passages the mosaic will spread faster; during quiet passages it will slow almost to a halt, making the entire transition breathe in sync with the music's emotional arc. This creates a direct connection between the soundtrack and the visual transformation.

---

### Member 3 — Time-based: Countdown & Animated Reveal

After the user's first click, Member 3 will start a 30-second countdown timer. If the user stops interacting, already-mosaiced tiles will continue to spread outward automatically at a slow rate. When the countdown reaches zero, any remaining un-flipped tiles will complete in a rapid chain reaction — a cascade that sweeps across the canvas and delivers the final reveal of *The Kiss*. The transition to the completed second painting will use an easing curve (slow-in, fast-out) to give the finale a sense of ceremony and weight. This time structure means the piece always resolves, but rewards active viewers who accelerate it themselves.

---

### Member 4 — User Input: Ripple Mosaic

Member 4 gives the viewer direct control over the transformation. Each mouse click on the canvas triggers a ripple of mosaic tiles expanding outward from the click point — the tiles nearest the cursor flip first, followed by a wave of surrounding tiles, creating a circular pond-ripple spreading effect. Different regions of the painting respond in visually distinct ways: clicking on Adele's face produces fine, dense tiles; clicking the gold background produces larger, bolder ones. A hover preview effect means that as the cursor moves across the canvas, the tiles immediately beneath it become slightly pixelated, hinting to the viewer that this area can be clicked and inviting further exploration.

---

## Part 3: Putting It Together

All four mechanics operate on the same shared canvas — a grid of mosaic tiles that together form either *Adele* or *The Kiss* depending on how many have flipped. User Input determines where on the canvas tiles begin to turn; Time-based ensures the transformation always completes within a fixed window; Audio links the speed and rhythm of flipping to the music's energy; and Perlin Noise ensures no two tiles look identical, giving the whole surface a handcrafted warmth. Visually, everything is held together by Klimt's gold palette — the mosaic tiles, the shimmer, and the destination painting all share the same amber, ochre, and warm black tones.

---
