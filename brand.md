# Dirksen Engineering — Brand Document

**Client:** Dirksen Engineering
**Tagline:** Civil Engineering & Land Surveying
**Location:** Uvalde, TX (Southwest / West Texas)

---

## Colors

| Name         | Variable       | Hex       | Usage                                      |
|--------------|----------------|-----------|--------------------------------------------|
| Sand         | `--sand`       | `#F5F0E8` | Page background, service cards             |
| Sand Dark    | `--sand-dark`  | `#EDE5D4` | Hero right panel, contact section bg       |
| Tan          | `--tan`        | `#C9B99A` | Nav links, subtitles, borders, muted text  |
| Brown        | `--brown`      | `#7C6248` | Body copy, form labels, service desc       |
| Rust         | `--rust`       | `#B54A1E` | Primary CTA, eyebrows, accents, footer border |
| Rust Dark    | `--rust-dark`  | `#8C3A16` | Rust hover state                           |
| Earth        | `--earth`      | `#3D2B1F` | Nav bg, hero left, footer, headings        |
| Sky          | `--sky`        | `#4A7FA5` | Defined but not actively used in v-b       |
| White        | `--white`      | `#FDFCF9` | Warm off-white; text on dark, services bg  |
| Text Muted   | `--text-muted` | `#8A7560` | Defined; available for secondary text      |

### Color Roles Summary
- **Primary background:** Sand `#F5F0E8`
- **Dark / structural:** Earth `#3D2B1F`
- **Accent / CTA:** Rust `#B54A1E`
- **Supporting neutral:** Tan `#C9B99A`
- **Body on dark:** Tan; body on light: Brown

---

## Typography

### Typefaces

| Font            | Source          | Weights Used              | Role                          |
|-----------------|-----------------|---------------------------|-------------------------------|
| Bebas Neue      | Google Fonts    | Regular (400)             | Display headings, logo, stats |
| Source Serif 4  | Google Fonts    | 300, 400, 600 + italics   | Body prose, subtitles         |
| IBM Plex Sans   | Google Fonts    | 300, 400, 500             | UI text, nav, labels, forms   |

### Usage by Element

| Element             | Font            | Size                  | Weight | Style  | Letter-spacing | Transform  |
|---------------------|-----------------|-----------------------|--------|--------|----------------|------------|
| Nav logo            | Bebas Neue      | 22px                  | —      | —      | 0.12em         | —          |
| Nav logo sub        | IBM Plex Sans   | 9px                   | 400    | —      | 0.25em         | uppercase  |
| Nav links           | IBM Plex Sans   | 12px                  | 500    | —      | 0.1em          | uppercase  |
| Nav CTA             | IBM Plex Sans   | 12px                  | 500    | —      | 0.08em         | uppercase  |
| Hero title (h1)     | Bebas Neue      | clamp(72px–128px)     | —      | —      | 0.04em         | —          |
| Hero subtitle       | Source Serif 4  | 18px                  | 300    | italic | —              | —          |
| Hero tag / eyebrow  | IBM Plex Sans   | 10–11px               | 500    | —      | 0.22em         | uppercase  |
| Hero stat number    | Bebas Neue      | 52px                  | —      | —      | 0.04em         | —          |
| Hero stat label     | IBM Plex Sans   | 10px                  | 500    | —      | 0.18em         | uppercase  |
| Section eyebrow     | IBM Plex Sans   | 10px                  | 500    | —      | 0.25em         | uppercase  |
| Section title (h2)  | Bebas Neue      | clamp(40px–68px)      | —      | —      | 0.05em         | —          |
| Service name        | Bebas Neue      | 24px                  | —      | —      | 0.06em         | —          |
| Service desc        | IBM Plex Sans   | 15px                  | 300    | —      | —              | —          |
| Credentials list    | IBM Plex Sans   | 15px                  | 300    | —      | —              | —          |
| About title         | Bebas Neue      | clamp(36px–60px)      | —      | —      | 0.05em         | —          |
| About body          | Source Serif 4  | 17px                  | 300    | —      | —              | —          |
| Contact title       | Bebas Neue      | clamp(36px–56px)      | —      | —      | 0.05em         | —          |
| Contact body        | Source Serif 4  | 16px                  | 300    | —      | —              | —          |
| Form labels         | IBM Plex Sans   | 10px                  | 500    | —      | 0.18em         | uppercase  |
| Form inputs         | IBM Plex Sans   | 14px                  | 300    | —      | —              | —          |
| Footer logo         | Bebas Neue      | 18px                  | —      | —      | 0.1em          | —          |
| Footer copy         | IBM Plex Sans   | 11px                  | 300    | —      | —              | —          |

---

## UI & Style Patterns

### Layout
- Max content width: `1200px` (centered with `margin: 0 auto`)
- Base horizontal padding: `56px`
- Fixed nav height: `68px`
- Section vertical padding: `100px`

### Buttons

| Variant      | Background     | Text          | Border                       | Hover                        |
|--------------|----------------|---------------|------------------------------|------------------------------|
| `.btn-rust`  | Rust `#B54A1E` | White         | None                         | Rust Dark + translateY(-2px) |
| `.btn-ghost` | Transparent    | Tan           | 1px solid tan (30% opacity)  | Full tan border + white text |
| Nav CTA      | Rust `#B54A1E` | White         | None                         | Rust Dark                    |
| Form submit  | Rust `#B54A1E` | White         | None                         | Rust Dark                    |

- Button padding: `15px 30px` (hero); `16px` full-width (form)
- Font: IBM Plex Sans, 12px, weight 500, uppercase, 0.1em letter-spacing
- No border-radius — all elements are sharp/square

### Cards (Service Cards)
- Background: Sand `#F5F0E8`
- Padding: `36px 28px`
- Bottom border: 3px, transparent default → Rust on hover
- Hover: `translateY(-4px)` lift
- Icon: 40×40px Earth square, SVG stroke in Sand

### Forms
- Input/select/textarea border: `1px solid --tan`
- Background: Sand
- Focus border: Rust
- Font: IBM Plex Sans 14px weight 300
- No border-radius

### Eyebrow Style
- IBM Plex Sans, 10px, weight 500, uppercase, 0.25em letter-spacing
- Color: Rust
- Followed by a short `::after` rule: 1px Rust line, max-width 60px

### Decorative Motif
- Topographic concentric ring effect via `box-shadow` on `::before` pseudo-element
- Uses tan at very low opacity (2%–8%) on Earth background

### Animation
- `fadeUp` keyframe: opacity 0→1, translateY 20px→0, duration 0.6–0.7s ease
- Staggered delays: 0.1s increments per hero element

### Footer
- Background: Earth
- Top border: 3px solid Rust
- Logo: Bebas Neue 18px White
- Copy: IBM Plex Sans 11px Tan weight 300

---

## Brand Voice / Context Notes
- Established 2005, Southwest/West Texas
- Professional engineer (PE F-8848) and licensed surveyor (RPLS #10193741)
- Tone: authoritative, no-frills, regional expertise
- Aesthetic: industrial-earthy — warm neutrals, sharp geometry, no rounded corners
