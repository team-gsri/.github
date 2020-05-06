# Guide de contribution standard GSRI

👉 [Version anglaise / english version](./CONTRIBUTING.md)

***Note :** ce document est une traduction du [GSRI Standard Contribution Guide](./CONTRIBUTING.md). En cas d'incohérence entre les deux documents, c'est la version anglophone qui s'applique. Cette version est fournie pour faciliter la compréhension mais n'a pas la valeur probante du document anglophone.*

Cette documentation offre des lignes directrices et des procédures standards pour contribuer à nos projets. Il s'agit d'une documentation générique susceptible d'être remplacée au niveau de chaque projet. Merci de vérifier le fichier `.guithub\CONTRIBUTING.md` du projet concerné pour davantage d'instructions.

## Possibilités de contribution aux projets GSRI

Il existe deux manières de contribuer à nos projets :

1. Suggérer des idées, donner un retour d'expérience
2. Contribuer au code source

**Note :** afin de contribuer au code source vous devez posséder un compte _github.com_.

## Comment transmettre des idées et retours d'expérience

La meilleure manière de procéder est d'ouvrir une `issue` sur le dépôt Github concerné.
Pour cela, rendez-vous sur le dépôt en question, et cliquez sur l'onglet `issues` en dessous du nom du dépôt.
Cliquez ensuite sur le bouton vert indiquant `New issue`, qui vous donnera accès au formulaire de création.

Avant d'envoyer votre `issue`, vérifiez que vous avez indiqué les éléments suivants :
* un titre significatif
* une description détaillée
* un label `bug` ou encore `enhancement`

Si vous avez besoin d'aide dans ce processus, n'hésitez pas à venir sur notre serveur Discord.

## Contribution ponctuelle au code source

**Note :** *cette procédure s'adresse aux contributeurs ponctuels hors-GSRI. Vous n'êtes pas autorisé à écrire directement dans le dépôt, mais vous pouvez soumettre une `pull request` depuis un `fork` de notre dépôt.*

### Fork le dépôt

La première étape pour contribuer est de réaliser un `fork` du dépôt. Cela signifie concrètement que vous créez votre propre copie de notre dépôt. Pour faire cela, cliquez simplement sur le bouton `Fork` en haut à droite de l'interface.

C'est tout.

### Cloner le dépôt

