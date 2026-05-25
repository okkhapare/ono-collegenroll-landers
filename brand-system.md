# CollegEnroll Brand System

Reusable reference extracted from `CollegEnroll-index.html`, `CollegEnroll-index_files/home.css`, and the homepage PDF capture from May 21, 2026.

## Brand Personality

CollegEnroll uses a calm education-services palette: deep navy foundations, white content surfaces, pale blue-gray section bands, and bright orange action accents. The visual system relies on large editorial headings, rounded form controls, image-led cards, outlined SVG icons, and CTA arrows.

## Color System

### Primary Colors

| Token | Hex | Usage |
| --- | --- | --- |
| Brand Navy | `#1B3459` | Hero background overlays, footer background, dark category card, secondary CTA background, body text fallback |
| Ink Navy | `#081B37` | Main headings, sticky navigation text, mobile menu text, modal/disclosure text |
| Mobile Header Navy | `#193154` | Mobile header background |
| Near Black Navy | `#01112B` | Dropdown hover/active text |

### Secondary Colors

| Token | Hex | Usage |
| --- | --- | --- |
| White | `#FFFFFF` | Page background, cards, form controls, header when sticky |
| Pale Section Blue | `#F0F3F9` | Major section backgrounds, dropdown option hover background |
| Border Blue Gray | `#E2E7F0` | Card borders, form dividers, inactive icon accents |
| Input Border | `#E1EAF3` | Custom select borders |
| Soft Card Gray | `#F9F9F9` | Article/category card backgrounds |
| Light Surface | `#F7F7F7` | Program card border |
| Muted Text | `#96A2B3` | Dates, read-time metadata, copyright, footer disclosure |
| Body Gray Blue | `#495D7A` | Paragraph text in content cards and banner quote |
| Form Text | `#39495F` | Select/input values |

### Accent Colors

| Token | Hex | Usage |
| --- | --- | --- |
| CollegEnroll Orange | `#FF8600` | Primary CTAs, logo block, heading highlight spans, nav/link underline hover, active tabs, icon accents |
| CTA Hover Orange | `#FF9F34` | Primary orange button hover state |
| Warm Orange Variant | `#FF8637` | Form-card heading highlight |
| Pale Orange | `#FFF3E6` | Carousel arrow button background |
| Orange Border | `#FFAE54` | Carousel arrow border |
| Blue Hover | `#0B75D7` | Navy rounded CTA hover state |
| Focus Blue | `#4E69FF` | Open custom select border |

### Utility / Miscellaneous

`#000`, `#333`, `#999`, `#B3B3B3`, `#B7B7B7`, `#D2D2D2`, `#D8E1EC`, `#D9D9D9`, `#DDD`, `#E1E1E1`, `#EEE`, `#F0F0F0`, `#F2F4F7`, `#F8F8F8`, `#FB5858`, `#929EC9`, plus transparent black overlays `#00000014`, `#0000001A`, and `#00000033`.

## Typography

### Font Families

| Role | Family | Source / Weight |
| --- | --- | --- |
| Headings / display | `Author, Arial, Helvetica, sans-serif` | `Author-Semibold.woff`, weight `600` |
| Body / UI | `DMSans, -apple-system, BlinkMacSystemFont, Segoe UI, Helvetica, Arial, sans-serif` | `DMSans-Regular.woff`, weight `400`; `DMSans-Bold.woff`, weight `700` |
| Disclosure modal only | `PlayfairDisplay-Bold` / `PlayfairDisplay-Regular` | Used in disclosure overlay title and paragraphs |

Note: Some selectors spell the family as `DmSans`; use `DMSans` as the canonical token because that is the `@font-face` family name.

### Type Scale

