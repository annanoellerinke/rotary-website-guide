# Build your own rotary website

A personal link page that works like an old rotary phone: the dial moves, you choose a circle, and it turns to that destination before opening the link.

**[See Anna’s finished website →](https://anna-noelle-rinke.vercel.app/)**

This guide helps you make a version with **your name, your links, and your choice of icons**. You do not have to use the same platforms or the same seven categories. A booking page, podcast, portfolio, shop, newsletter, or something entirely different can have its own circle.

## Start here

1. **Open Codex and start a new task.** If you need help getting set up, use the [official Codex quickstart](https://learn.chatgpt.com/docs/quickstart).
2. **Copy the prompt below into that task.** Attach a reference image if you have a particular rotary, finish, or type style in mind.
3. **Answer the questions Codex asks.** Have the exact links you want people to open ready. You can say “I’m unsure” about an icon or a design choice.
4. **Review the working preview.** Check your name, the dial, every destination, and the phone layout. Ask for changes in ordinary language. Save the version you like before trying a new direction.
5. **Publish when you like it.** Use the publishing prompt farther down this page. Codex can prepare the files and guide you through the Vercel sign-in or connection required in your setup.

You do not need to manually create folders or upload code just to get started. Ask Codex to handle the project files. This GitHub repository is where the instructions and starter live; having your own GitHub account is useful if you also want to save your finished website there.

## Copy this into Codex

```text
I want to build my own animated rotary link website using this guide:
https://github.com/annanoellerinke/rotary-website-guide

Read README.md, PERSONALIZE.md, and BUILD_BRIEF.md before starting.
If you cannot access them, tell me so I can attach the files.

Use Anna’s finished site as a reference for the interaction:
https://anna-noelle-rinke.vercel.app/

Ask me questions BEFORE building. Start with my name, the number of circles,
and the destinations I want. For EVERY circle, collect the visible label,
my exact full URL or public contact address, and my icon preference.
Let me replace any suggested platform, add a different destination, or remove
a circle. Do not assume I want Anna’s categories, name, links, or email.

Ask about my rotary reference, material, background, center lettering,
curved text, colors, and the links below. If I’m unsure, offer a few clear
choices. Ask follow-up questions in small groups rather than one huge form.

Show me a table of the proposed circles, labels, exact destinations, and icons.
Flag anything missing. Confirm the design direction with me before building.
Do not invent URLs or substitute a platform’s homepage for my profile.

Create the project files for me and build a working local preview.
The included starter.html is a functional CSS demo, not Anna’s photographic
chrome artwork. If I want a realistic dial, follow the layered-artwork notes
in BUILD_BRIEF.md and use a reference I provide or approve.

Keep the center and finger stop still while the outer dial and its circles
move together. Automatically wind and return the rotary. On a normal click,
rotate the chosen circle to the stop before opening its actual destination.
Make the text links below work too. Include a pause control, keyboard access,
reduced-motion support, and mobile-friendly touch targets.

Show me the result on desktop and phone sizes. Verify the links, assets,
rotation, and navigation. Tell me what was actually tested.
Save approved versions before major visual changes.
Ask before installing software, incurring costs, or publishing the website.
```

## What should go in the circles?

Anything with a destination you want to share. These are suggestions, not a required list:

| What you want people to do | Possible destination | Icon ideas |
| --- | --- | --- |
| Follow you | Instagram, TikTok, LinkedIn, YouTube, Pinterest | Platform logo |
| Read your work | Substack, a digital newsstand, blog, archive | Publication logo, newspaper, open book |
| Learn about your business | Your website or a specific service page | Your logo or initials |
| Shop your picks | ShopMy, LTK, a storefront, a collection | Platform logo, shopping bag |
| Book something | Appointment page, studio, calendar, consultation | Calendar, key, small building |
| Listen | Podcast homepage, Spotify, Apple Podcasts | Microphone or show artwork |
| See your work | Portfolio, gallery, case studies, scrapbook | Camera, frame, collage |
| Get something useful | Public guide, download, resource library | Folder, paperclip, document |
| Join you | Community, membership, event, mailing-list signup | People, ticket, envelope |
| Contact you | Public email address or contact form | Envelope |

Two circles may use the same platform with different destinations. For example, your newsletter and your digital newsstand can be separate. A circle can also link to one specific collection instead of an entire shop.

**The important part is where it opens.** “My Instagram” is not a complete destination. Give Codex the full address from your profile. A private dashboard or a link that requires your login will not work for visitors.

Use the [personalization worksheet](PERSONALIZE.md) if you want to gather everything first.

## Make it look like you

Anna’s version uses a photographic chrome rotary, colored icons, a cream center, a stacked script name, curved “LET’S KEEP IN TOUCH” text, and a centered group of left-aligned links below it.

You can change any of those. Tell Codex which details to preserve and which to change. A reference photo is especially useful for metal color, reflections, depth, rim thickness, and the shape of the finger stop. “Make it vintage” leaves much more room for interpretation than an actual image.

For fonts, share the font name and a licensed webfont file if you have one. If you only have a screenshot, ask for a visual match and have Codex explain whether it is an approximation. The starter uses system fonts; it does not include commercial font files or Anna’s personalized artwork.

Useful feedback sounds like:

> Keep this version. Make a separate variation with a darker rotary, keeping the layout, motion, center lettering, and destinations the same.

> Move my name slightly higher inside the center circle. Keep the arch text and everything else where they are.

> Replace my fifth circle with my booking page. Use this exact URL: [paste URL]. Show me two icon options before changing the design.

## What is included here?

| File | What it does |
| --- | --- |
| [PERSONALIZE.md](PERSONALIZE.md) | Questions and a fill-in table for your name, links, icons, and visual choices |
| [BUILD_BRIEF.md](BUILD_BRIEF.md) | Implementation guidance for the motion, realistic artwork, accessibility, mobile checks, and publishing |
| [starter.html](starter.html) | A working, dependency-free demo with seven editable slots, automatic rotation, click-to-dial, and a link list |

**The starter is a simple CSS illustration.** It demonstrates the working interaction and configuration. It is not an exact copy of the photographed chrome dial on Anna’s live site. For that level of realism, the artwork needs its own reference, layered assets, and visual review.

Ask Codex to download the starter into your own project and open a local preview. It is a single HTML file; there is no package installation or build step. The `SITE` block near the bottom holds the name, curved phrase, ordered links, initials, icon images, and colors. The default destinations are intentionally empty and stay inactive until you provide yours. The starter supports four through nine circles; seven is the starting point.

## When you are ready to publish

First open every destination from the preview. Resolve every missing link or remove that circle. Then paste:

```text
I approve this version. Prepare it for Vercel and check it before publishing.
Confirm the target account and project name so we do not overwrite another site.
Guide me through any sign-in or connection needed, and tell me if anything
would cost money before proceeding. Do not ask me to paste passwords or tokens
into the chat or the website files.

Check the exact personal links, assets, metadata, phone layout, touch behavior,
keyboard navigation, reduced motion, and pause control. Do not publish missing
destinations or someone else’s personal information.

Deploy the approved website to my Vercel account and give me the public URL.
Verify the public site after deployment, including at phone widths.
If you cannot deploy from this setup, explain the specific blocker and give me
the prepared site files and the shortest supported next step.
```

You will need access to a Vercel account to publish there. The exact sign-in and deployment route depends on the tools available in your Codex session. A custom domain is optional; it can be connected after the site works. Current hosting options are covered in [Vercel’s deployment documentation](https://vercel.com/docs/deployments).

If you also want the finished source saved in your GitHub account, add:

```text
Save the finished source and a short editing guide in my GitHub account too.
Confirm the repository name and whether it should be public or private.
Only include files needed for this website—no credentials, private references,
unrelated projects, or local backups. Give me the repository link when it is saved.
```

## Before you share the link

- Open the **public URL** on your own phone and in a private browser window.
- Tap every circle and every text link. Check the exact profile, page, shelf, or booking screen that opens.
- Confirm the rotary reaches the selected circle before navigation.
- Check that your name, arch text, finger stop, and holes still line up as it moves.
- Scroll to the last link and make sure the pause control does not cover it.
- Try pausing the animation and navigating with a keyboard.
- Ask Codex to verify reduced-motion behavior and report any device tests it could not perform.

Keep your project files after publishing. When you want to update something, return to the same project, give Codex the new exact link or design change, review the preview, and ask it to update the existing deployment.

---

Created by [Anna Noelle Rinke](https://anna-noelle-rinke.vercel.app/). This guide is intended to be adapted for your own site. Use your own permitted artwork, logos, and fonts; the original reference photos and personalized production assets are not included.
