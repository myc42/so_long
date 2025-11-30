🕹️ so_long : Le Petit Jeu 2D de 42

📝 Description du Projet

Le projet so_long est une introduction au développement graphique 2D à l'école 42. Le but est de créer un petit jeu de collection/évasion simple, où un joueur doit se déplacer sur une carte, collecter tous les objets, et atteindre la sortie.

C'est un exercice qui met en œuvre :

    Le parsing et la validation de fichiers (la carte du jeu, au format .ber).

    La manipulation de la MiniLibX pour l'affichage graphique et la gestion des événements.

    La gestion des événements clavier pour les mouvements.

    L'intégration de la Libft et de Printf personnalisés.

🧠 Pourquoi le nom "so_long" ?

Le nom est un jeu de mots. "So long!" signifie "au revoir" en anglais. D'après 42, il fait référence à la réputation du projet d'être un exercice long à réaliser.

✨ Aperçu du Jeu

    Objectif : Déplacer le personnage (P) pour ramasser tous les objets (C), puis atteindre la sortie (E).

<img src="Screencast from 07-31-2025 09_03_11 PM.gif" alt="Aperçu du jeu so_long" width="600" />

🗺️ Composants de la Carte

La carte du jeu (fichier .ber) est composée de caractères spécifiques :
Caractère	Description	Exigence de la Map
1	Mur (délimite le plateau)	La carte doit être entourée de murs.
0	Espace vide (sol)	
C	Collectible	Au moins un (1 ou plus).
E	Sortie	Exactement un (1). Accessible seulement si tous les C sont ramassés.
P	Position de départ du Joueur	Exactement un (1).
T	Ennemi (Optionnel / Bonus)	Si présent, il doit y avoir des règles de déplacement ou de collision.

🔑 Commandes du Joueur

Action	Touches (QWERTY)	Touches (AZERTY)
Haut	W	Z
Gauche	A	Q
Bas	S	S
Droite	D	D
Quitter	ESC ou la croix de la fenêtre	

(Note : J'ai ajouté une fonctionnalité bonus où l'ennemi se déplace avec les flèches du clavier.)

🛠️ Technologies & Contraintes

    Langage : C

    Librairie Graphique : MiniLibX (Bibliothèque simple fournie par 42)

    Compilation : make (utilise un Makefile standard)

    Contraintes Strictes :

        Aucune autre bibliothèque graphique externe (SDL, SFML, etc.) n'est autorisée.

        Utilisation de ma propre version de Libft et de ft_printf.

💡 Installation et Lancement

    Cloner le dépôt (avec l'utilisateur myc42) :
    Bash

git clone https://github.com/myc42/so_long.git
cd so_long

Pré-requis MiniLibX :

    Téléchargez la MiniLibX adaptée à votre système (Linux ou macOS) et placez-la dans un dossier nommé exactement minilibx à la racine du projet.

Compiler le jeu :
Bash

make

Lancer le jeu avec une carte (exemple) :
Bash

    ./so_long ressources/map/valid/test_map.ber

    ⚠️ Gestion des Erreurs : Le programme gère plusieurs cas d'erreurs (fichiers non valides, carte non rectangulaire, carte sans chemin valide, etc.) et s'arrête proprement dans ces situations.

👨‍💻 Auteur

<p align="center"> <a href="https://github.com/myc42"> <img src="https://avatars.githubusercontent.com/u/votre_id_github?v=4" width="80px" alt="Avatar GitHub myc42"/> </a> </p>

    Nom : [Votre Vrai Nom/Alias]

    GitHub : @myc42

    École : [École 42 / Autre]

🏆 Statut du Projet

Critère	Statut
Parsing Map	✅ Complété (vérification des murs, des composants, de la forme)
Map Jouable	✅ Complété (Vérification d'un chemin valide avec l'algorithme Flood Fill)
Affichage (MLX)	✅ Complété (Gestion des sprites et de la fenêtre)
Mouvements	✅ Complété (avec affichage du compteur de pas)
Gestion des Erreurs	✅ Complété
Fonctionnalité Bonus (Ennemi)	🚧 Implémenté
