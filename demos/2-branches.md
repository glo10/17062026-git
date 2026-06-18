# Branches

## Liste des branches

```bash
git branch
```
- * devant le nom d'une branche indique la branche courante

## Créer une branche

```bash
git branch feature/user
```
- On crée la nouvelle branche mais on reste toujours sur la branche courante (la branche source qui dévrait normalement être main)

## Créer et se placer sur la nouvelle

```bash
git checkout -b feature/product
```
- git branch affichera l'étoile (*) devant feature/product

## Supprimer une branche

```bash
git branch -d feature/product
```

- La suppression se fait uniquement si le merge a été fait avec main ou s'il n'y a pas eu de commit et des modifications
- Pour forcer la suppression malgré les modificationq effectuées sur cette branche, c'est l'option -D (attention perte du travail effectué dans cette branche, les fichiers, les dossiers et les commits).

```bash
git branch -D feature/product
```