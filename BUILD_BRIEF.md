# Build brief for Codex

Read this with [README.md](README.md) and [PERSONALIZE.md](PERSONALIZE.md). This is a reusable brief for a new person’s website. Anna’s live site is an interaction and visual reference, not a source of default personal data.

## Start with the person

Ask the worksheet questions in small groups before implementation. Collect an exact destination, visible label, and icon choice for each circle. Offer alternatives to the suggested platforms. Confirm whether newsletters/newsstands, shops/collections, or business/location pages should be separate destinations. Never infer an email or profile from a name.

Present the resolved configuration and design direction for review. Ask only the follow-ups still needed. Missing links must stay inactive in the local preview and must be supplied or removed before launch. Do not use Anna’s links as placeholders.

## Choose the right starting point

`starter.html` is a single-file, buildless implementation with a CSS dial. It includes editable text, 4–9 configurable circles, a fixed center and finger stop, rotation, click-to-dial, contact links, a pause control, and responsive styles. It intentionally has blank destinations. It uses no external fonts, tracking, keys, or runtime libraries.

Copy it into the reader’s project as `index.html`. Edit the `SITE` object. Change the array length to add or remove circles within the supported range. Each item has:

```js
{
  label: 'My portfolio',
  url: '', // Replace with the exact public URL supplied by the person.
  initials: 'MP',
  color: '#526864',
  icon: '' // Optional local image path, e.g. assets/portfolio.svg.
}
```

Use a local preview server for review. There is no package installation or build step. To host the starter on Vercel as a static site, the deployable folder needs `index.html` and any assets you added. When importing that folder, use the static/Other configuration with no framework build command. Confirm the actual root/output settings in the current Vercel interface. Do not publish the questionnaire, private references, or local backup files with the site.

The starter is a functional base, **not the finished photographic artwork**. If the person wants Anna’s degree of realism, prepare the assets below and retain the tested interaction. Do not describe an approximate CSS illustration as an exact photographic match.

## Realistic rotary artwork

Use the reader’s supplied or approved reference. Match its silhouette, hole placement, center size, perspective, metal tone, reflections, highlights, edge thickness, and finger-stop shape. Preserve depth and material texture. Do not add unrelated decorative text or reinterpret a precise reference without asking.

Build separate aligned layers:

1. **Rotating outer plate:** the metal body, rims, and all empty finger holes. No baked-in numbers, letters, logos, or name. It rotates as one piece.
2. **Circle content:** icons placed in the actual openings, rotating with the plate. Use the same coordinates for visual icons and their clickable targets.
3. **Stationary center:** bezel, cream paper, name, and optional curved caption. Its outline must align exactly with the plate opening.
4. **Stationary finger stop:** a realistic arm with the reference’s reflections, contact shadow, and proper overlap. It stays attached to the stationary assembly.

The hole rims belong to the rotating plate. A fixed background must not retain duplicate rims: that creates “ghost edges” as it turns. Inspect both the resting dial and several intermediate angles. Mask the center tightly enough to hide old text without covering the openings or flattening the chrome bezel. Keep the finger stop out of the rotating plate so there is only one arm.

For an image-based treatment, prepare transparent layers with the same canvas dimensions and center coordinates. Use optimized local images with enough resolution for phone and desktop displays. Verify transparency around cutouts. Keep the approved assets before making a new visual version.

### Center lettering and curved type

Use the chosen name, exact capitalization, and approved line breaks. Leave room for the arch phrase and visually balance the name inside the paper, not just its mathematical box. Anna’s final personalized name is raster artwork; changing it requires replacing that artwork, not merely changing a CSS `font-family`.

For a new build, editable HTML/SVG text is useful when an appropriate licensed webfont is available. Use an SVG `textPath` for the arch, or a carefully prepared artwork layer when exact lettering is more important. If a font cannot be identified or licensed, explain the limitation and offer a preview with a clear substitute. Do not ship a demo-only font as a licensed production webfont.

## Interaction contract

