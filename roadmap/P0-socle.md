# P0 — Socle (S01-S04)

But : retrouver CSS motion, maîtriser la boucle d'animation JS sans lib, acquérir maths niveau 1, découvrir Canvas 2D. Aucune librairie d'animation.

## S01 — CSS motion
- Transitions, `@keyframes`, `transform` (translate/rotate/scale, `transform-origin`), `cubic-bezier`, `animation-*`, `steps()`.
- Perf : layout → paint → composite, propriétés « gratuites » (`transform`, `opacity`), `will-change`, DevTools Performance + Rendering (paint flashing).
- `prefers-reduced-motion`.
- Ressources : Josh Comeau — *An Interactive Guide to CSS Transitions*, *An Interactive Guide to Keyframe Animations* ; easings.net ; cubic-bezier.com ; MDN.
- Livrable : 5 micro-interactions CSS pur (bouton, loader, menu burger → croix, card hover 3D, reveal de titre ligne par ligne).

## S02 — Boucle d'animation JS
- `requestAnimationFrame`, delta time, boucle indépendante du framerate.
- Écrire à la main : `lerp`, `clamp`, `map` (remap), `normalize`, easing functions (quad, cubic, expo, back, elastic).
- Pointer events, scroll, resize (debounce), `IntersectionObserver`, Web Animations API.
- Ressources : MDN rAF ; Freya Holmér — *Lerp smoothing is broken* (YouTube) ; easings.net (formules).
- Livrable : curseur custom avec suivi lissé (lerp frame-rate independent) + reveal au scroll maison + barre de progression scroll.

## S03 — Maths 1 + Canvas 2D
- Vecteurs 2D : addition, soustraction, longueur, normalisation, produit scalaire. Trigo : `sin`/`cos`, cercle unité, radians, `atan2`, coordonnées polaires.
- Canvas 2D : contexte, formes, paths, `save/restore`, `translate/rotate/scale`, `devicePixelRatio`, resize net.
- Ressources : *Coding Math* (Keith Peters, YouTube, épisodes 1-15) ; Freya Holmér — *Math for Game Devs* (YouTube, partie vecteurs) ; MDN Canvas tutorial.
- Livrable : classe `Vec2` maison, horloge analogique animée, système orbital, oscillateurs (ondes sinusoïdales combinées).

## S04 — Canvas avancé + validation
- Particules simples (tableau d'objets, vie, vitesse, friction), pointeur comme force, trails (`globalAlpha`, fond semi-transparent), blend modes (`globalCompositeOperation`).
- **Projet de validation P0** — *Hero vanilla interactif* :
  - Intro animée CSS (titre, sous-titre, CTA) séquencée.
  - Fond Canvas interactif réagissant au pointeur (vecteurs + lerp).
  - Reveal au scroll maison (`IntersectionObserver`).
  - 60 fps vérifiés au profiler, `prefers-reduced-motion` géré, net sur écran retina.
  - Zéro librairie, zéro code IA.
