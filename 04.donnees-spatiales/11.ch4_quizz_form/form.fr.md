---
title: Quizz
form:
    name: Quizz4
    fields:
        -
            name: name
            label: Nom
            placeholder: 'Votre nom :'
            autofocus: 'on'
            autocomplete: 'on'
            type: text
            validate:
                required: true
                message: 'Saisissez votre nom SVP.'
        -
            name: espace1
            type: spacer
        -
            name: attributs
            label: "Que sont les attributs des données ?"
            type: radio
            default: 
            options:
                geod: Des caractéristiques géodésiques
                style: Des caractéristiques de style d'affichage
                data: Des donnnées alphanumériques associées
            validate:
                required: true
                message: 'Choisissez une des propositions.'
        -
            name: espace2
            type: spacer
        -
            name: nom_raster
            label: "Quel est l'autre nom des données raster ?"
            type: radio
            default: 
            options:
                matricielles: Matricielles
                carrelees: Carrelées
                pixellisees: Pixellisées
            validate:
                required: true
                message: 'Choisissez un des noms proposés.'
        -
            name: espace3
            type: spacer
        -
            name: canaux_raster
            label: "Quels sont les canaux d'une image en couleurs naturelles ?"
            type: radio
            default: 
            options:
                noir_blanc: Noir et blanc
                rvb: Rouge, Vert, Bleu
                ir: Infra-rouge
            validate:
                required: true
                message: 'Choisissez une des propositions.'
        -
            name: espace4
            type: spacer
        -
            name: projection
            label: "Quelle est la propriété primordiale à régler lorsque l'on crée un nouveau projet dans QGIS ?"
            type: radio
            default: 
            options:
                couleur: La couleur par défaut de la sélection
                titre: Le titre du projet
                proj: Le système de référence spatiale (projection)
            validate:
                required: true
                message: 'Choisissez une des propositions.'
        -
            name: espace5
            type: spacer
        -
            name: qualite
            label: "Quels sont les points à vérifier sur la qualité des données ?"
            type: checkboxes
            options:
                origine: Origine
                precision: Précision
                homogeneite: Homogénéité
                age: Âge
                exhaustivite: Exhaustivité
                compatibilite: Compatibilité
                popularite: Popularité
            validate:
                required: true
                message: 'Choisissez toutes les propositions valables.'
        -
            name: espace6
            type: spacer
    buttons:
        -
            type: submit
            value: Envoyer
        -
            type: reset
            value: Effacer
    process:
        -
            message: 'Vos réponses au quizz sur les données spatiales.'
        -
            display: ch4_quizz

---

## Données spatiales : le quizz