| Element | Desktop | Mobile | Color |
| --- | --- | --- | --- |
| Hero H1 | `72px / 80px`, `Author 600` | `40px / 42px` | `#FFFFFF` |
| Section H2 | `60px / 68-80px`, `Author 600` | `36px / 38-42px` | `#081B37`, highlight span `#FF8600` |
| Category heading | `36px / 38px`, `Author 600` | `28px / 32px` | `#1B3459` or white on navy card |
| Hero body | `20px / 26px`, `DMSans 400` | `16px / 24px` | `#FFFFFF` |
| Section intro | `18px / 28px`, `DMSans 400` | `16px / 24px` | `#081B37` |
| Carousel card title | `28px / 32px`, `DMSans 700` | same unless constrained | `#FFFFFF`, span `#FF8600` |
| Article title | `20px / 26px`, `DMSans 700` | same | `#1B3459`; hover `#FF8600` |
| Article description | `18px / 28px`, `DMSans 400` | hidden on mobile cards | `#495D7A` |
| Metadata | `14px / 20px`, `DMSans 400` | same | `#96A2B3` |
| Header nav | `1.4rem / 2`, `DMSans 400` | mobile menu `1.6rem / 1.5` | white over hero, `#081B37` when sticky |
| Footer nav / copyright | `1.3rem`, line-height `1.35-2` | centered stack | nav white, meta `#96A2B3` |

Base HTML uses `font-size: 62.5%`, so `1rem` equals `10px`.

## Buttons and CTAs

### Primary Orange Button

Used by the homepage search form and program widgets.

- Background: `#FF8600`
- Hover background: `#FF9F34`
- Text: `#FFFFFF`
- Font: `Author 600`, usually `1.8rem`
- Shape: `border-radius: 100px` for standalone widgets
- Padding variants: `22px 22px 22px 30px`, `20px 21px 20px 26px`, or `18px 14px`
- Icon: right arrow SVG, white stroke, typically with `15px` left margin

Hero search variant:

- Width: `220px` desktop
- Padding: `20px 12px`
- Shape: `border-radius: 0 0 16px 16px`
- Has a left slanted tab using `border-right: 59px solid #FF8600` and `border-bottom: 60px solid transparent`
- Mobile removes the slant and becomes full width with `padding: 15px 12px`

### Secondary Navy Button

Used for the "Start Exploring" CTA.

- Background: `#1B3459`
- Hover background: `#0B75D7`
- Text: `#FFFFFF`
- Font: `DMSans 500`, `18px / 60px`
- Size: max-width `222px`, height `60px`
- Shape: `border-radius: 40px`
- Shadow: `0 1px 2px rgba(16,24,40,.05)`
- Icon: white right-chevron background image positioned near the right edge

### Text CTA

Used for "View All" category links.

- Font: `DMSans 400`, `18px / 28px`
- Color: `#1B3459`; white on navy cards
- Padding right: `8px`
- Icon: inline right arrow SVG with `4px` left offset
- Hover: underline
- Mobile: text hidden (`font-size: 0`), icon remains visible

### Carousel Arrow Buttons

- Size: `44px x 44px`
- Shape: circular (`border-radius: 50%`)
- Background: `#FFF3E6`
- Border: `1px solid #FFAE54`
- Icon: orange outlined arrow SVG
- Hover: background `#FF8600`, icon changes to white

## Cards and Containers

### Page Containers

- Global `.container`: max-width `1054px`, centered, `padding: 0 20px`
- Homepage/header/footer override: max-width `1320px`
- Main content avoids hard cards for page-level sections; bands and large image sections separate major content.

### Hero

- Section padding: `125px 0 192px`
- Mobile padding: `266px 0 50px`; tablet `340px 0 40px`
- Visual: dark navy left field with full-bleed student/campus image on the right and a wave transition into the next pale band
- Text content max-width: `640px`; inner content max-width `552px`

### Subject Carousel Cards

- `.swiper-slide`: `border-radius: 16px`, `overflow: hidden`, image-cover background
- Inactive scale: `.84`; active scale: `1`
- Hover lift: `translateY(-15px)` on desktop
- Title overlay: bottom-aligned gradient from transparent to `#1B3459` with `.9` opacity
- Title area padding: `56px 24px 24px`
- Icon: `44px` circle, turns orange on card hover

### Article / Category Cards

