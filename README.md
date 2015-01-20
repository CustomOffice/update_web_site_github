# update_web_site_github
Instruction pour personnaliser les sitewebs des projets github, avec intégration du plugin Lytebox (mise en page légèrement modifier)

## Instructions
1. créer le siteweb du projet à l'aide l'assistant (texte, code, titre etc) ajouter éventuellements les images et publier
2.Ajouter dans le dossier images du site Github les images contenues dans le dossier miniature de ce projet (branche gh-pages/images)
3.Ajouter les fichiers Lytebox.js et Lytebox.css à la racine du site (branche gh-pages)
4.Remplacer le fichier stylesheet.css dans le dossier stylesheets (branche gh-pages/stylesheets)
5.Modifier le fichier index.html comme suit 
  Ajouter au <head> :
'
<link rel="stylesheet" type="text/css" media="screen" href="lytebox.css">
<script type="text/javascript" language="javascript" src="lytebox.js"></script>
'

  Remplacer le <p> pour les images par :
'
<p>
	<a href="captures/calendrier.png" class="lytebox" data-lyte-options="group:vacation" data-title="Vue du calendrier" data-description="">
		<img src="captures/calendrier.png" alt="Vue du calendrier">
	</a>
	<a href="captures/parametre.png" class="lytebox" data-lyte-options="group:vacation" data-title="Vue des paramètres d'affichage" data-description="">
		<img src="captures/parametre.png" alt="Vue des paramètres d'affichage">
	</a>
</p>
'