git# Collaborer avec main, develop et des branches de fonctionnalités
1- Créez un repo GitHub avec une branche main par défaut.
2- Clonez ce repository dans deux destinations différentes : un dossier Adam et un dossier Eve.  
   Vous pouvez travailler à deux pour cet exercice ou simuler la collaboration sur votre poste.
3- Depuis le dossier d’Adam, créez une branche develop à partir de main, poussez-la sur le dépôt distant :
   - Créez la branche develop à partir de main.
   - Poussez develop sur le repo distant.
   - Vérifiez vos branches locales et distantes.
5- Depuis le dossier d’Eve, récupérez les dernières informations du dépôt distant (branches, commits, etc.).  
   Assurez-vous que origin/develop est disponible localement puis créez une branche locale develop bindé à origin/develop.
6- Placez-vous sur develop côté Eve et créez une branche de fonctionnalité feature/login à partir de develop.  
   Faites un petit changement (par exemple, un fichier login.md avec quelques lignes de texte), commitez et poussez la branche feature/login sur le dépôt distant.
7- Vérifiez les branches locales et distantes depuis Eve : assurez-vous que feature/login existe à la fois en local et sur origin.
8- De retour sur Adam, synchronisez votre repo avec le dépôt distant :
   - Récupérez les nouvelles branches distantes.
   - Affichez l’historique sous forme de graphe, en une ligne, avec l’option --all (ou utilisez l’alias git lga si vous l’avez).
   - Créez une branche locale feature/login suivie de origin/feature/login.
   Vérifiez que vous voyez bien le commit d’Eve dans l’historique de feature/login.
9- Depuis Adam, ajoutez un nouveau commit sur la branche feature/login (complétez le travail d’Eve, par exemple en modifiant login.md).  
   Poussez ce commit sur origin/feature/login et vérifiez l’historique pour confirmer que les deux commits (Eve + Adam) sont présents.
10- Sur GitHub, depuis la branche feature/login, créez une pull request vers la branche develop.  
    - Vérifiez les commits inclus dans la PR.  
    - Ajoutez un petit message de description.
    - Mettez un reviewer (à minima copilot)
    - Fusionnez la PR dans develop.
11- De retour sur le dossier d’Eve, synchronisez votre dépôt local avec le distant :
    - Récupérez les dernières modifications.  
    - Placez-vous sur la branche locale develop et intégrez origin/develop dans celle-ci.  
    Vérifiez l’historique pour vous assurer que develop contient bien les commits de feature/login.
12- Toujours côté Eve, créez une nouvelle branche de fonctionnalité feature/register à partir de develop.  
    - Faites un commit (par exemple, un fichier register.md).  
    - Poussez feature/register sur le dépôt distant.
13- De retour sur Adam, récupérez la branche feature/register, créez une branche locale suivie de origin/feature/register, faites un commit supplémentaire sur cette branche, puis poussez vos modifications.
14- Sur GitHub, créez une pull request pour fusionner feature/register dans develop.  
    - Examinez l’historique, puis fusionnez la PR.  
    - Une fois la PR fusionnée, supprimez la branche distante feature/register depuis l’interface GitHub.
15- C’est le moment de préparer une version stable sur main.  
    - Sur GitHub, créez une pull request de develop vers main.  
    - Vérifiez les commits qui seront intégrés.  
    - Fusionnez la PR de develop dans main.
    - Mettez un reviewer
16- De retour sur Adam puis sur Eve, synchronisez votre dépôt local avec les branches distantes :
    - Récupérez les dernières informations.  
    - Placez-vous sur main puis intégrez origin/main dans votre main local.  
    - Faites de même pour develop si nécessaire.  
    Vérifiez que main et develop sont au même niveau ou que vous comprenez clairement leur différence si ce n’est pas le cas.
17- Une fois que toutes les fonctionnalités sont intégrées :
    - Supprimez les branches locales feature/login et feature/register sur Adam et Eve.  
    - Vérifiez que les branches distantes correspondantes n’existent plus (ou supprimez-les si ce n’est pas déjà fait).
18- Affichez une dernière fois l’historique en graphe avec l’option --all pour visualiser le flux de travail entre main, develop et les branches de fonctionnalités.  