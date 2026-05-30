# A Weekend with Friends

A single-page, scroll-driven photo-story site for a 4-day weekend, built in the
style of an elegant brand "history" page: full-bleed hero, alternating photo/text
sections, gentle fade-in-on-scroll animations, warm minimal palette, and a click-to-zoom lightbox.

Everything lives in **`index.html`** (HTML + CSS + JS in one file). No build step — just open it.

## Adding your photos

1. Drop image files into **`weekend/photos/`** (e.g. `day1-1.jpg`, `hero.jpg`).
2. For each photo slot in `index.html`, replace the placeholder figure:

   ```html
   <figure class="ph reveal" data-label="Day 1 · Photo 1"></figure>
   ```

   with a real image:

   ```html
   <figure class="reveal">
     <img src="photos/day1-1.jpg" alt="">
     <figcaption>Optional caption shown on hover</figcaption>
   </figure>
   ```

   (Remove the `ph` class and the `data-label` — those just style the placeholder tile.)

3. **Hero photo:** on the `<section class="hero">` tag, add the class `has-photo`
   and set the image, e.g.:

   ```html
   <section class="hero has-photo" id="top" style="--hero-img:url('photos/hero.jpg')">
   ```

> Or just send me the pictures and tell me roughly which day each belongs to —
> I'll wire them in, set captions, and adjust the layout to the number of photos.

## Editing text

- Title, dates, and intro: top of `index.html` (hero + intro sections).
- Each day has a heading, date/place line, a short narrative paragraph, and captions —
  all clearly marked with placeholder copy to replace.
- Colours and fonts: edit the CSS variables in the `:root` block at the top of the file.

## Layout helpers available

- `.full` — full-bleed banner image
- `.grid.g-2` / `.grid.g-3` — 2- or 3-up photo grids
- `.split` / `.split.flip` — image beside a text block (flip swaps sides)
