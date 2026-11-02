# unslop-mn

Монгол хэлтэй интерфейст зориулсан [unslop](https://github.com/heydamir/unslop)-ийн хувилбар. Эх skill-ийг Damir Sokolovsky ([@heydamir](https://x.com/heydamir)) бүтээсэн.

unslop бол Claude Code болон Codex-д зориулсан skill. AI-аар хийсэн, "AI-ын үнэр"-тэй хуудсыг (ягаан градиент, гэрэлтэлт, эможи, хашгирсан текст, жигд бус зай) дизайнер хийсэн мэт болгодог. Энэ хувилбар монгол текст, тоо, огноо, ₮, кирилл фонтын дүрмүүдийг нэмсэн.

## Эх хувилбараас юугаараа ялгаатай вэ

- [mongolian.md](skills/unslop/references/mongolian.md): монгол slop-ийн шинж, товчны үгийн хэлбэр, ₮ ба огнооны формат, гарагийн товчлол, Ө ба Ү үсэг дэмждэг фонт, `lang="mn"`
- [SKILL.md](skills/unslop/SKILL.md): аудит хийх алхам болон эцсийн шалгах жагсаалтаас mongolian.md руу холбосон
- [tokens.md](skills/unslop/references/tokens.md): кирилл дэмждэггүй фонтын тухай анхааруулга
- Монгол жишээ, өмнө ба дараа: [dashboard-mn.html](examples/dashboard-mn.html) → [dashboard-mn-unslopped.html](examples/dashboard-mn-unslopped.html)

## Суулгах

Claude Code-д бүх төсөлд ашиглах бол:

```bash
git clone https://github.com/Ulziisuren/unslop-mn
mkdir -p ~/.claude/skills && cp -r unslop-mn/skills/unslop ~/.claude/skills/
```

Зөвхөн нэг төсөлд ашиглах бол тухайн төслийн `.claude/skills/` хавтсанд хуулна.

Сайтын snapshot авах эсвэл story видео хийх бол Playwright болон ffmpeg хэрэгтэй:

```bash
npm install -D playwright
npx playwright install chromium
```

## Ашиглах

Claude Code-д `/unslop` гэж бичээд юу хийлгэхээ хэлнэ:

```
/unslop энэ dashboard-ыг цэвэрлэ
/unslop https://example.mn сайтын нүүр хэсгийг
```

Юу ч өөрчлөхөөс өмнө аудит болон чиглэлээ харуулаад таны зөвшөөрлийг авна.

## Лиценз

[CC BY 4.0](LICENSE). Энэ бол Damir Sokolovsky-гийн [unslop](https://github.com/heydamir/unslop)-ийг өөрчилсөн хувилбар. Хуулж, өөрчилж ашиглахдаа эх зохиогчийг дурдаж, эх репо руу холбоос тавина уу.

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
