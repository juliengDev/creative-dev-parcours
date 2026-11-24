# P3 — Three.js vanilla + Blender minimal (S15-S24)

But : maîtriser Three.js en vanilla, le pipeline Blender → glTF et l'intégration WebGL dans un vrai site. Maths niveau 3 (matrices, espaces, quaternions intuitifs).

Ressource principale : **Three.js Journey** (Bruno Simon) — achat S15. Suivre dans l'ordre. Faire chaque exercice dans `weeks/` puis une variation perso.

## S15 — Bases
- TJJ Basics : première scène, transformations, animations, caméras, fullscreen/resize, géométries, debug UI.
- Maths 3 : repères local/monde, matrices de transformation (intuition), quaternions (intuition, pas le calcul).
- Ressource maths : Freya Holmér — *Math for Game Devs* (parties transformations) ; *3D Math Primer for Graphics* (chapitres choisis).

## S16 — Textures, matériaux, lumières
- TJJ : textures (UV, filtrage, mipmaps), matériaux, 3D text, lumières, ombres.
- Livrable : scène perso composée (objet + typographie 3D + lumière soignée).

## S17 — Classiques
- TJJ : haunted house, particles, galaxy generator, scroll-based animation.
- Livrable : galaxy generator paramétrable + page scroll-based synchronisée GSAP.

## S18 — Avancé 1
- TJJ : physique (Rapier/Cannon), modèles importés (glTF, Draco), raycaster + événements souris, environment maps, rendu réaliste (tone mapping, color space).
- Livrable : scène avec objets cliquables, survol, physique légère.

## S19 — Blender 1 (~8 h)
- Interface, modélisation low-poly simple, modificateurs de base, UV unwrap, matériaux simples.
- Ressources : TJJ « Custom model with Blender » ; Blender Guru — *Donut* (partie modélisation uniquement).
- Livrable : modèle simple maison importé dans Three.js.

## S20 — Blender 2 : baking (~7 h) + scène baked
- Baking des lumières/textures, export glTF, optimisation (Draco, taille des textures).
- TJJ : Portal Scene (modélisation, baking, export, import).
- Livrable : scène baked perso, rendu beau à coût GPU minimal.

## S21 — Architecture et perf
- TJJ : *Code structuring for bigger projects* (classe Experience, singletons, events, resources loader), *Performance tips*.
- Outils : `stats.js`/`r3f-perf`-like, Spector.js, draw calls, instancing (`InstancedMesh`), dispose/fuites mémoire.
- Livrable : refactor de S18 en architecture Experience propre.

## S22 — WebGL dans un site
- Synchro DOM ↔ WebGL : plans WebGL calés sur des images DOM, synchro scroll (Lenis), resize, canvas fixe en fond.
- Ressources : tutoriels Codrops (images WebGL au scroll) ; flux Yuri Artiukh / Akella (YouTube) pour voir un pro travailler.
- Livrable : galerie d'images WebGL synchronisée au scroll (déformation simple au scroll, sans shader custom pour l'instant).

## S23-S24 — Projet de validation P3
- **Site 3D interactif** :
  - Modèle Blender perso baked, interactions raycaster, caméra pilotée au scroll, loader avec progression réelle.
  - Architecture Experience, dispose propre, 60 fps desktop / 30+ mobile.
  - Publié. **Pièce portfolio #1.**
