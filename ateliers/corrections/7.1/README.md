# Correction atelier 7.1 : méthodologie et organisation

## Partie I : reset

1. Q1 : reprenez le dépôt sur les sandwichs
2. Q2 : créez une nouvelle branche *feature/reset-soft* à partir de la branche *main*
```bash
# R2
git checkout main
git checkout -b feature/reset-soft
```
3. Q3 : supprimez les 5 derniers commits tout en conservant vos modifications, observez l'état de votre dépôt et effectuez un nouveau commit.
```bash
# R3
git reset --soft HEAD~5
git status
git commit -m "refactor: reset soft last 5 commits"
```
4. Q4 : créez une nouvelle branche *feature/reset-mixed* à partir de la branche *main*
```bash
# R4
git checkout main
git checkout -b feature/reset-mixed"
```
5. Q5 : supprimez les 5 derniers commits tout en conservant vos modifications, observez l'état de votre dépôt et effectuez un nouveau commit.
```bash
# R5
git reset --mixed HEAD~5
git status
git commit -am "refactor: reset mixed last 5 commits"
```
6. Q6 : créez une nouvelle branche *feature/reset-hard* à partir de la branche *main*
```bash
# R6
git checkout main
git checkout -b feature/reset-hard"
```
7. Q7 : supprimez les 5 derniers commits et toutes les modifications qui ont été effectuées, observez l'état de votre dépôt, effectuez un commit si nécessaire.
```bash
# R7
git reset --hard HEAD~5
git status
# faire le commit uniquement s'il y a des changements en cours non rattachés à un commit
git commit -am "refactor: reset hard last 5 commits" 
```

---

## Partie II : checkout

8. Q8 : depuis la branche *main*, utilisez la commande `git checkout [HASH_COMMIT]`, en remplaçant [HASH_COMMIT] par l'identifiant de commit de votre choix afin de pouvoir observer l'état de vos fichiers à un instant T
```bash
# R8
git checkout 02890a3
```
9. Q9 : quittez le mode observateur avec la commande `git checkout main`
```bash
# R9
git checkout main # Ici main est la branche courante, si vous êtes sur une autre branche que main, indiquez le nom de cette branche pour replacer le curseur HEAD à l'état actuel de votre branche
```