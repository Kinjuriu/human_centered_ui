# No vibe coding

**A field guide for building websites, dashboards and data stories with AI tools that still look and feel made by a person.**

AI coding tools let anyone build in an afternoon what used to take a designer and an engineer weeks. That power is wonderful, and it comes with a trap: the same tools push everyone toward the same defaults, so sites built with them start to look identical, and visitors have learned to spot it. This guide collects the tells, explains why they happen, and sets out the habits and rules we use to avoid them.

Most of the ideas come from YC's *Design Review* episode on avoiding vibe coded sites (6 March 2026), in which YC's Aaron Epstein and visiting partner Raphael Schaad, the founder and designer of Cron (now Notion Calendar), reviewed landing pages that YC companies had built with AI tools. The rest come from our own practice building data dashboards and journalistic data stories.

---

## Contents

1. [Why AI-built sites all look the same](#1-why-ai-built-sites-all-look-the-same)
2. [The one test that matters: would a human hand-code this?](#2-the-one-test-that-matters-would-a-human-hand-code-this)
3. [The tells: a catalogue](#3-the-tells-a-catalogue)
4. [Hover: rules of thumb](#4-hover-rules-of-thumb)
5. [Scrolling and motion](#5-scrolling-and-motion)
6. [Colour, contrast and brand](#6-colour-contrast-and-brand)
7. [Icons, emoji and images](#7-icons-emoji-and-images)
8. [Navigation and layout](#8-navigation-and-layout)
9. [Communicating value above the fold](#9-communicating-value-above-the-fold)
10. [Dashboards and data stories](#10-dashboards-and-data-stories)
11. [Working with AI without outsourcing your thinking](#11-working-with-ai-without-outsourcing-your-thinking)
12. [What to put in your prompts](#12-what-to-put-in-your-prompts)
13. [QA: the human pass](#13-qa-the-human-pass)
14. [Pre-ship checklist](#14-pre-ship-checklist)
15. [Credits](#15-credits)

---

## 1. Why AI-built sites all look the same

The episode started from a late-night tweet by Raphael about the "dumb hover effects" on startup landing pages, and a question: how did these effects get into language models, and why are they suddenly everywhere?

The mechanism they describe is simple:

- Language models learn from the web, and they learn most from the sites that get linked to a lot, which tend to be the good ones.
- When one well-made site sets a trend (a purple gradient, a scroll effect, a glowing card), that trend gets absorbed into the models.
- In the old world it took a long time for others to copy a trend, because copying it meant designing and coding it. Now the copy is one prompt away, so within a week every new startup site has it.

The effects themselves are often fine in isolation. A purple gradient can look modern and attractive on one site. The problem is ubiquity: once everyone has it, it stops meaning anything, it erases the originality that founders want for their brand, and it signals "an AI made this" to anyone who has seen a few of them. Raphael put it this way about the first site they reviewed: before language models he would have thought it looked very nice, and now it screams AI to him.

**The goal of this guide is originality and intent.** Every visual choice on the page should be one you made on purpose, for a reason you can say out loud.

---

## 2. The one test that matters: would a human hand-code this?

This is the most important idea in the whole episode, and it came up again and again. Many of the effects on AI-built sites only exist because they are now free to produce. Nobody sat in a planning meeting and said "we need a line that follows the reader down the page; let's start coding that from scratch". Effects like that were hard for a human to build, so before AI nobody would have thought to build them, and if someone had spent a week getting one working, they would have decided it was not worth it.

So before you keep any effect, flourish or interaction, ask:

> **If a person had to build this by hand, taking a day or a week of real effort, would they still choose to build it?**

If the honest answer is no, delete it. Cheap to make is a terrible reason to ship something; as Aaron said about a button that chased the cursor around the page, just because something is easy does not mean it is worth doing.

Follow-up questions that sharpen the test:

- **Does it help the visitor understand or act?** If it only makes the page feel busy, it is decoration.
- **Would anyone notice if it were gone?** If not, it was never doing a job.
- **After scrolling past it, can I remember the content?** On one site in the episode, an animated line drew so much attention that Aaron could not recall anything from the sections it ran through. An effect that makes the content forgettable is actively harmful.
- **How would a careful human designer solve this?** Usually with less: a clear heading, a good image, standard controls, enough contrast.

Treat AI the other way round: use it to build the things that *are* worth a week of hand-coding (an interactive map, a well-made chart, a genuinely useful tool) at a fraction of the cost.

---

## 3. The tells: a catalogue

Every pattern below was either called out in the episode or is on our own banned list. The "do instead" column is what a careful human would do.

| Pattern | Why it reads as vibe coded | Do instead |
|---|---|---|
| Purple or purple-to-pink gradients | The single most common AI default; now signals "AI made this" | Choose your palette first, from your brand; use colour with intent |
| Pinkish-purple accent colour on every button | Same as above; every startup ends up with it | One accent colour that belongs to you and complements your logo |
| A line or path that follows you as you scroll | Hard to hand-code, so nobody did it before AI; it steals attention from the content | Nothing; let the content carry the page |
| Sections that fade in and fade out as you scroll | Ubiquitous AI default; delays content; feels sluggish | Content is simply there when you arrive |
| Scroll-jacking (the page controls your scroll speed or snapping) | Breaks the browser's native behaviour; disorienting | Native scrolling, always |
| Hover effects that make things fade or disappear | No designer would choose it; it makes the clickable thing retreat | Make it slightly more active (see section 4) |
| A light or glow that follows the cursor around card edges | Costs nothing with AI, so it gets thrown in; a week of work would never justify it | Static, well-made cards, or no cards |
| A button that chases the cursor around the screen | Distracting, and hard to actually click | A fixed, clearly labelled button where people expect it |
| "Meteors" or particles shooting across the background | Adds no value to the product; pure decoration | A plain background |
| Two sticky headers visible at once while scrolling | A transition bug between a detached and a fixed header | One header that transitions smoothly, then QA it |
| Stock icon sets and emoji as UI | The easy path; a model has no visual identity of its own, so it reaches for standard icons; an immediate tell | Words, or custom marks drawn for your product |
| Light grey text on white, low contrast | Hard to read; looks stylish in a mockup and fails in use | Text that passes WCAG AA contrast |
| Blurry hero images or video posters | Looks careless; sometimes an AI artefact | High-resolution assets that match what they introduce |
| Non-standard navigation | Visitors cannot work out how to use the site | Standard navigation patterns |
| "Scroll down to see more" cues, bouncing chevrons | Filler that treats the visitor as lost | Design the first screen so people want to scroll |
| Glassmorphism, liquid glass, blurred blobs, radial orbs | Trend defaults | Flat, honest surfaces |
| Rows of three feature cards; bento grids | The default landing-page skeleton | A layout shaped by your actual content |
| Black-and-purple palettes, sparkle "AI" icons, animated arrows | Trend defaults | See above |

None of these is forbidden by a law of design. They are banned *here* because they have become defaults, and defaults are what make a site look like every other site.

---

## 4. Hover: rules of thumb

Hover was the starting point of the whole conversation, so it gets its own section.

1. **The browser already gives you a hover effect for free.** The cursor turns into a hand over anything clickable, even with no CSS at all. That already says "you can click this".
2. **If you add an effect, make the element more inviting, never less.** A shade lighter or more saturated, a slightly stronger border, a small glow. Raphael's line: make it pop a little, and don't make it go away. The aim is to make things clickable; he recalled Steve Jobs wanting the Aqua interface to look "lickable".
3. **Stick to standard behaviour.** Visitors already know how buttons and links behave; surprises cost attention.
4. **Do not hide critical information or functionality behind hover.** Hover is fine for making an interface feel alive, and it is increasingly misused to reveal things people need. A tool should show what it can do; making users hunt around with the cursor to discover features is an anti-pattern. Raphael's framing: a computer should be a tool, a "bicycle for the mind", and a screen that hides its tools to look clean is a worse tool.
5. **Remember there is no hover on phones.** Long press, the closest equivalent, never caught on because nobody can discover it. Anything only reachable by hover is unreachable on mobile.

**For dashboards and maps** this means: hover may show a tooltip as a convenience, and the same information must also be reachable by tap, click or keyboard, and the most important numbers must be visible on the page without any interaction at all.

---

## 5. Scrolling and motion

- **Native scrolling only.** No scroll-jacking, no smooth-scroll libraries that change the speed, no snapping unless it is a carousel the user is clearly operating.
- **No reveal animations.** Sections do not fade, slide or scale in as they enter the viewport. Content is there when the reader arrives.
- **Nothing follows the user.** No elements that chase the cursor or track the scroll position for decoration.
- **Sticky headers must have one state at a time.** If a header detaches and becomes fixed, test the exact scroll position where it switches.
- **Motion has to carry information.** Acceptable motion shows that something changed: data updating when a filter changes, a bar growing to its new value. Keep it short (150 to 250ms) and turn it off under `prefers-reduced-motion`.
- **No autoplay.** If an animation or a time series can "play", the user starts it, and it stops at the end.

**The good kind of scroll feedback: a reading progress indicator.** A thin bar showing how far through a long article you are answers a real reader question, "how far into the book have I read?", the same way a bookmark or the thickness of the remaining pages does in print. That is why it passes the test in section 2 when the line-that-follows-you fails it: one tells the reader something useful, and the other only moves. Keep a progress indicator thin, static in colour, at the top or side, and free of extra animation.

---

## 6. Colour, contrast and brand

- **Start from your palette and your brand,** then feed them to the AI tool. Do not start from whatever the tool produces and tweak it; you will end up where everyone else ended up. Aaron's advice in the wrap-up: you have to be intentional about ending up somewhere different.
- **Colours must work together.** A red logo with a purple accent colour, as on one reviewed site, is not a complementary pairing; it reads as two defaults colliding.
- **Use colour for meaning.** In data work, colour belongs to the data (party, category, change). Page chrome stays neutral.
- **Contrast is not optional.** Light, thin, low-contrast text was one of the first readability problems spotted in the episode. Body text should meet WCAG AA (4.5:1) at minimum.
- **Avoid the current default palettes:** purple gradients, black-and-purple, neon on dark, pastel blobs.

---

## 7. Icons, emoji and images

- **No stock icon sets and no emoji as interface elements.** A language model has no visual identity of its own, so it reaches for the same standard icons every time; to anyone who has seen a few AI sites, they are an instant tell. Use words, or draw a small set of custom marks that belong to your product.
- **Every asset must be high resolution.** A blurry hero image or video poster makes the whole site look careless.
- **A poster image must match its video.** One reviewed site showed a still that belonged to a different video from the one that played.
- **Show the real product.** A real screenshot, a playable demo or an actual chart beats an illustration. One reviewed site let visitors play a 3D game in the browser straight from the landing page, which was the strongest moment in that review.

---

## 8. Navigation and layout

- **Use standard navigation.** On one site the reviewers could not tell whether they were creating a game or modifying an existing one, because the navigation was unconventional.
- **Put the company name by the logo,** where people look for it, and keep it out of the headline where it competes with the value proposition.
- **One header.** It may become sticky; it must never appear twice.
- **Let your content shape the layout.** The three-card row and the bento grid are what you get when the layout comes first and the content is poured in afterwards.

---

## 9. Communicating value above the fold

A startup landing page is a **customer acquisition channel**, and Raphael was explicit about it: the landing page is not your product, and it is not a "cool thing on the web" either. There is room for experimental sites, but a landing page exists to convert visitors.

So the first screen, before any scrolling, must answer:

1. **What is it?**
2. **Who is it for?**
3. **To what end?** Why should that person care?
4. **A call to action.**

If those four are not above the fold, conversion suffers. Effects that compete with them for attention (moving lines, chasing buttons, meteors) work directly against the page's job.

**The equivalent for data stories and dashboards:** the headline states the finding in plain English, the subtitle defines the measure, and the most important number or chart is visible on the first screen.

---

## 10. Dashboards and data stories

Everything above applies to data work, plus these rules from our own practice:

- **One question per chart.** Its headline answers the question; its subtitle says exactly what is measured.
- **Every chart carries its source and a date.** Methodology is one click away.
- **Direct labels beat legends.** Put the label on the line, the bar or the state.
- **No decorative KPI tiles.** A row of big numbers with tiny sparklines is the dashboard version of the three-card row.
- **No pie or donut charts, no 3D, no dual axes.**
- **Hand-built SVG over chart-library defaults.** Library defaults are the chart world's purple gradient; newsrooms (AP, FT, NYT) draw their graphics deliberately, and that is why they read as journalism.
- **Squared geometry.** Hairline rules, corner radii of 0 to 2px, seats and units drawn as squares.
- **Tooltips are a convenience,** never the only way to get a number (see section 4).
- **The page works with JavaScript off** at its default state, then interaction enhances it.

> **To add:** Stephane's notes on what the reviewers said about dashboards in the episode.

---

## 11. Working with AI without outsourcing your thinking

Raphael's closing point: he would have loved to have these AI superpowers when he built his first website, and you are still responsible for not outsourcing your thinking to the model. Use the tools to get *your* ideas, designs and interactions onto the web.

In practice:

1. **Decide before you prompt.** Palette, typefaces, tone of voice, what the page must achieve, what the first screen says. Write them down.
2. **Give the tool references you chose,** such as screenshots of sites you admire and why, rather than letting it draw on the average of the web.
3. **Give it a banned list** (section 3) so the defaults are off the table from the start.
4. **Review every effect with the hand-coding test** (section 2).
5. **Spend the saved time on the hard, valuable parts** that used to be too expensive: a real interactive demo, a well-made map, a custom illustration, careful copy.

---

## 12. What to put in your prompts

A starting template for briefing an AI coding tool on any site or dashboard:

```text
Before writing any UI code, read DESIGN_RULES.md and look at every image in reference/.

Brand: [palette with hex values], [typefaces], [tone of voice].
Purpose of the page: [who it is for, what they should do or learn].
First screen must show: [what it is, who it is for, why it matters, the call to action
or the key finding].

Do not use: purple or decorative gradients; fade-in or slide-in on scroll; scroll-jacking;
hover effects that move, fade or hide elements; cursor-following effects; particles or
meteors; glassmorphism; stock icon sets or emoji; three-card rows or bento grids;
"scroll down" cues; low-contrast grey text.

For every effect or animation you add, explain in your report why a human designer would
have spent real time hand-coding it. If you cannot, remove it.

When you finish, take screenshots at 375px and 1440px and list anything you are unsure of.
```

---

## 13. QA: the human pass

Aaron's closing point: it is very easy to create something, and in a single episode they found quirks, bugs and confusing moments across several sites. You, the human, have to go through the site and confirm that every interaction works.

Walk through it as a first-time visitor, on a phone and on a laptop:

- Click every link and button; check every hover state, and do the same with taps on a phone.
- Scroll slowly through every transition point, especially sticky headers.
- Watch every video and check its poster image.
- Zoom into every image to check resolution.
- Use the whole page by keyboard only.
- Turn on reduced motion in your operating system and reload.
- Read every word aloud. Delete anything that sounds like a template.
- Ask someone who has never seen the product to tell you, after ten seconds, what it is and who it is for.

---

## 14. Pre-ship checklist

- [ ] Palette and typefaces were chosen before building, and the site uses only those
- [ ] Every effect passes the hand-coding test, with a one-line reason
- [ ] Nothing from the catalogue in section 3 remains
- [ ] Hover only makes clickable things more inviting; nothing disappears on hover
- [ ] Nothing important is reachable only by hover
- [ ] Native scrolling; no reveal animations; one header state at a time
- [ ] Body text meets WCAG AA contrast
- [ ] No stock icons or emoji in the interface
- [ ] All images and video posters are sharp and match their content
- [ ] The first screen says what it is, who it is for, why it matters, and what to do (or, for data, the key finding)
- [ ] Every chart has a title, subtitle, source and date
- [ ] Works at 360px, 768px, 1280px and 1600px
- [ ] Keyboard and reduced-motion checks pass
- [ ] A human has QA'd every page and every interaction

---

## 15. Credits

- YC *Design Review*, "how to avoid a site that feels vibe coded", with Aaron Epstein and visiting partner Raphael Schaad (founder and designer of Cron, now Notion Calendar), published 6 March 2026. Thanks to the YC companies whose sites were reviewed. This guide paraphrases the discussion; watch the episode for the full context.
- Newsroom graphics teams at AP, the Financial Times and The New York Times, whose election and data pages set the standard for the dashboard rules in section 10.

Compiled by Stephane. Contributions and corrections welcome.
