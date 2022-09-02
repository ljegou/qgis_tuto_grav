---
title: Quizz
form:
    name: 'Quizz mise en forme'
    fields:
        -
            name: name
            label: 'Nom ou pseudo'
            placeholder: 'Votre nom ou pseudo :'
            autofocus: 'on'
            autocomplete: 'on'
            type: text
            validate:
                required: true
                message: 'Saisissez votre nom ou pseudo SVP.'
        -
            name: espace1
            type: spacer
        -
            name: efficacite
            label: 'Qu''est-ce qu''une carte thématique efficace ?'
            type: radio
            default: null
            options:
                rapidement: 'Une carte qui transmet rapidement son information'
                completement: 'Une carte qui transmet complètement l''information'
                clarte: 'Une carte qui permet au lecteur de se faire une idée juste et claire'
            validate:
                required: true
                message: 'Choisissez une des propositions.'
        -
            name: espace2
            type: spacer
        -
            name: representation
            label: 'Quelle serait le bon type de représentation pour le nombre d''habitants d''une région par communes ?'
            type: radio
            default: null
            options:
                symboles: 'Des symboles à la surface proportionnelle aux populations des communes'
                plages: 'Des plages de couleurs dont l''intensité est proportionnelle aux populations des communes'
                secteurs: 'Des secteurs dont l''angle est proportionnel à la population totale de la région'
            validate:
                required: true
                message: 'Choisissez un des propositions.'
        -
            name: espace3
            type: spacer
        -
            name: mep
            label: 'Quels sont les éléments indispensables à toute planche cartographique ?'
            type: checkboxes
            options:
                Carte: Carte
                Légende: Légende
                Échelle: Échelle
                Titre: Titre
                Sources: Sources
                Auteur: Auteur
                Nord: 'Flèche de nord'
            validate:
                required: true
                message: 'Choisissez toutes les propositions valables.'
        -
            name: espace4
            type: spacer
        -
            name: classification
            label: 'Pourquoi la classification d''une variable est-elle importante pour représenter une variable quantitative continue ?'
            type: radio
            default: null
            options:
                a: 'Pour que les classes produites soient équilibrées en taille'
                b: 'Pour que les classes produites soient représentatives des fréquences'
                c: 'Pour que les classes produites soient équilibrées en surface de la carte finale'
            validate:
                required: true
                message: 'Choisissez une des propositions.'
        -
            name: espace5
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
            message: 'Vos réponses au quizz sur la mise en forme.'
        -
            display: mef1_quizz
---

## La mise en forme : quizz