# P5 — React Three Fiber + Next.js + niveau pro (S35-S42)

But : passer au stack le plus demandé en agence (R3F + Next.js + GSAP), et aux exigences pro : perf, accessibilité, CMS, déploiement, workflow avec designers.

## S35 — R3F bases
- TJJ : React Three Fiber, Drei, debug (Leva), environnement et staging, chargement de modèles.
- Livrable : porter la scène P3 en R3F, comparer avec la version vanilla.

## S36 — R3F avancé
- TJJ : mouse events R3F, post-processing R3F, physique Rapier R3F, Portal Scene R3F.
- Shaders custom en R3F (`shaderMaterial` de Drei).
- Livrable : port d'un effet shader P4 en composant R3F réutilisable.

## S37 — Next.js + WebGL + GSAP
- App Router, canvas WebGL persistant entre les routes, transitions de page WebGL, `useGSAP`, Lenis en React.
- Livrable : starter perso « Next + R3F + GSAP + Lenis » propre, réutilisable en mission.

## S38 — Performance pro
- Lighthouse, Core Web Vitals, budget JS, lazy loading des scènes et assets.
- Compression : Draco, Meshopt, KTX2/Basis, `gltf-transform`. Qualité adaptative (`detect-gpu`, DPR dynamique). Tests sur vrais devices mobiles.
- Livrable : audit + optimisation du Projet P3 (mesures avant/après).

## S39 — Robustesse et accessibilité
- `prefers-reduced-motion` en WebGL, fallback sans WebGL, focus et clavier, SEO avec WebGL (contenu DOM réel).
- CMS headless courant en agence (Sanity ou Prismic) : contenu piloté.
- Livrable : starter S37 enrichi (CMS + fallbacks + a11y).

## S40 — Workflow agence
- De la maquette Figma à la spec motion, estimation, découpage, échanges avec le DA, git flow, déploiement Vercel, gestion des retours.
- Étude de studios de référence : Lusion, Active Theory, 14islands, Locomotive, Immersive Garden, Resn (Jour léger + J1).
- Livrable : spec motion écrite pour une maquette existante, avec estimation en jours.

## S41-S42 — Projet de validation P5
- **Site complet déployé** : Next + R3F + GSAP + CMS, d'après une maquette de designer (idéalement collaboration réelle : designer junior, asso, ami).
  - Perf auditée, a11y, fallbacks, contenu piloté par CMS.
  - **Pièce portfolio #3.** Génération IA autorisée sur le boilerplate uniquement (P0-P4 validées).
