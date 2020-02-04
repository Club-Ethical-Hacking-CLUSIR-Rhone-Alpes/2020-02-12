# Club Ethical Hacking - CLUSIR-Rhone-Alpes

## 2020-02-12

### Installation

1. installer `docker` et `docker-compose`:
    - https://docs.docker.com/install
    - https://docs.docker.com/compose/install/
2. cloner ce dépôt:
    - `git clone https://github.com/Club-Ethical-Hacking-CLUSIR-Rhone-Alpes/2020-02-12.git`
3. rendez-vous dans le répertoire du projet, puis dans `challenge/`
4. création des challenges:
    - `chmod u+x start_level`
    - `docker-compose build -q`
5. démarrage des challenges:
    - `docker-compose up -d`
6. démarrage d'un niveau:
    - `./start_level X` , où X est le numéro du niveau (1 à 10)
    - utilisez levelX comme mot de passe, où X est le numéro du niveau (1 à 10)

> `docker-compose down` OU `ctrl+c` pour arrêter le challenge

---

### Objectifs

Vous devez réussir à passer “root” sur chacun des 10 challenges.

Dans le fichier *“/root/flag”* se trouve un code qui permet de valider le
challenge.

Les challenges sont répartis par niveaux de difficultés (10).

### Outils & Cheatsheet

- https://gtfobins.github.io/
- https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Linux%20-%20Privilege%20Escalation.md
