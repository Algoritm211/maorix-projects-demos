Add a new demo project to the Maorix portfolio.

## Steps

1. **Determine inputs** — if the user didn't provide them, ask:
   - `slug` — folder name (lowercase, hyphens, e.g. `my-feature`)
   - `title` — display name shown on the card
   - `description` — one sentence describing the demo
   - `tag` — category label (e.g. Design, Fintech, Security, AI, Product)
   - Whether they have an existing `index.html` to place, or need a blank placeholder

2. **Create the folder** — `<slug>/index.html`
   - If the user has their own file: remind them to copy it to `./<slug>/index.html`
   - If they need a placeholder: create a minimal branded HTML file that says "Coming soon" and links back to `../`

3. **Add a card to `index.html`** inside `.grid`, before the closing `</div>`:
   - Increment `card-index` from the last existing card
   - Use the exact card markup pattern from the file (see existing cards for reference)

4. **Commit and push**:
   ```
   git add <slug>/index.html index.html
   git commit -m "add: <slug>"
   git push
   ```

5. **Report** the live URL: `https://algoritm211.github.io/maorix-projects-demos/<slug>/`

## Card markup pattern

```html
<a class="card" href="./<slug>/">
  <div class="card-index">NN</div>
  <div class="card-title"><title></div>
  <div class="card-desc"><description></div>
  <div class="card-footer">
    <span class="card-tag"><tag></span>
    <span class="card-arrow">Open →</span>
  </div>
</a>
```
