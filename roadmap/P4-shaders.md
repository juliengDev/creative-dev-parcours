# P4 — Shaders (S25-S34, pause S26)

But : écrire et inventer des shaders GLSL. C'est le différenciateur clé face à l'IA et aux juniors. Maths niveau 4 (fonctions de forme, bruit, SDF).

Ressources : *The Book of Shaders* (Gonzalez Vivo & Lowe) ; chapitres shaders de Three.js Journey ; articles d'Inigo Quilez (iquilezles.org) ; Shadertoy ; Frontend Masters — *WebGL Shaders* (Matt DesLauriers, S28-S29) ; The Art of Code (YouTube, raymarching).

## S25 — Premiers shaders
- Pipeline GPU : vertex vs fragment, attributes / uniforms / varyings, `ShaderMaterial` / `RawShaderMaterial`.
- BoS ch. 1-7 : uniforms, fonctions de forme (`step`, `smoothstep`, `mix`, `fract`), couleurs, formes.
- TJJ : Shaders (intro). Compte Shadertoy créé.
- Livrable : 10 mini-shaders 2D (dégradés, formes, motifs simples).

## S26 — Pause / consolidation
- Rien de nouveau. Rembourser les Dettes, refaire un exercice faible, ranger `PROGRESS.md`, repos.

## S27 — Motifs et bruit
- BoS ch. 8-11 : matrices 2D, motifs, random, bruit.
- TJJ : Shader patterns, Raging sea.
- Livrable : surface d'eau stylisée personnelle.

## S28 — Shaders dans Three.js
- TJJ : animated galaxy, modified materials (`onBeforeCompile`).
- Frontend Masters — *WebGL Shaders* (Matt DesLauriers), début.
- Livrable : effet de déformation d'image au survol (classique Codrops), écrit par toi.

## S29 — Bruit avancé + IQ
- BoS : fBm, cellular noise. Inigo Quilez : SDF 2D, smooth min, palettes cosinus, domain warping.
- Fin du cours Frontend Masters.
- Livrable : 3 pièces Shadertoy publiées.

## S30 — Raymarching
- SDF 3D, raymarching, normales, éclairage simple, ombres douces.
- Ressources : The Art of Code (*Raymarching for dummies*), articles IQ sur les primitives SDF.
- Livrable : scène raymarchée animée sur Shadertoy.

## S31 — Post-processing
- `EffectComposer`, passes custom, render targets (FBO), transitions plein écran entre deux scènes.
- TJJ : Post-processing.
- Livrable : transition entre deux scènes via un shader de dissolution maison.

## S32 — GPGPU
- Simulation sur GPU via textures ping-pong, `GPUComputationRenderer`.
- TJJ : GPGPU flow field particles.
- Livrable : 100k+ particules pilotées par un flow field sur GPU, réagissant au pointeur.

## S33-S34 — Projet de validation P4
- **Effets shader en site** :
  - Site (ou section) avec transitions d'images shader, effet signature au scroll/survol, post-processing léger.
  - Plus une pièce shader « pure » (Shadertoy ou plein écran) montrant ton style.
  - Zéro code IA. **Pièce portfolio #2.**
