# Correction atelier 5.1 : gestion des branches

## Partie I : changement et fusion des branches sans conflit

1. Q1 : créez une nouvelle branche *feature/pokebowl* à partir de la branche *main* et placez-vous dessus à l'aide de la commande `git checkout -b feature/pokebowl`
```bash
# R2
git checkout -b feature/pokebowl
```
- Assurez-vous au préalable que votre *Working directory* est propre avant de créer la nouvelle branche. S'il n'est pas clean, effectuez un commit ou effectuez la commande `git stash` pour mettre de côté les modifications en cours

2. Q2 : créez un nouveau fichier *pokebowl.md* et listez les ingrédients d'un pokebowl
- R2 : cf [pokebowl.md](./pokebowl.md)
3. Q3 : Effectuez un commit
```bash
# R3
git add pokebowl.md
git commit -m "feat: add pokebowl.md"
```
4. Q4 : créez une nouvelle branche *feature/salad* à partir de *main*
```bash
# R4
git checkout main
git checkout -b feature/salad
```
5. Q5 : créez un nouveau fichier *salad.md* et ajoutez une liste d'ingrédients pour une salade
- R5 : cf [salad.md](./salad.md)
6. Q6 : effectuez un commit
```bash
# R6
git add salad.md
git commit -m "feat: add salad.md"
```
7. Q7 : replacez-vous dans la branche *main*, fusionnez la branche *feature/pokebowl* dans *main* à l'aide de la commande `git merge feature/pokebowl`
```bash
# R7
git checkout main
git merge feature/pokebowl'
```
8. Q8 : fusionnez également la branche *feature/salad* dans *main*
```bash
# R8
git merge feature/salad
```

---

## Partie II : changement et fusion des branches avec les conflits

9. Q9 : créez une nouvelle branche *feature/vegan-pizza* à partir de *main*
```bash
# R9
git checkout main # Pas nécessairement car normalement, vous êtes déjà sur la branche main
git checkout -b feature/vegan-pizza
```
10. Q10 : créez un nouveau fichier *pizza.md* et ajoutez les ingrédients d'une pizza vegan
- R10 : cf [pizza.md](pizza.md)
11. Q11 : effectuez un commit
```bash
# R11
git add pizza.md
git commit -m "feat: add pizza.md"
```
12. Q12 : créez une nouvelle branche *feature/italian-pizza* à partir de *main*
```bash
# R12
git checkout main
git checkout -b feature/italian-pizza
```
13. Q13 : créez un nouveau fichier *pizza.md*, ajoutez les ingrédients d'une pizza italienne et effectuez un commit
- [cf. pizza.md](./pizza.md)
```bash
# R13
git add pizza.md
git commit -m "feat: add italian pizza"
```
14. Q14 : fusionnez la branche *feature/vegan-pizza* dans *main*
```bash
# R14
git checkout main
git merge feature/vegan-pizza
```
15. Q15 : fusionnez la branche *feature/italian-pizza* dans *main* et résolvez le conflit en finissant avec un commit de résolution de conflit
```bash
# R15
git merge feature/italian-pizza
```
- Pour résoudre le conflit, retirez les marqueurs de Git *<<<<,>>>>,===*, choisissez une de deux versions ou combiner les deux, effectuez un commit.
- Lorsqu'il y a un conflit, vous êtes sur une branche temporaire, après le commit vous revenez sur la branche de destination ici *main*
16. Q16 : envoyez la branche *main* vers le dépôt distant
```bash
# R16
git push
```
17. Q17 : affichez l'historique graphique de votre dépôt
```bash
# R17
git log --oneline
```
18. Q18 : supprimez les branches *feature/** en local

```bash
# R18
# ou option -D à la place -d pour supprimer sans avertissement sur la fusion des modifications apportées dans cette branche vers la branche principale main
git branch -d feature/italian-pizza
git branch -d feature/vegan-pizza
git branch -d feature/salad
git branch -D feature/pokebowl
```
---

## Partie III : fetch

19. Q19 : créez une nouvelle branche sur GitHub, *feature/drinks* à partir de *main*
- R : [vidéo création de branche depuis Github](../videos/create_branch.mp4)
20. Q20 : récupérez en locale la nouvelle branche à l'aide de la commande `git fetch origin`
```bash
# R20
git fetch origin
git checkout feature/drinks
```
21. Q21 : créez un fichier *drinks.md* et ajoutez une liste de boissons
- R21 : [cf. drinks](./drinks.md)
22. Q22 : effectuez un commit et envoyez les modifications de cette branche en ligne sur GitHub.
```bash
# R22
git add drinks.md
git commit -m "feat: add drinks"
git push
```