- Base `.category-block-2`: background `#F9F9F9`, border `1px solid #E2E7F0`, `border-radius: 12px`, padding `25px 20px 24px`, horizontal margin `25px`
- Navy feature card: background `#1B3459`, white headings/text
- White degree cards: background `#FFFFFF`
- Bootcamp card: background `#E2E7F0`, shadow `0 4px 7px 0 #D2D2D2`
- Career card: shadow `0 4px 6px 0 rgba(0,0,0,.07)`
- Image thumbnails: `border-radius: 10px`, `overflow: hidden`, object-fit cover
- Standard thumbnail: `188px x 130px`; degree thumbnail: full width x `294px`
- Hover: image scales to `1.1`; title underlines and turns `#FF8600`

### Program / Form Cards

- `.find-program-long`: background `#FFFFFF`, border `1px solid #F7F7F7`, `border-radius: 20px`, shadow `0 50px 50px rgba(0,0,0,.05)`, padding `40px 20px`, width `298px`
- Horizontal variant: width `100%`, margin `20px 0`, padding `40px 20px 20px`
- Mixed content wrapper: background `#FFFFFF`, `border-radius: 20px`, shadow `0 50px 50px rgba(0,0,0,.05)`, max-width `880px`

## Spacing System

The site does not use a named spacing scale, but these values repeat enough to treat as tokens:

| Token | Value | Common Usage |
| --- | --- | --- |
| `space-4` | `4px` | Icon offsets |
| `space-8` | `8px` | CTA/link/icon gaps |
| `space-10` | `10px` | Dropdown labels, small card gaps |
| `space-12` | `12px` | Mobile CTA padding, separators |
| `space-15` | `15px` | Form/icon horizontal gaps |
| `space-16` | `16px` | Header/card small margins, mobile text padding |
| `space-20` | `20px` | Container gutter, card padding, image/text gap |
| `space-24` | `24px` | Footer copyright gap, carousel title padding |
| `space-25` | `25px` | Category card padding/margins |
| `space-30` | `30px` | Footer link gaps, form/icon placement |
| `space-35` | `35px` | Form field vertical gap |
| `space-40` | `40px` | Section/card vertical padding |
| `space-50` | `50px` | Section overlaps and tab gaps |
| `space-52` | `52px` | Section intro bottom margin |
| `space-60` | `60px` | CTA height, content-band padding |
| `space-70` | `70px` | Blog section bottom padding |
| `space-80` | `80px` | Major section padding, CTA top margin |
| `space-120` | `120px` | Major top section offset |
| `space-200` | `200px` | Large section bottom padding |

Use `20px` horizontal page gutters on standard containers.

## Header Structure

Desktop header:

- Fixed/sticky header inside `.banner-main-wrap`
- `.container` uses flex alignment and max-width `1320px`
- Left: SVG logo with white and black variants
- Right: desktop nav with links: Degree Programs, Bootcamps, Blog, About Us
- Initial desktop state over hero: transparent/dark hero context, white logo and white nav text
- Sticky state: `position: fixed`, top `0`, width `100%`, z-index `99999`, background `#FFFFFF`, shadow `rgba(149,157,165,.2) 0 8px 24px`; black logo shown and nav turns `#081B37`
- Nav hover: `2px` orange underline animated from right-to-left using `#FF8600`

Mobile header:

- Background `#193154`
- Padding `20px 0`
- Desktop menu hidden; hamburger shown at right
- Hamburger: two white `2px` rounded bars; sticky version turns black
- Slide-out menu: full-screen white panel, z-index `99999`, menu links `17px 50px 17px 28px`, border-bottom `1px solid #E1E1E1`, arrow icon at right in orange
- Close row background `#F8F8F8`

## Footer Structure

