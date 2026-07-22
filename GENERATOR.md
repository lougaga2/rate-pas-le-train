# « Rate pas le train » — générateur d'édition

Instructions à exécuter à chaque édition (mercredi et dimanche). Chaque exécution
part de zéro : ce fichier contient tout ce qu'il faut savoir.

## Contexte

Veille personnelle IA / Tech de Louis. Deux éditions par semaine (mercredi, dimanche).
Chaque édition = une page HTML publiée sur GitHub Pages. Le lecteur unique est Louis.
Ton : français, clair, accessible (pas de jargon inutile). ~7 min de lecture.

## Emplacement

Dossier projet : `C:\Users\neuvi\rate-pas-le-train`
- `editions/AAAA-MM-JJ-<jour>.html` : une page par édition
- `index.html` : liste des éditions, la plus récente en haut
- `editions/2026-07-10-vendredi.html` : édition de référence pour le style/format (à imiter)

## Étapes

1. **Dater.** Déterminer la date du jour et le jour de la semaine (mercredi ou dimanche).
   Regarder le fichier le plus récent dans `editions/` pour connaître la date de la
   dernière édition : on ne couvre que l'actu parue **depuis** cette date.

2. **Rechercher.** Faire des recherches web sur les 6 thèmes, en ciblant les jours
   écoulés depuis la dernière édition :
   - 🤖 IA / modèles (nouveaux modèles, recherche, outils IA)
   - 🏢 Big Tech / business (GAFAM, OpenAI, levées, stratégie, régulation)
   - 🚀 Startups / produits (levées, lancements, nouveaux produits)
   - 🛠️ Dev / outils (frameworks, langages, open source, sorties techniques)
   - 🇨🇳 Chine (modèles et labos chinois, Alibaba/ByteDance/Moonshot/DeepSeek, régulation, géopolitique IA)
   - 🇪🇺 Europe (Mistral et startups européennes, levées, AI Act et régulation UE, souveraineté)

3. **Sélectionner.** Garder 10 à 15 actus notables au total, réparties dans les 6
   rubriques. **Ordre des rubriques : IA → Big Tech → Startups → Dev → Chine → Europe.**
   Une rubrique peut rester vide si rien de notable — ne jamais remplir artificiellement.
   Écarter toute actu déjà traitée dans l'édition précédente (comparer titres/sources).
   Éviter les doublons entre rubriques : une actu chinoise ou européenne va dans sa
   rubrique géographique plutôt que dans IA/Big Tech/Startups/Dev.

4. **Rédiger.** Créer `editions/AAAA-MM-JJ-<jour>.html` en copiant la structure EXACTE
   de l'édition de référence (`2026-07-10-vendredi.html`) : même CSS, même mise en page.
   Pour chaque actu : un `<h3>` titre court, un `<p class="desc">` de 2-4 phrases en
   français, un lien `<a>` « Source → » vers l'article réel (viser l'URL précise de la
   source, pas une page d'accueil générique). Mettre à jour le titre `<title>`, le `<h1>`
   reste « 🚂 Rate pas le train », et la date dans `.meta`.

5. **Mettre à jour l'index.** Ajouter une ligne `<li>` EN HAUT de la liste dans
   `index.html`, pointant vers la nouvelle édition, avec la date lisible (ex. « Dimanche
   12 juillet 2026 »).

6. **Publier.** Dans `C:\Users\neuvi\rate-pas-le-train` :
   ```
   git add -A
   git commit -m "Édition du <date>"
   git push
   ```
   GitHub Pages met la page en ligne tout seul en ~1 min.

## Cas d'échec (important)

- **Recherche vide / panne réseau / moins de ~6 actus notables** : NE PAS créer de page
  ni modifier l'index. À la place, créer un brouillon Gmail à neuville.louis75@gmail.com
  avec l'objet « Rate pas le train — pas d'édition aujourd'hui » expliquant brièvement
  pourquoi, puis s'arrêter. Mieux vaut pas d'édition qu'une édition vide.
- **Doublons** : toujours comparer à l'édition précédente pour ne pas répéter une actu.

## Rappel des contraintes

- Français, clair, ~7 min. 10-15 actus. 6 rubriques dans l'ordre IA → Big Tech → Startups → Dev → Chine → Europe.
- Titre du bulletin : « Rate pas le train ». Sections vides autorisées. Pas de doublons.
- Liens vers les vraies sources (URL précises).