Vous devez utiliser un client git afin de télécharger et synchroniser votre travail avec le dépôt. Si vous n'êtes pas coutumier de git, nous vous recommandons l'usage de [Github Desktop](https://desktop.github.com/).

Une fois votre client git installé, rendez-vous sur la page de votre `fork` sur github.com, et cliquez sur le bouton vert `Clone or download` sur la droite de la page, puis cliquez sur `Open in Desktop` dans l'encart. Github Desktop démarrera alors et vous demandera où télécharger le code source. Sélectionner le dossier de votre choix puis cliquez sur `Clone` ; Github Desktop téléchargera les sources sur votre ordinateur.

### Modifier les sources

Vous pouvez alors travailler sur les sources à l'aide de votre éditeur favoris. Si vous n'en avez pas encore, nous vous conseillons [Microsoft Visual Studio Code](https://code.visualstudio.com/), qui fonctionne bien avec Github Dekstop. Si vous modifiez une mission, merci de suivre les lignes directrices *Comment contribuer aux missions Arma 3*.

Git dispose de trois différentes fonctions de suivi des changements :

* `git stage` signifie que vous considérez la version actuelle d'un fichier *prêt pour le commit*. C'est une façon efficace d'ajouter ou retirer des changements au commit en cours.

* `git commit` signifie que vos modifications en mode `stage` sont stockées **localement**. Chaque commit est associé à votre identité et vous pouvez ajouter une petite description résumant ce que vous avez modifié et pourquoi. Si vous n'avez rien mis en `stage`, git placera en mode `stage` tous les changements et créera le commit en fonction.

* `git push` permet d'envoyer vos *commits* vers Github. Toutes les modifications restent locales jusqu'à l'utilisation de la commande `push`. D'autres utilisateurs peuvent alors accéder à vos modifications depuis leur dépôt. Vous pouvez également récupérer le code `pushed` par d'autres personnes sur Github en utilisant la commande `fetch`.

### Conserver les dépôts synchronisés

Assurez-vous fréquemment que vous ne travaillez pas sur une version obsolète des sources. Vérifiez que votre branche n'a aucun commit *behind* (en retard) relativement à notre branche `master`. Si votre branche n'est pas à jour avec `upstream/master`, l'ouverture d'une `pull request` sera refusée par notre équipe.

Si vous avez besoin de mettre à jour, vous devriez synchroniser les changements de notre dépôt vers le votre. Cette opération se nomme *intégration*. Durant l'intégration, des conflits peuvent apparaître, par exemple si vous avez modifié une entité qui a été par ailleurs supprimée de notre dépôt par un autre développeur.

La résolution des conflits doit être effectuée sur votre branche de travail, car cela facilite les tests visant à s'assurer que le processus d'intégration n'a pas endommagé vos fonctionnalités. Une fois satisfait de la fusion, vérifiez que votre version du code source fonctionne toujours avant d'ouvrir une `pull request`. Cette technique est nommée *ping-pong merging*.

### Ouvrir une pull request vers upstream

Lorsque vous êtes satisfait de votre travail et que vous souhaitez nous le soumettre, vous pouvez ouvrir une `pull request` pour intégrer vos modifications *upstream*.

Ouvrez la `pull request` en sélectionnant `Branch` / `Create pull request` dans Github Desktop. Cela ouvrira dans votre navigateur un formulaire à remplir. Assurez-vous que la branche source est votre branche de travail, et que la branche destination est `master` sur notre propre dépôt. Une fois prêt, cliquez sur `Open pull request`.

 **Note : toutes les PR vers d'autres branches que `master` seront refusées.**

Les administrateurs du projet effectueront une revue de votre code avant de fusionner votre travail. Selon le type de projet, des tests et autres opérations automatisées pourront être mises en place afin de s'assurer de la robustesse de votre production. Si un problème apparait, ou si nous remarquons un détail à modifier, vous pourrez ajouter des commits sur votre propre branche de travail afin d'effectuer les corrections nécessaires : elles seront automatiquement ajoutées à votre `pull request`.

## Contribution régulière au code source

**Note :** cette procédure s'adresse aux membres du GSRI ou aux contributeurs réguliers identifiés. Ils·elles sont autorisés à contribuer directement dans notre dépôt afin d'éviter la prolifération des forks. Si vous n'êtes pas autorisés à contribuer directement au dépôt, référez-vous aux instructions de la section *Contribution ponctuelle au code source* plus haut dans ce document.

### Récupérer le droit d'écriture sur le dépôt

Votre première étape pour les contributions directes est d'obtenir les droits d'accès sur notre dépôt. Prenez contact avec nous sur Discord et nous étudierons votre demande.

### Cloner le dépôt

Si vous êtes un contributeur régulier, vous pouvez contribuer directement au dépôt. Vous n'avez pas besoin de créer de fork de notre dépôt : vous pouvez cloner directement le dépôt qui vous intéresse.

### Créer une nouvelle branche

**Note : cette étape est obligatoire.** Y circonvenir vous permettra de créer des commits sur master **localement**, mais toute tentative de `push` vers Github sera automatiquement refusée.

Afin de créer une branche, sélectionnez `Branch` / `New branch ...` dans le menu. Github Desktop demandera un nom de branche. Entrez le nom souhaité : pseudo, fonctionnalité... Dans le doute, demandez-nous si le nom choisi est pertinent. Assurez-vous que la branche source est `master`. Une fois créée, publiez la branche sur Github en cliquant sur le bouton dans la barre en haut de Github Desktop.

Les autres opérations sont similaires à celles décrites dans la procédure ci-dessus.

### Garder votre branche à jour avec master

Il est recommandé de vérifier régulièrement que vous ne travaillez pas sur une version obsolète des sources. Vérifiez que votre branche n'a aucun commit *behind* (en retard) relativement à notre branche `master`. Si votre branche n'est pas à jour avec `master`, l'ouverture d'une `pull request` sera refusée par notre équipe. Si des changements ont eu lieu sur la branche `master`, vous pouvez utiliser la fonction `Branch` / `Update from master` de Github Desktop afin de rattraper le retard. La résolution des conflits doit être faite sur votre actuelle branche de travail.

### Ouvrir une pull request vers master

Cette procédure est également la même que pour les contributeurs occasionnels. Votre dépôt doit être à jour avec `master`, sans quoi votre `pull request` sera refusée. Des tests et autres opérations automatisées pourront également être menées pour s'assurer de la robustesse de votre production. Les fusions sont ensuite faites par l'équipe de maintenance du GSRI. Vous pouvez ajouter des commit à votre branche de travail : ils seront automatiquement ajoutés à la PR en cours.

## Informations spécifiques à propos des contributions aux missions ArmA 3

Si vous souhaitez contribuer à une mission ArmA, voici les lignes de conduite à respecter :

### Dossier cible

Vous **DEVEZ** cloner le dépôt dans votre dossier `mpmissions` afin d'être en mesure de modifier et visualiser votre mission dans l'éditeur Eden. Ce dossier est situé à différents endroits selon la manière dont votre jeu est installé :

* Si vous n'avez jamais utilisé d'option en ligne de commande ni créé de nouveau profil pour ArmA 3, le dossier est `%USERPROFILE%\Documents\Arma 3\mpmissions`

* Si vous utilisez un profil personnalisé, le dossier est `%USERPROFILE%\Documents\Arma 3 - Other Profiles\<profile_name>\mpmissions`

* Si vous utilisez l'option `-profiles` en démarrant le jeu, le dossier est `<profiles_path>\Users\<profile_name>\mpmissions`

### Mods optionnels

Assurez-vous de n'utiliser **AUCUN** mod optionnel de notre modpack, ni aucun autre mod hors du core. Editer une mission avec de tels mods tend à créer des dépendances indésirables qui empêcheront quiconque ne possède pas ces mods de jouer ou de modifier votre mission.

### Binarisation du fichier de mission

**Vérifier que les fichiers ne sont *pas* binarisés.**

Cela concerne principalement les fichiers de type `mission.sqm`, mais également de type `config.cpp`. Git sait versionner efficacement les fichiers texte, pas les binaires. Cela permet également de garder un meilleur historique des changements. La binarisation du fichier final est prévue par nos outils avant publication sous forme de fichier PBO.

Par ailleurs, n'ajoutez pas de contenu binarisé ou archivé sous forme de PBO par vos propres soins. Nos outils se chargeront d'assembler, de binariser et d'archiver correctement tout le contenu depuis les sources.

Si vos modifications incluent de gros fichiers binaires (images, audio, video), merci de nous contacter afin de déterminer s'il doit être versionné dans Github ou bien être hébergée dans notre cloud privé pour intégration.

## Quelques conseils

* Débutez toujours votre travail en effectuant les actions `Fetch from Github` et `Update from master`.
* Travaillez toujours sur votre propre branche, n'ouvrez de `pull request` que vers `master`.
* Créez des commits petits et dotés de descriptions représentatives de vos changements.
* Créez des commits fréquemment, il s'agit d'un proche équivalent du raccourci `Ctrl + S` pour un document.
* Effectuez un `push` au moins quotidiennement, même si votre code ne fonctionne pas (mieux vaut inachevé que perdu).
* Le mode Fenêtré sans bordures sur ArmA 3 permet une transition plus aisée entre le jeu et le bureau.