- Background: `#1B3459`
- Padding: `58px 0 54px`; mobile `40px 0`, then `24px` top below `650px`
- Top wave image overlays at `top: -28px`
- Container max-width: `1320px`
- Desktop layout: two columns using `.footer-wrap`
- Left: white SVG logo, copyright, Facebook and Instagram filled white icons
- Right: footer nav links, then legal disclosure copy
- Footer links: `1.3rem / 2`, white, inline row, `30px` right margin
- Footer link hover: same animated `2px` orange underline as header
- Disclosure text: `1.3rem / 1.5`, `#96A2B3`, opacity `.8`
- Mobile: columns stack centered, social icons move under nav via `.icons-wrap.mob`, nav becomes vertical with `38px` rows, hover underline disabled

## Form Input Styles

### Hero Search Form

- Three dropdowns in a horizontal row on desktop; each takes `33.3333%`
- Dropdown toggle: white surface, `height: 100%`, padding `18px 20px`
- Outer corners: first dropdown `16px 0 0 16px`, last dropdown `0 16px 0 0`
- Dividers: `1px` vertical line in `#E2E7F0`
- Text: `DMSans 400`, `16px / 19px`, `#39495F`
- Arrow indicator: filled SVG, `#96A2B3`, `15px x 12px`
- Disabled fields: white background, cursor `not-allowed`, opacity `.9`
- Dropdown menu: margin `-12px 0 0`, max-height `170px`, scrollable
- Dropdown item: `16px`, `#39495F`, padding `8px 5px 8px 25px`
- Dropdown hover/highlight: background `#F0F3F9`, text `#01112B`
- Scrollbar thumb: `#D9D9D9`, white border, `10px` radius

### Custom Select / Long Form Variant

- Selected field: background `#FFFFFF`, border `1px solid #E1EAF3`, `border-radius: 10px`, color `#1B3459`
- Default padding: `2.2rem 6rem 2.2rem 3.7rem`
- Open border: `#4E69FF`; scoped program variants keep open border `#E1EAF3`
- Dropdown wrapper: background `#FFFFFF`, border `1px solid #E1EAF3`, `border-radius: 10px`, shadow `0 10px 10px rgba(169,177,185,.2)`, top `74px`
- Floating label: background white, `1.6rem`, padding `10px 8px`, positioned above field
- Long form field: `border-radius: 10px`, padding `17px 22px 8px`, `1.8rem / 35px`

## Icon Style

- Primary icon language is inline SVG, not icon fonts.
- Icons are mostly outlined with rounded strokes, using navy/gray strokes plus orange highlights.
- CTA arrows use simple right-arrow or chevron SVGs with white stroke.
- Category icons are small outlined illustrations, usually navy/blue-gray with `#FF8600` details.
- Footer social icons are filled white SVGs.
- Logo is inline SVG with navy/white wordmark variants and a solid orange block.

## Common UI Patterns

- Section separation: pale blue-gray bands (`#F0F3F9`) with curved/wave transitions rather than hard horizontal rules.
- Hero composition: full-bleed image and navy overlay, white copy, compact search widget, orange CTA.
- CTAs: orange for conversion/search, navy for exploration/content CTA, text links with orange hover underlines.
- Headline highlights: wrap key phrase in `span` and color `#FF8600`.
- Cards: use rounded corners from `10px` to `20px`; image cards use `16px`; article cards use `12px`.
- Hover motion: image cards lift or zoom; text links underline and titles turn orange.
- Content rhythm: large vertical bands (`80px+`) for major sections; `20-25px` card padding; `40-60px` internal section padding.
- Data/meta rows: small outlined date/time icons with gray text and orange icon detail.
- Navigation affordance: links do not change background; they animate a thin orange underline.

## Implementation Notes

- Use `#FF8600` as the canonical action/highlight color.
- Use `#1B3459` for dark surfaces and secondary CTAs; use `#081B37` for main heading/ink text.
- Prefer `Author 600` for large headings and CTA labels in form modules.
- Prefer `DMSans 400/700` for body copy, nav, article headings, dropdowns, and metadata.
- Keep page-level sections unframed; reserve cards for repeated content, forms, and article/category modules.
- Use inline SVG icons that can inherit or explicitly set `#FF8600`, `#96A2B3`, `#1B3459`, or white.
