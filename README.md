# Quiz 9

---

## Part 1: Project Direction

### Reinterpreting an Existing Artwork

**Artwork:** *Portrait of Adele Bloch-Bauer I* (1907) → *The Kiss* (1907–08)
**Artist:** Gustav Klimt

Our project uses two works by Klimt as a pair — the first painting (*Adele*) is the starting state, and the second (*The Kiss*) is the hidden destination revealed through interaction.

![Portrait of Adele Bloch-Bauer I by Gustav Klimt 1907 gold leaf oil painting](readmeImages/Adele_Bloch-Bauer_I.jpg)

*Gustav Klimt, Portrait of Adele Bloch-Bauer I, 1907 — Neue Galerie, New York*

![Portrait of Adele Bloch-Bauer I by Gustav Klimt 1907 gold leaf oil painting](readmeImages/The-Kiss.jpg)

*Gustav Klimt, The Kiss, 1907 — Neue Galerie, New York*

---

### Vision & Inspiration

Our team will reinterpret Gustav Klimt's *Portrait of Adele Bloch-Bauer I* as an interactive mosaic experience that gradually reveals *The Kiss* hidden beneath. The viewer begins facing Adele — still, golden, composed — and through clicking, causes the surface to fragment into mosaic tiles that dissolve the portrait and uncover the embrace beneath. The inspiration for this transformation comes from **Refik Anadol's** data-driven material explorations (*Unsupervised*, MoMA 2022), where surfaces appear to melt and reform, and from **teamLab's** touch-reactive installations where viewers physically unlock imagery through interaction. Klimt's obsession with gold, texture, and decoration makes his work uniquely suited to a tile-based, layered reveal — every mosaic piece feels like a fragment of real gold leaf being turned over.

**Inspiration Source 1 — *The Kiss*, Gustav Klimt, 1907–08**

![The Kiss by Gustav Klimt 1907 gold oil painting couple embracing in golden robes]()

*Gustav Klimt, The Kiss, 1907–08 — Österreichische Galerie Belvedere, Vienna*

**Inspiration Source 2 — Refik Anadol, *Unsupervised*, MoMA 2022**

![Refik Anadol Unsupervised MoMA 2022 large scale AI data sculpture flowing colourful organic shapes](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Refik_Anadol_Machine_Hallucinations_Space_Chapter_MoMA_2022.jpg/640px-Refik_Anadol_Machine_Hallucinations_Space_Chapter_MoMA_2022.jpg)

*Refik Anadol, Unsupervised, MoMA 2022 — Wikimedia Commons*

---

## Part 2: Mechanics

### Yuanxin Yu — Perlin Noise & Randomness: Organic Tile Texture

Rather than breaking the canvas into a uniform grid of identical squares, Member 1 will use Perlin noise to control the size of each mosaic tile across the canvas. Areas of high noise value will produce larger tiles; areas of low value will produce smaller, denser ones — giving the mosaic a breathing, irregular quality that echoes Klimt's original handmade gold-leaf application. On top of this, `randomSeed` will introduce subtle colour variation within each tile: even tiles sampling the same gold region of the source painting will differ slightly in hue and saturation, simulating the way real gold leaf catches light differently across its surface. Together, these two techniques replace a mechanical grid with something that feels handcrafted and alive.

---

### Carol Tao — Audio: Music-Driven Flip Rhythm

The audio mechanic uses FFT-based frequency analysis to drive the rhythm and behaviour of the mosaic tiles. We will use a public-domain classical track such as **Erik Satie’s Gymnopédie No.1**, whose soft dynamics and slow tempo complement Klimt’s ornamental aesthetic. Low-frequency energy triggers large-tile flips, mid-frequency ranges create shimmering pulses, and high-frequency peaks generate fine flickers resembling gold leaf catching light. Louder musical passages accelerate the spread of mosaic transformation, while quiet sections slow or pause the motion. The user does not directly control this mechanic; instead, the music becomes an invisible performer shaping the artwork’s emotional pacing. This mechanic reinforces our vision by giving the golden surface a breathing, ceremonial rhythm that echoes Klimt’s layered luminosity.

---

### Xiaorong Dang — Time-based: Countdown & Animated Reveal

After the user's first click, Member 3 will start a 30-second countdown timer. If the user stops interacting, already-mosaiced tiles will continue to spread outward automatically at a slow rate. When the countdown reaches zero, any remaining un-flipped tiles will complete in a rapid chain reaction — a cascade that sweeps across the canvas and delivers the final reveal of *The Kiss*. The transition to the completed second painting will use an easing curve (slow-in, fast-out) to give the finale a sense of ceremony and weight. This time structure means the piece always resolves, but rewards active viewers who accelerate it themselves.

---

### Liqi Lu — User Input: Ripple Mosaic

Member 4 gives the viewer direct control over the transformation. Each mouse click on the canvas triggers a ripple of mosaic tiles expanding outward from the click point — the tiles nearest the cursor flip first, followed by a wave of surrounding tiles, creating a circular pond-ripple spreading effect. Different regions of the painting respond in visually distinct ways: clicking on Adele's face produces fine, dense tiles; clicking the gold background produces larger, bolder ones. A hover preview effect means that as the cursor moves across the canvas, the tiles immediately beneath it become slightly pixelated, hinting to the viewer that this area can be clicked and inviting further exploration.

---

## Part 3: Putting It Together

All four mechanisms operate within the same painting. A grid of mosaic tiles, depending on the number of tiles flipped, eventually forms a pattern resembling Adele or a kiss. User input determines where the tiles begin to flip on the canvas; a time-based mechanism ensures the transformation always occurs within a fixed timeframe; an audio mechanism links the speed and rhythm of the flips to the energy of music; and Burmester noise ensures no two tiles look exactly alike, giving the entire image a warm, handcrafted feel. Visually, Klimt's gold palette perfectly blends all elements together—the mosaic tiles, the shimmering effects, and the final painting all share the same amber, ochre, and warm black tones.

---
