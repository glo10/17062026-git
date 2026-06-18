
# Résolution d'un conflit

## Contexte

1. Un fichier qui évolue dans une branche par exemple main
- On a fait un commit associé à ce changement
2. Le même fichier évolue également dans une autre branche par exemple feature/user
- On a fait un commit associé à ce changement
3. On fait un merge pour fusionner le travail de la branche feature/user dans main
4. On aura un conflit à résoudre car git ne sait pas quelle version garder entre ce qui vient de feature/user et ce qui est présent dans main
- Git nous place automatiquement dans une branche temporaire main|MERGING
5. Il faut choisir la bonne version du fichier (en gardant l'une de 2 versions ou une résultante et en supprimmant les marqueurs du conflit >>>HEAD, ===, <<<<)
6. Faire un commit
7. Git nous placera à nouveau sur la branche main et on a résolu le conflit
