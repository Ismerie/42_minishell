# 42_minishell

42_minishell est un projet de groupe de l'école 42 dans lequel nous devons créer un **programme shel**l basé sur Bash en C.  
Il implémente **les pipes** et **les redirections**, ainsi que **les variables d'environnement** et **les builtins commandes  `cd`, `echo`, `env`, `exit`, `export`, `pwd` and `unset`**.  
Ce projet a été réalisé avec [@ThibautCharpentier](https://github.com/ThibautCharpentier)

## 📋 Fonctionnalités

42_minshell prend en charge :
* Historique des commandes (flèche haut et bas)
* Exécutables système disponibles depuis l'environnement (`ls`, `cat`, `grep`, etc.)
* Exécutables locaux (`./minishell`)
* Pipe `|` qui redirige la sortie d'une commande vers l'entrée de la suivante
* Redirections :
  * `>` redirige la sortie
  * `>>` redirige la sortie en mode append
  * `<` redirige l'entrée
  * `<< DELIMITER` affiche un nouveau prompt, lit les entrées de l'utilisateur jusqu'à atteindre `DELIMITER`, redirige l'entrée de l'utilisateur vers l'entrée de commande
* Variables d'environnement (cad `$USER` ou `$VAR`) qui s'étendent à leurs valeurs
  * `$?` se développe jusqu'à l'état de sortie du pipeline de premier plan exécuté le plus récemment.
* Signaux du clavier :
  * `ctrl-c` affiche une nouvelle ligne prompt
  * `ctrl-d` quitte minishell
  * `ctrl-\` ne fait rien

Notre shell doit implémenter les commandes builtins suivantes :

| Commande  | Option                   | Action                                              |
| -----     | ------------------------ | --------------------------------------------------- |
| `echo`    | -n                       | Affiche les arguments passés sur la sortie standard |
| `cd`      | chemin relatif et absolu | Modifie le répertoire de travail actuel             |
| `pwd`     |                          | Affiche le répertoire courant                       |
| `export`  |                          | Exporte une variable d'environnement                |
| `unset`   |                          | Supprime une variable d'environnement               |
| `env`     |                          | Liste toutes les variables d'environnement          |
| `exit`    |                          | Sort du processus courant                           |

Cependant 42_minishell ne prend pas en charge `\`, `;`, `&&`, et `||`.

## 🛠️ Usage

Utilisez la commande ```make``` pour compiler puis exécutez avec : 
```
./minishell
```
***
