# Boost Mobile – Device Upgrade Offer Lookup

Interactive tool: the user picks an offer color, then a rate plan, and sees the device offers for that combination.

## Files
```
index.html                 ← the tool (all offer data lives at the top of the <script>)
fonts/                     ← Druk Super Italic, Druk Text Wide Heavy, Neue Haas Grotesk Text 55/75
assets/boost-logo-white.png
```

## Host on GitHub Pages
1. Create a repo and upload everything in this folder (keep the folder structure).
2. Repo **Settings → Pages** → Source: *Deploy from a branch* → `main` / root → Save.
3. Your URL will be `https://<username>.github.io/<repo>/`.

> ⚠️ Brand fonts are licensed (Commercial Type license 2405-WKJMKI, Neue Haas Grotesk). Use a **private/internal** repo or confirm your license allows web hosting. If the repo must be public and that isn't allowed, delete the `fonts/` folder — the tool falls back to system fonts.

## Embed in the LMS
```html
<iframe src="https://<username>.github.io/<repo>/" width="100%" height="760"
        style="border:0;max-width:960px" title="Device Upgrade Offer Lookup"></iframe>
```
Optional auto-height (if your LMS allows scripts):
```html
<script>
window.addEventListener("message", e => {
  if (e.data && e.data.type === "boost-offer-tool-height")
    document.querySelector('iframe[title="Device Upgrade Offer Lookup"]').style.height = e.data.height + "px";
});
</script>
```

## Updating offers
Edit `DEVICES`, `PLANS`, and `OFFERS` at the top of the script in `index.html`, and update the "Offers valid" dates in the header.
