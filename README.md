# unslop-mn

Монгол хэл дээрх UI-д зориулан өргөтгөсөн [unslop](https://github.com/heydamir/unslop) skill. Эх хувилбарыг Damir Sokolovsky ([@heydamir](https://x.com/heydamir)) бүтээсэн.

unslop нь Claude Code болон Codex-д зориулсан skill юм. AI ашиглан хийсэн, vibecoded UI-д түгээмэл тохиолддог AI slop буюу gradient, glow, emoji, анхаарал татах гэж хэт оролдсон текст (`!!`, ТОМ ҮСЭГ, "гайхалтай", "хувьсгалт" гэх мэт үгс), жигд бус spacing зэргийг илрүүлж, тухайн бүтээгдэхүүнд тохирсон design болгон засдаг. Энэ хувилбарт монгол текст, тоо, огноо, ₮ тэмдэгт болон Cyrillic font-той холбоотой дүрмүүдийг нэмсэн.

## Эх хувилбараас ялгарах зүйлс

- [mongolian.md](skills/unslop/references/mongolian.md): монгол UI дахь slop-ийн шинж тэмдэг, button-ий текстийн хэлбэр, ₮ болон огнооны формат, гарагийн товчлол, Ө, Ү үсэг дэмждэг font, `lang="mn"` тохиргоо
- [SKILL.md](skills/unslop/SKILL.md): Audit алхам болон Checklist-д mongolian.md-ийн холбоосыг нэмсэн
- [tokens.md](skills/unslop/references/tokens.md): Cyrillic дэмждэггүй font-ын талаарх анхааруулга
- Монгол жишээ (before / after): [dashboard-mn.html](examples/dashboard-mn.html) → [dashboard-mn-unslopped.html](examples/dashboard-mn-unslopped.html)

## Суулгах заавар

Claude Code-ийн бүх төсөлд (global) ашиглах бол:

```bash
git clone https://github.com/Ulziisuren/unslop-mn
mkdir -p ~/.claude/skills && cp -r unslop-mn/skills/unslop ~/.claude/skills/
```

Зөвхөн тодорхой нэг төсөлд ашиглах бол тухайн төслийн `.claude/skills/` фолдерт хуулна.

Live сайтын snapshot авах эсвэл story video үүсгэхэд Playwright болон ffmpeg шаардлагатай:

```bash
npm install -D playwright
npx playwright install chromium
```

## Хэрэглээ

Claude Code дээр `/unslop` командын араас хийлгэх ажлаа бичнэ:

```
/unslop энэ dashboard-ийг засварла
/unslop https://example.mn сайтын hero хэсгийг засварла
```

Skill нь өөрчлөлт хийхээс өмнө audit болон direction-оо танилцуулж, таны зөвшөөрлийг авна.

## License

[CC BY 4.0](LICENSE). Энэхүү repository нь Damir Sokolovsky-ийн [unslop](https://github.com/heydamir/unslop)-ийг өөрчилж боловсруулсан хувилбар юм. Хуулбарлах, өөрчлөх, түгээхдээ эх зохиогчийг дурдаж, эх repository-ийн холбоосыг хавсаргана уу.

---

## Original README (English)

Created by Damir Sokolovsky ([@heydamir](https://x.com/heydamir)), who started the [Unslopping series](https://x.com/heydamir/status/2115063463063998736) on X. This repository is a Mongolian adaptation; the original lives at [heydamir/unslop](https://github.com/heydamir/unslop).

![A vibecoded dashboard unslopping itself, frame by frame](skills/unslop/references/refs/story-dashboard-frames.webp)

unslop is a skill for Claude Code and Codex that turns vibecoded, AI-looking UI into a designed interface with its own character. It finds the slop first, the purple gradients, glows, emoji labels, shouty copy and uneven spacing, then sets a direction from your product and fixes the screen pass by pass like a designer doing a redline review. It works in whatever your screen is built with, like Next.js, React, Vue, Svelte, Tailwind or plain HTML and CSS, on dashboards, apps and landing pages, and even on a live site when all you have is a link.

### What it does

- **Audit.** Lists every sign of slop with where it lives.
- **Direction.** Character, world, the one or two moments that carry the color, and a signature detail, all taken from your product.
- **Passes.** Spacing, color, icons, copy, type, layout, details, visuals and motion, in that order.
- **Visuals.** Shows your product instead of a glossy blob. When a hero needs a scene or an object, it can generate one through an image service like fal, Replicate, OpenAI images or Higgsfield. If none is connected, it offers to connect one as an MCP server, and it shows the prompt and asks before every paid generation. Dashboards and apps rarely need one.
- **Story video.** A square video under 10 seconds of your screen unslopping itself, ready to post. It needs Playwright and ffmpeg.

### Hire the unslopper

Would rather have a designer do it? Damir unslops one key screen in 3 days, built in your stack, at [heydamir.design/unslop](https://heydamir.design/unslop).

### License

[CC BY 4.0](LICENSE). Use it, change it and share it, including commercially, as long as you credit Damir Sokolovsky ([@heydamir](https://x.com/heydamir)) and link back to [the original repository](https://github.com/heydamir/unslop).
