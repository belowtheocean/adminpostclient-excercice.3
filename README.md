# adminpostclient-excercice.3 Gestion des permissions et sécurité des fichiers

<img width="544" height="295" alt="Capture d'écran 2025-10-08 105417" src="https://github.com/user-attachments/assets/754890b4-3267-473d-9374-cf32db47d9a3" />

Objectif :

Créer un fichier "secret.txt" dans un répertoire personnel, puis configurer les permissions pour que seul le propriétaire puiss y accéder. Enfin, vérifier qu'un autre utilisateur ne puisse pas voir ou modifier ce fichier.

Étapes réalisées : 

1. Création du répertoire
   - mkdir exercice3
   - cd exerice3
   - pwd
La commande mkdir "nom" permet de créer un dossier que j'ai nommé exercice3, et avec la commande cd j'ai pu me déplacer à l'intérieur du dossier puis vérifier le courant avec la commande pwd.
J'ai pu avoir comme résultat : /home/test/exercice3 ; ça montre que je travaille bien dans le bon dossier (exercice3).

2. Création du fichier secret.txt
  - touch secret.txt<img width="544" height="295" alt="Capture d'écran 2025-10-08 105417" src="https://github.com/user-attachments/assets/e44cca24-a53d-4f83-9ec0-dbc0b7a25ae1" />

La commande touch crée un fichier vide nommé secret.txt. Je l'utilise ici pour simuler un fichier confidentiel.

3. Modification des permissions du répertoire
  - chmod 700 .
La commande chmod permet de modifier les permissions d'accès, et 700 donne tous les droits : lecture, écriture, exécution ; au propriétaire, mais aucun droit au groupe ni aux autres utilisateurs.
J'ai obtenu comme résultat : drwx------ ; le répertoire exercice3 est donc totalement privé.

4. Modification des permissions du fichier
  - chmod 600 secret.txt
Pareil le chmod permet de modifier les permissions d'accès, et le 600 signifie : lecture et écriture uniquement pour le propriétaire. Ainsi, le fichier devient complètement privé.
J'ai eu comme résultat : -rw------- ; le fichier secret.txt est donc complètement protégé.

5. Vérification des permissions
  - ls -l
  - ls -ld .
Affiche les droits sur le fichier et le dossier.
J'ai obtenu comme résultat : -rw------- 1 test test 0 Oct  8 10:22 secret.txt et drwx------ 2 test test 4096 Oct  8 10:22 .
Ça confirme que seul l’utilisateur test peut accéder au fichier.

En résumé le dossier de l'exercice3 est accessible uniquement par le propriétaire. Et le fichier secret.txt est totalement privé. Aucun autre utilisateur ne peut lire, modifier ou supprimer son contenu.
