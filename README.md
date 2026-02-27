# Brief

Legal case analyzer. Describe a complaint in plain language, and the analysis engine scores case viability, identifies legal issues, and suggests next steps.

## Architecture

```
User describes situation -> Analysis Engine -> Structured Results
```

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 820 180" fill="none">
  <style>
    text { font-family: -apple-system, BlinkMacSystemFont, sans-serif; }
    .box { rx: 12; ry: 12; stroke-width: 1.5; }
    .label { font-size: 13px; fill: #f5f5f7; font-weight: 600; }
    .sub { font-size: 10px; fill: #888; }
    .arrow { stroke: #555; stroke-width: 1.5; marker-end: url(#arrowhead); }
  </style>
  <defs>
    <marker id="arrowhead" markerWidth="8" markerHeight="6" refX="8" refY="3" orient="auto">
      <polygon points="0 0, 8 3, 0 6" fill="#555"/>
    </marker>
  </defs>
  <rect x="0" y="0" width="820" height="180" rx="16" fill="#1a1a2e"/>

  <!-- User Input -->
  <rect class="box" x="30" y="40" width="160" height="100" fill="rgba(255,255,255,0.06)" stroke="rgba(255,255,255,0.12)"/>
  <text class="label" x="110" y="78" text-anchor="middle">User Input</text>
  <text class="sub" x="110" y="98" text-anchor="middle">Textarea</text>
  <text class="sub" x="110" y="114" text-anchor="middle">Plain language</text>

  <!-- Arrow 1 -->
  <line class="arrow" x1="200" y1="90" x2="260" y2="90"/>

  <!-- Analysis Engine -->
  <rect class="box" x="270" y="28" width="200" height="124" fill="rgba(0,113,227,0.1)" stroke="rgba(0,113,227,0.3)"/>
  <text class="label" x="370" y="62" text-anchor="middle">Analysis Engine</text>
  <text class="sub" x="370" y="84" text-anchor="middle">Keyword detection</text>
  <text class="sub" x="370" y="100" text-anchor="middle">Area matching</text>
  <text class="sub" x="370" y="116" text-anchor="middle">Strength scoring</text>
  <text class="sub" x="370" y="132" text-anchor="middle">Step generation</text>

  <!-- Arrow 2 -->
  <line class="arrow" x1="480" y1="90" x2="540" y2="90"/>

  <!-- Results -->
  <rect class="box" x="550" y="28" width="240" height="124" fill="rgba(48,209,88,0.08)" stroke="rgba(48,209,88,0.25)"/>
  <text class="label" x="670" y="58" text-anchor="middle">Results</text>
  <text class="sub" x="670" y="80" text-anchor="middle">Strength gauge (0-95%)</text>
  <text class="sub" x="670" y="96" text-anchor="middle">Legal issues identified</text>
  <text class="sub" x="670" y="112" text-anchor="middle">Relevant areas of law</text>
  <text class="sub" x="670" y="128" text-anchor="middle">Recommended next steps</text>
</svg>

## Stack

- **Vite 7** -- dev server and build tool
- **Vanilla JavaScript** -- no framework, ES modules
- **animate.css** -- entrance/exit animations
- **Apple Liquid Glass** -- frosted glass cards, backdrop-filter blur, dark theme

## Project Structure

```
brief/
  index.html          Entry point (textarea + results shell)
  package.json        Vite 7 + animate.css
  src/
    main.js           App bootstrap, event listeners, state
    analysis.js       Mock analysis engine (keyword detection, scoring)
    ui.js             DOM rendering (results, loading states)
    style.css         Base reset, design tokens, glass primitives
    hero.css          Hero section + textarea input styles
    results.css       Results grid, gauge, tags, steps timeline
    layout.css        Footer, loading spinner, utility buttons
```

## Legal Areas Covered

- Employment Law (wrongful termination, harassment, discrimination)
- Landlord-Tenant Law (eviction, deposits, repairs)
- Personal Injury (negligence, accidents, medical)
- Consumer Protection (fraud, defective products, billing)
- Family Law (custody, divorce, support)

## Development

```bash
npm install
npm run dev
```

Build for production:

```bash
npm run build
npm run preview
```

## License

MIT 2026 Joshua Trommel
