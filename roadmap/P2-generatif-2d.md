# P2 — Génératif 2D : Nature of Code (S11-S14)

But : penser en simulation (forces, systèmes, bruit). Base intuitive pour particules GPU et shaders plus tard. Maths niveau 2.

Ressource principale : *The Nature of Code* (Daniel Shiffman, édition 2024, gratuite en ligne : natureofcode.com) + vidéos The Coding Train. Exemples en p5.js : les suivre en p5, puis porter au moins un sketch par semaine en Canvas 2D + TypeScript vanilla avec ta classe `Vec2`.

## S11 — Hasard, bruit, vecteurs
- NoC ch. 0-1 : distributions, random walk, Perlin/simplex noise (`simplex-noise`), vecteurs (refactor `Vec2`).
- Maths 2 : produit scalaire appliqué, projection, angles entre vecteurs.
- Livrable : flow field au bruit avec des milliers de lignes, paramétrable via `lil-gui`.

## S12 — Forces et oscillation
- NoC ch. 2-3 : forces, masse, gravité, friction, traînée, attraction ; oscillation, pendule, ressorts (loi de Hooke).
- Lien UI : ressorts = « spring physics » des interfaces haut de gamme.
- Livrable : menu élastique au ressort, curseur à ressort, chaîne de ressorts suivant le pointeur.

## S13 — Particules et agents autonomes
- NoC ch. 4-5 : systèmes de particules, émetteurs, héritage ; steering (seek, arrive, flee), flocking (boids).
- Perf : object pooling, typed arrays, éviter le GC. Mention OffscreenCanvas / Worker.
- Livrable : texte formé de particules qui fuient le pointeur puis reviennent (effet classique de hero).

## S14 — Projet de validation P2
- **Hero génératif intégré** dans le site P1 (ou nouveau) :
  - Système génératif (flow field, particules texte ou boids) piloté par le scroll (ScrollTrigger) et le pointeur.
  - Panneau `lil-gui` en mode debug (`#debug`).
  - Perf : 60 fps desktop, dégradation adaptée sur mobile (moins de particules).
  - Zéro code IA.
