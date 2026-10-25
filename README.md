# 현열 필요열량 계산기

상변화 없는 가열·냉각의 현열 변화량 계산

- Plan ID: E075
- App: https://nanalab.kr/eng-sensible-heat/
- Repository: https://github.com/NaNaCompany/eng-sensible-heat
- Formula: `Q = mc_pΔT`
- Output: 현열 변화 Q

## Model

m,c_p>0. c_p가 거의 일정한 온도 범위에서 정압 가열·냉각 또는 통상적인 고체·액체 근사에 쓴다. 냉각은 음수다. 잠열·열손실·가열 시간·히터 효율은 제외한다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `20000`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
