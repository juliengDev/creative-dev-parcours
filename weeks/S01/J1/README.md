# S01 J1 — Transitions, transforms, easing

**Phase** : P0 Socle · **Durée** : 5 h · **IA** : explications OK, code interdit.

## Objectif du jour

Sentir la différence entre une animation « qui bouge » et une animation « qui a du feel ». Maîtriser `transition`, `transform` et `cubic-bezier`.

## Théorie courte (à retenir)

1. **Ce qu'on anime** : seulement `transform` et `opacity` (étape compositing, GPU). Animer `width`, `top`, `margin`… déclenche un reflow à chaque frame → jank.
2. **`transform`** : `translate`, `rotate`, `scale`, `skew`. L'ordre compte : `rotate(45deg) translateX(100px)` ≠ `translateX(100px) rotate(45deg)`. `transform-origin` définit le pivot.
3. **Easing = intention** :
   - `ease-out` → ce qui **entre** à l'écran (réactif, arrive en douceur).
   - `ease-in` → ce qui **sort** (part en accélérant).
   - `ease-in-out` → ce qui **se déplace** d'un point à un autre déjà visible.
   - `linear` → presque jamais pour du mouvement ; ok pour rotation continue ou couleur.
4. **Durées** : micro-interaction 150-300 ms, élément moyen 300-500 ms, grand déplacement 500-900 ms. Plus c'est gros ou loin, plus c'est long.
5. **`cubic-bezier(x1, y1, x2, y2)`** : `y` hors de [0, 1] = overshoot. Ex. `cubic-bezier(0.34, 1.56, 0.64, 1)` (ease-out-back).
6. **Asymétrie** : souvent entrée plus lente que sortie (hover in 300 ms, hover out 200 ms) → déclarer la transition différemment sur l'état de base et l'état `:hover`.

## Ressources (dans cet ordre)

1. Josh Comeau — *An Interactive Guide to CSS Transitions* (joshwcomeau.com) — ~1 h, jouer avec chaque démo.
2. cubic-bezier.com — 20 min à tester des courbes, comparer avec `ease`.
3. easings.net — repérer visuellement : sine, quad, cubic, quart, expo, back, elastic.
4. MDN — `transform`, `transform-origin`, `transition` (référence, pas lecture complète).

## Exercice — « Easing lab » (≈ 3 h)

Dans `weeks/S01/J1/` : créer `index.html` + `style.css`. CSS pur, zéro JS.

1. **Piste de courses** : 6 carrés alignés à gauche, au hover de la page ils traversent jusqu'à droite en 800 ms, chacun avec un easing différent : `linear`, `ease`, `ease-in`, `ease-out`, `ease-in-out`, et un `cubic-bezier` overshoot perso. Label du nom à côté. But : voir les différences à l'œil.
2. **Bouton premium** : au hover, léger lift (`translateY`) + scale + ombre, au `:active` enfoncement. Entrée et sortie avec durées et easings différents (asymétrie).
3. **Card 3D tilt statique** : au hover, la carte pivote légèrement en 3D (`perspective`, `rotateX/Y`), l'image interne se décale (parallax léger), `transform-origin` réfléchi.
4. **Transition interrompue** : survoler puis quitter vite le bouton. Observer ce que fait le navigateur (retour depuis la position courante). Noter l'observation dans `NOTES.md`.

## Critères de réussite (Revue)

- Uniquement `transform` / `opacity` animés (box-shadow toléré sur le bouton, mais justifie le coût dans `NOTES.md`).
- Chaque choix d'easing justifié en 1 ligne dans `NOTES.md` (entrée / sortie / déplacement).
- DevTools → Rendering → *Paint flashing* activé : aucun repaint parasite pendant les animations de la piste.
- `@media (prefers-reduced-motion: reduce)` : animations réduites (pas supprimées brutalement : fondu court à la place).

## Fin de journée

- Ajouter 2+ mots nouveaux dans `LEXIQUE.md` si rencontrés.
- Lancer `pnpm dev`, ouvrir `/weeks/S01/J1/`.
- Me dire « Revue S01 J1 » → je relis code + `NOTES.md`.