- Automatic rotation winds clockwise toward the fixed stop, pauses briefly, then unwinds to rest. No destination opens automatically.
- A normal circle click selects that circle. Animate from the current angle until it reaches the stop, then navigate once to its exact URL.
- Clicking the matching text link triggers the same selection and destination.
- Keep automatic movement still while a mouse or keyboard user is interacting. On touch-down, hold the target under the finger until release or cancellation. Allow normal page scrolling.
- A new selection replaces an unfinished previous one; it must not open both links.
- Keep the center and arm stationary throughout.
- Respect modified clicks and native browser link behavior. Use real anchors with real URLs, not only JavaScript buttons.
- Default ordinary clicks to the same tab. If another tab is requested, account for popup blockers and test that behavior rather than calling delayed `window.open` and assuming it worked.
- A contact email may open an email application without leaving the page; return the dial smoothly afterward. Do not send any email automatically.
- Cancel stale pending navigation when returning to the page. Do not reopen a previous selection.
- Clamp animation elapsed time after backgrounding so the dial does not jump through a long gap. Stop advancing when the document is hidden.
- Provide a clearly named pause/resume button. Reduced-motion users start with automatic rotation off and navigate without a prolonged dialing animation. Preference changes should take effect while the page is open.

For geometry, compute each icon’s base angle from its center relative to the rotation origin. The required clockwise travel is:

```js
const turn = ((stopAngle - iconAngle - currentRotation) % 360 + 360) % 360;
```

Use the reference’s actual stop angle, not a guessed constant copied from another dial. If the number of circles changes, update the artwork and hit areas together. The CSS starter can redistribute its openings; a photograph cannot gain or lose holes just by changing an array.

## Personalization and accessibility

Keep one data source for both icon destinations and the link list. Insert user-provided labels as text, not raw HTML. Accept only intended URL schemes such as `https:`, `http:`, `mailto:`, and explicitly requested `tel:`. Reject script URLs. Validate public URLs and inspect their final destination; do not discard query parameters that identify a shelf, location, or signup page.

Use local, approved brand icons or images and provide an initials/symbol fallback. Give each link a meaningful accessible name. Treat duplicate decorative images and arrows as decorative. Ensure visible keyboard focus and adequate contrast over metal reflections. Keep readable text links even if an icon is unfamiliar or an image fails to load. Include the actual name in the document title and accessible heading.

On phones, scale the complete dial proportionally and use at least 44 × 44 CSS-pixel hit areas. Keep the link group centered while honoring the chosen text alignment. Keep long labels readable. Put the pause control where it cannot cover the last destination; in-flow placement beneath the link list works well. Avoid horizontal overflow and hover-only instructions.

## Review before deployment

Do the checks that matter and report their limits honestly:

- Render at 320, 390, and 430 pixels wide and a desktop width. Inspect the center, arch, icons, arm, text list, and pause control.
- Verify no horizontal overflow and that all links remain reachable by scrolling.
- Confirm every circle and its text row share the exact intended URL. Test each destination, including query strings and contact links.
- Observe the automatic wind, stop, return, and multiple selected-circle angles. Look for duplicate hole edges, a second arm, or slipping masks.
- Check a selection during rotation, rapid selection changes, pausing, keyboard focus/Enter, modified clicks, and returning from another page.
- Test reduced motion. Check touch behavior where the available tooling permits; distinguish simulated viewport testing from testing on a physical phone.
- Check that assets load, the page has no relevant console errors, and unfinished placeholders are removed.
- Ask the owner to try the actual public page on their phone after publishing.

Keep the approved preview saved before experimenting. Do not replace someone’s approved black/chrome version just to try an alternative.

## Publish only the approved website

Wait until the person requests publication. Confirm the intended account, project, and any existing site before deploying. Do not overwrite an unrelated Vercel project. Guide them through sign-in if necessary; never ask for credentials in the public files or chat. Explain any cost before committing to it.

Deploy the static output and referenced assets only. If saving source on GitHub is requested, confirm its account, repository name, and visibility and save a concise editing guide with it. Do not upload unrelated workspace contents, credentials, private images, or backups.

After publishing, verify the **public** URL independently of the local preview. Check the root route, fonts/images, exact links, rotation, and mobile layout. Report the public website and repository URLs separately, plus any real limits on testing or deployment.

Current setup references: [Codex quickstart](https://learn.chatgpt.com/docs/quickstart), [Codex app](https://learn.chatgpt.com/docs/app), [Vercel deployments](https://vercel.com/docs/deployments).
