# Site Alain Papazoglou · Kredeum

Page d'accueil d'Alain Papazoglou (développeur senior, IA appliquée au code) et de Kredeum (studio logiciel et IA à Rennes). Publiée sur GitHub Pages depuis la branche `main`, racine du dépôt.

## Structure

- `index.html` : la page entière, HTML statique avec styles en ligne. Pas de build.
- `en/index.html` : la même page en anglais, même structure. Toute modification de `index.html` se reporte ici. Le français est la langue par défaut. Lien vers l'autre langue en pied de page seulement, jamais dans le menu.
- `.nojekyll` : désactive Jekyll sur GitHub Pages.
- `CNAME` : domaine personnalisé `alain.kredeum.com` (entrée CNAME chez OVH vers kredeum.github.io).
- `README.md` : présentation du dépôt, reprend l'accroche de la page et les liens de contact (à tenir à jour si l'en-tête change).

## Charte

Deux thèmes : nuit (le thème d'origine) et jour. Au premier passage, le thème suit le réglage clair ou sombre du système. Le bouton soleil/lune en fin de menu permet de basculer, et le choix est retenu (`localStorage`, partagé entre FR et EN). Sans JavaScript, la page s'affiche en nuit.

Toutes les couleurs passent par des variables CSS définies en tête de page : `:root` pour la nuit, `:root[data-theme="day"]` pour le jour. Ne jamais écrire une couleur en dur dans un `style=""`. Utiliser une variable existante, ou en ajouter une dans les deux blocs. Certaines variables portent un rôle (`--malt-bg`, `--team-bg`, `--pastille-bg`…), parce qu'une même couleur de nuit devient deux couleurs différentes en jour.

Nuit :
- Fond noir chaud `#0E0D0C`, bandes alternées `#24201C` avec liseré `rgba(243,233,220,0.3)`.
- Texte blanc cassé `#F3ECE4`, texte secondaire `#CFC6BC`, gris `#A89F95`.
- Crème `#F3E9DC` pour les boutons et les encadrés ; orange `#FF7A2F` uniquement pour du texte (titres en italique, chiffres, étiquettes), jamais en fond d'encadré. Orange foncé `#B4410F` pour le texte orange sur fond crème.

Jour (aucun aplat noir) :
- Fond papier `#F5F0E8`, bandes `#ECE5D9`, liserés en `rgba(22,19,15,…)`.
- Texte encre `#16130F`, secondaire `#5E554B`, gris `#8A8076`, orange brûlé `#C2410C`.
- Encadrés blancs, cartes `#FBF8F3`, « Avec l'IA » et « Avec l'équipe Kredeum » sur abricot `#F6E3D3`. Boutons pleins et pastilles en orange brûlé avec texte blanc.

Les propositions de design écartées sont gardées dans le tag `designs-2026-11-10` (page de comparaison `design/index.html`).

Communs aux deux thèmes :
- Polices Google Fonts : Gelasio (titres, proche de Georgia) et Inter (texte).
- Boutons : pilule avec pastille ronde à droite contenant une flèche, deux couleurs par bouton (noir + crème).
- Le titre principal doit tenir sur 2 lignes en écran large.

## Contenu

- Positionnement : Alain en façade, son équipe en renfort. Écrire au « nous », y compris pour ce qu'Alain fait lui-même (choix d'Alain : il n'aime pas le « je »).
- Jamais « on » : toujours « nous ».
- Style direct et sans remplissage (pas de « le tout… »). Listes d'actions à l'infinitif, pas à l'impératif.
- Espace insécable (`&nbsp;`) avant « ? », « : », « ! » et « ; », pour qu'ils ne passent jamais seuls en début de ligne.
- Kredeum le moins possible : nommé seulement dans le nom en haut à gauche (« Alain Papazoglou @ Kredeum »), la phrase d'en-tête (« Projet ambitieux, besoin de plus de ressources ? L'équipe Kredeum vous accompagne »), dans l'étiquette « Avec l'équipe Kredeum » de la démarche, dans le texte du bloc contact (« avec Alain ou l'équipe Kredeum »), et en pied de page (« © 2026 Alain Papazoglou @ Kredeum · Rennes », lien « Kredeum » vers labs.kredeum.com). Ailleurs, dire « l'équipe ».
- Sections : en-tête, Votre projet (3 types), La démarche (3 étapes + deux façons de travailler), Nos références (expérience + preuve chiffrée), Contact.
- Pas de section équipe ni de photos : l'équipe est présentée sur labs.kredeum.com.
