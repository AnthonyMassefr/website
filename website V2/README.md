# Solar Scale — Site V2 (wrapper Perspective)

Ce dossier contient **tout le site**. C'est une page unique qui affiche le tunnel
Perspective en plein écran via une iframe.

## Comment modifier le site
Tout le contenu (textes, images, vidéos, étapes, formulaire) se modifie **dans Perspective**.
Publier dans Perspective = le site est à jour immédiatement. Aucun redéploiement nécessaire.

Ce dossier ne change que si l'on veut modifier :
- le `<title>` / la meta description (référencement Google)
- l'image de partage Open Graph (`og:image`)
- le favicon

## Déploiement Vercel
Le projet Vercel doit être configuré avec :
- **Root Directory** : `website V2`
- **Framework Preset** : Other
- Aucune commande de build

Domaines : `solarscale.fr` + `www.solarscale.fr`

## Tunnel embarqué
- ID embed : `6a072b93fb8f6c4a2bc19c08`
- URL directe : https://perspectivefunnel.co/69304373d3e309003cb76956/6a072b93fb8f6c4a2bc19c08/

Si l'on change de tunnel dans Perspective, il faut remplacer l'`id` de l'iframe,
l'URL `src`, **et** l'ID dans le `<script>` en bas de `index.html` (3 endroits).

## Tracking
Les pixels Meta / Google doivent être configurés **dans Perspective**, pas ici :
le tunnel tourne dans l'iframe sur le domaine `perspectivefunnel.co`, un pixel posé
sur cette page ne verrait qu'une seule pageview et aucun événement du tunnel.
