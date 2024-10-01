# Création et publication de MkDocs/GitLab

**Date :** `01/10/2024`  
**Auteur :** `David Pereira`

---

## Sommaire
1. [Lancer la venv](#lancer-la-venv)
2. [Créé un nouveau projet mkdocs](#créé-un-nouveau-projet-mkdocs)
3. [Créé un projet GitLab](#créé-un-projet-gitlab)
4. [Cloner le git](#cloner-le-git)
5. [Publier le site sur GitLab](#publier-le-site-sur-gitlab)
6. [Conclusion](#conclusion)

---

## Lancer la venv
- Pour lancer la venv :
```source ~/venv/mkdocs-venv/bin/activate```

- Pour arrêter la venv :
```deactivate```

---

## Créé un nouveau projet mkdocs

- Pour créér un nouveau projet mkdocs :
```
mkdocs new nom-du-projet
cd nom-du-projet
```
- Pour lancer le serveur mkdocs :
```mkdocs serve```

- Pour construire le site :
```mkdocs build```

- Pour avoir material-mkdocs :
```pip install mkdocs mkdocs-material mkdocs-macros-plugin weasyprint mkdocs-with-pdf mkdocs-minify-plugin```

---

## Créé un projet GitLab

1. Aller sur [GitLab](https://gitlab.ictge.ch/)
2. Cliquer sur 'New Project' et créé le

## Cloner le git

```
cd le_dossier_mkdocs_cree
git init --initial-branch=main
git remote add origin git@gitlab.ictge.ch:david-prr2/le_projet_gitlab.git
git add .
git commit -m "Initial commit"
git push --set-upstream origin main
```

---

## Publier le site sur GitLab
1. Récupère ces fichiers :
|[.gitlab-ci.yml](https://github.com/ZodZodPOWA/MkDocs-Notes/blob/main/.gitlab-ci.yml)|
|[requirements.txt](https://github.com/ZodZodPOWA/MkDocs-Notes/blob/main/requirements.txt)|
2. Place les dans ton dossier mkdocs
3. Renomme 'gitlab-ci.yml' en ```.gitlab-ci.yml```
4. Push sur GitLab :
```
git add .
git commit -m "le commit"
git push
```
5. Aller sur votre projet GitLab
6. Dans la rubrique 'Deploy' et décocher 'Use unique domain', sauvegarder
7. Dans les paramètres général, mettre le projet en public

---

## Conclusion
Après ce tuto votre projet devrait être publié
