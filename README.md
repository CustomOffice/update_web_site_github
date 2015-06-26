# update_web_site_github
Instruction pour personnaliser les sitewebs des projets github, avec intégration du plugin Lytebox (mise en page légèrement modifier)

## Sources
[Lytebox](<http://lytebox.com/>)

## Instructions
1. Créer le siteweb du projet à l'aide l'assistant (texte, code, titre etc) ajouter éventuellements les images et publier
	```bash
		# Description
		Ce calendrier utilise uniquement des formules et mise en forme conditionnel.

		# Paramètres
		- Année
		- Jours ouvrés/non-ouvrés
		- Premier jour de la semaine
		- Affichage des mois (court / complet)
		- Liste des jours fériés (inclus vacances)

		# Captures d'écran
		![Vue du calendrier](https://raw.githubusercontent.com/CustomOffice/Calendrier_Paysage/gh-pages/captures/calendrier.png)
		![Vue des paramètres d'affichage](https://raw.githubusercontent.com/CustomOffice/Calendrier_Paysage/gh-pages/captures/parametre.png)

		# Infos fichiers :
		**Logiciel :** Excel 2010    
		**Taille :** 45 Ko    
		**Extension :** .xlsx 
	```
2. Ajouter dans le dossier images du site Github les images contenues dans le dossier miniature de ce projet (branche gh-pages/images)
3. Ajouter les fichiers Lytebox.js et Lytebox.css à la racine du site (branche gh-pages)
4. Remplacer le fichier stylesheet.css dans le dossier stylesheets (branche gh-pages/stylesheets)    
5. Remplacer le bouton sprite_download.png dans le dossier images (branche gh-pages/images) 
6. Modifier le fichier index.html comme suit 
	* Ajouter au `<head>` :
	```bash
	<link rel="stylesheet" type="text/css" media="screen" href="lytebox.css">
	<script type="text/javascript" language="javascript" src="lytebox.js"></script>
	```

	* Remplacer le `<p>` pour les images par :
	```bash
	<p>
		<a href="captures/calendrier.png" class="lytebox" data-lyte-options="group:vacation" data-title="Vue du calendrier" data-description="">
			<img src="captures/calendrier.png" alt="Vue du calendrier">
		</a>
		<a href="captures/parametre.png" class="lytebox" data-lyte-options="group:vacation" data-title="Vue des paramètres d'affichage" data-description="">
			<img src="captures/parametre.png" alt="Vue des paramètres d'affichage">
		</a>
	</p>
	```
	* Ajouter à la fin du `<footer>` :
	```bash
		<a href="http://download.custom-office.ch/"><img src="http://www.custom-office.ch/Logo_download_long.png" alt="Logo Custom Office site Download" id="logo_perso_download"></a>
		<a href="http://www.custom-office.ch"><img src="http://www.custom-office.ch/logo.png" alt="Logo Custom Office" id="logo_perso"></a>
	```

