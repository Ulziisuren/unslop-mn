# Mongolian interfaces

Read this when the interface text is in Mongolian Cyrillic, before the audit and again before the copy and type passes. These rules add to the main passes, they do not replace them. Keep the interface in Mongolian, never translate it to English while unslopping.

## Signs of slop in Mongolian

Add these to the audit next to [signs.md](signs.md).

- Hype words, like `гайхалтай`, `хувьсгалт`, `дээд зэргийн`, `шилдэг`, `төгс`, `шинэлэг`, `ухаалаг`, `хязгааргүй`, `нэг товшилтоор` → what the thing actually does, with the product's own nouns
- `AI-д суурилсан` or `хиймэл оюун ухаантай` on everything → only where it explains what the AI produces
- Greeting headlines, like `Тавтай морил, Болд! 👋` or `Сайн байна уу! 😊` → the page or period as the title, like `2026 оны 10-р сар`
- Exclamation marks, like `Амжилттай хадгалагдлаа!` → `Хадгалагдсан`
- Pleading or shouting buttons, like `Одоо эхэлнэ үү!` or `ЭХЛЭХ` → `Эхлэх`
- Wordy placeholders, like `Юу ч хамаагүй хайгаарай...` → `Хайх`
- Uppercase tracked labels in Cyrillic, like `НАВИГАЦ` or `ЭНЭ САРЫН ОРЛОГО` → `Навигац`, `Энэ сарын орлого`
- English and Mongolian mixed in one interface, like `Dashboard` next to `Тайлан` → one language, keep English only for product names and real technical terms
- Latin transliteration of Mongolian, like `Hadgalah` → Cyrillic `Хадгалах`
- Machine translated phrasing that reads like English word order, like `Таны тохиргоонууд` → natural Mongolian, `Тохиргоо`
- Fake looking data, like `Бат Батбат` or `99,999,999₮` → plausible Mongolian names and amounts, like `Б.Мөнхзул` or `248,500₮`

## Copy

- Buttons and menu items use the verbal noun ending in -х, like `Хадгалах`, `Илгээх`, `Устгах`, `Нэмэх`. One form across the whole screen, never `Хадгалах` next to `Илгээнэ үү`.
- Address the user with polite `та` consistently, never mix it with `чи`.
- Status and result messages are short past forms, like `Хадгалсан`, `Илгээсэн`, `Алдаа гарлаа`.
- A change says what it compares to, like `өмнөх сараас +12%` or `өмнөх сараас 3-аар цөөн`.
- Names follow the Mongolian convention, the initial of the father's name then the given name, like `Б.Мөнхзул`. In tight spaces the given name alone is fine.
- Headlines, labels and buttons end without a period, same as the main rules.
- Quotation marks are one style across the screen, either `«...»` or `"..."`.

## Numbers, dates and money

- Pick one number format per screen. Thousands with a comma and decimals with a dot, like `48,210` and `3.5`, is the common choice.
- Tugrik goes after the number with no space, like `48,210₮`. Use `төг` only if the product already does. Never mix `₮` and `MNT` on one screen.
- Dates in one format per screen. Long form `2026 оны 10-р сарын 2`, short form `2026.10.02`. Month labels on charts `1-р сар` to `12-р сар`, or `1 сар` to `12 сар` when space is tight. Never English month names.
- Weekdays on charts and calendars start on Monday and use two-letter abbreviations in sentence case, `Да Мя Лх Пү Ба Бя Ня`. Full names are `Даваа`, `Мягмар`, `Лхагва`, `Пүрэв`, `Баасан`, `Бямба`, `Ням`, with `гараг` added in running text, like `Пүрэв гараг`. Never English day names.
- Times use 24 hours, like `14:30`.
- Numbers still use `tabular-nums`.

## Type

- The font must cover Cyrillic, including the Mongolian letters `Ө ө Ү ү`. Check the glyph coverage before choosing a family from [tokens.md](tokens.md), several of them have no Cyrillic at all. Missing letters fall back to another font and the line looks broken.
- Known to cover Mongolian Cyrillic: Inter, IBM Plex Sans, Noto Sans, Roboto, PT Sans for the interface, IBM Plex Mono and JetBrains Mono for figures and meta, Noto Serif and PT Serif for a display headline.
- Render a test string with every special letter, like `Өглөө үүрээр Үнэн Өнөр`, and look at it before you commit to a family.
- When loading from Google Fonts, request the `cyrillic` subset, like `&subset=cyrillic` or the `cyrillic` unicode range, otherwise only Latin is served.
- Sentence case applies to Cyrillic too. Capitalize only the first word and proper names.

## Layout

- Mongolian words are often longer than English ones. Give buttons, tabs and nav items room to grow instead of fixed widths, and check that the longest label fits on one line at the mobile size.
- Do not rely on `hyphens: auto` for Mongolian, browser support is poor. Shorten the copy instead.
- Set `lang="mn"` on the `html` element, so screen readers and the browser treat the text as Mongolian.
- Traditional Mongolian script is vertical and needs `writing-mode: vertical-lr`. It is out of scope for this skill unless the user asks for it.

## Checklist additions

- [ ] The font renders `Ө ө Ү ү` in its own glyphs, no fallback
- [ ] No English words left in the interface except product names and real technical terms
- [ ] Buttons share one verb form, polite `та` throughout
- [ ] Money, dates and numbers each in one Mongolian format
- [ ] `lang="mn"` is set

---

Mongolian adaptation built on unslop by Damir Sokolovsky ([@heydamir](https://x.com/heydamir)), CC BY 4.0. Keep this credit in copies and adaptations.
