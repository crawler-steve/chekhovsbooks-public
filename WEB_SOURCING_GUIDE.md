# Web Sourcing Guide — Taxonomy for Chekhov's Gun Discovery Prototype

This note records the web-sourced reference points used to refine the Phase 1.2 prototype.

## 1) Trope language
Working trope vocabulary was anchored to romance-reader discovery language and popularity signals.

Primary source used:
- Tropesmith romance trope demand list: https://tropesmith.com/romance-tropes/

How it was used:
- to favor reader-facing terms already common in romance discovery
- to keep trope labels short, recognizable, and searchable
- to support a curated trope picker in the prototype

Examples included in prototype:
- Found Family
- Slow Burn
- Forced Proximity
- Second Chance Romance
- Enemies to Lovers
- Friends to Lovers
- Fake Dating
- Grumpy/Sunshine
- Only One Bed
- Forbidden Romance
- Touch Her & Die
- Morally Grey MMC
- Villain Gets the Girl
- Why Choose
- Mafia
- Monster Romance
- Secret Society
- Stalker Romance
- Captor/Captive
- He Falls First
- Obsessive/Possessive
- Sports Romance
- Gothic Romance
- Serial Killer
- Omegaverse

## 2) Spice scale
Working heat language was informed by reader-facing explanations that distinguish open door, closed door, fade-to-black, frequency, and explicitness.

Primary sources used:
- Fractal Enigma — Romance Spice Levels Explained: https://fractalenigma.com/romance-spice-levels-explained/
- Fractal Enigma — Open-Door vs. Closed-Door Romance: https://fractalenigma.com/open-door-vs-closed-door-romance/
- HowSpicyIsThisBook.com: https://howspicyisthisbook.com/

Prototype implementation:
- 0 = No spice / kisses only
- 1 = Closed door
- 2 = Cracked door / limited detail
- 3 = Open door
- 4 = Explicit / high heat
- 5 = Very spicy / frequent explicit scenes

Design note:
There is no universal industry standard. The prototype spells out what each level means instead of relying on numbers alone.

## 3) Darkness scale
There is not a universal, consistent industry darkness scale comparable to spice scales.
For that reason, the prototype uses a store-defined scale so customers can separate darkness from heat.

Prototype implementation:
- 1 = Shadowed (lightly intense)
- 2 = Thorned (noticeably moody)
- 3 = Midnight (dark but mainstream-readable)
- 4 = Obsidian (very dark / intense)
- 5 = Abyssal (extreme material)

Interpretation note:
This scale is intentionally separate from spice. A book can be low-spice and still very dark, or very spicy without being especially dark.

## 4) Trigger warning wording / content note style
Trigger-warning wording was grounded in StoryGraph's reader-facing content-warning structure.

Primary sources used:
- The StoryGraph homepage: https://www.thestorygraph.com/
- StoryGraph roadmap note on disliked topics/content warnings: https://roadmap.thestorygraph.com/changelog/disliked-topics-and-content-types-in-recommendations
- Example StoryGraph content warning page: https://app.thestorygraph.com/books/793d1e6d-f8db-4ba5-9dd5-0e4668f39280/content_warnings

How it was used:
- to favor the phrasing Content Notes / Content Warnings rather than vague marketing language
- to separate themes from heat level
- to align warning wording with familiar reader language such as Sexual Assault, Dubious Consent, Consensual Non-Consent, Stalking, Domestic Abuse, Emotional Abuse, Graphic Violence, Gore, Pregnancy Loss, Self-Harm, Suicide / Suicidal Ideation, Animal Death, Gaslighting, and Racism / Bigotry

Future metadata recommendation:
If you enrich title-level data later, severity can optionally be stored in a StoryGraph-style structure such as:
- Minor
- Moderate
- Graphic

## 5) Romance glossary wording
Helpful community shorthand used in the glossary was supported by:
- Fractal Enigma — Romance Book Abbreviations Explained: https://fractalenigma.com/romance-book-abbreviations/
- Fractal Enigma — Why Choose vs. Reverse Harem vs. Polyamorous Romance: https://fractalenigma.com/why-choose-vs-reverse-harem-polyamorous-romance/

Examples reflected in the prototype glossary:
- FMC / MMC / MC
- HEA / HFN
- Why Choose
- Open Door / Closed Door / Fade to Black
- Grumpy/Sunshine
- Only One Bed
- Found Family
