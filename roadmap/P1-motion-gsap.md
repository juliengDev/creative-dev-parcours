# P1 — Motion maîtrisé : SVG + GSAP (S05-S10)

But : passer de « GSAP via IA » à maîtrise réelle. Savoir séquencer, scroller, transitionner, et nettoyer proprement. Sans IA.

## S05 — SVG
- `viewBox`, coordonnées, syntaxe des `path` (M, L, C, Q, A, Z), `stroke-dasharray/offset` (line drawing), `clipPath`, `mask`, filtres de base (`feTurbulence`, `feDisplacementMap`).
- Export propre depuis Figma (outline, nettoyage SVGO).
- Ressources : Sara Soueidan (articles SVG) ; Josh Comeau — *A Friendly Introduction to SVG* ; MDN SVG tutorial.
- Livrable : logo dessiné au trait, icônes animées, effet « liquide » avec filtre SVG.

## S06 — GSAP core
- `gsap.to/from/fromTo/set`, eases, `timeline`, position parameter, labels, `stagger`, callbacks, `gsap.context()` + `revert()`, `matchMedia`, `quickTo`, `utils` (mapRange, interpolate, wrap).
- Ressources : docs gsap.com (Getting Started + Timeline) ; Creative Coding Club (Carl Schooff) — cours gratuits GSAP 3 Express.
- Livrable : refaire les 5 micro-interactions S01 en GSAP + intro de site séquencée en une timeline pilotable (pause, reverse, seek).

## S07 — ScrollTrigger + Lenis
- `scrub`, `pin`, `snap`, `start/end`, markers, `batch`, scroll horizontal, `containerAnimation`, `refresh`. Lenis (smooth scroll) + synchro ScrollTrigger.
- Ressources : docs ScrollTrigger ; démos officielles GSAP (CodePen) ; README Lenis.
- Livrable : page storytelling : sections épinglées, section horizontale, parallax, compteur animé.

## S08 — Plugins GSAP (tous gratuits depuis 2025)
- SplitText (lignes, mots, chars, masques), Flip, DrawSVG, MorphSVG, MotionPath, Observer, Draggable + Inertia.
- Livrable : révélations typographiques éditoriales, galerie grille → plein écran (Flip), slider draggable avec inertie.

## S09 — Transitions de page + architecture
- View Transitions API vs Barba.js. Cycle de vie : init / destroy / cleanup, resize, préchargement.
- Décortiquer 3 sites Awwwards SOTD : noter structure, timings, eases, techniques supposées (Jour léger + J1).
- Livrable : mini-site 3 pages avec transitions et animations réinitialisées sans fuite.

## S10 — Projet de validation P1
- **One-page de marque fictive** à partir d'une maquette Figma communautaire (ou maquette perso) :
  - Loader + intro, scroll storytelling (pin, horizontal, parallax), typographie animée (SplitText), une interaction Flip ou Draggable.
  - Responsive (`matchMedia`), `prefers-reduced-motion`, 60 fps mobile milieu de gamme.
  - Zéro code IA. Publié (Vercel/Netlify). Candidate Pièce portfolio.
