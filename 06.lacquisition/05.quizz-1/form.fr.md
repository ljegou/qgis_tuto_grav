---
title: Quizz
form:
    name: 'Quizz acquisition'
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
            name: gps
            label: 'Que ne permet pas le GPS ?'
            type: radio
            default: null
            options:
                hauteur: 'De mesurer la hauteur d''un point'
                chrono: 'De chronométrer le temps entre deux points de mesure'
                couleur: 'De capturer la couleur au sol du point de mesure'
            validate:
                required: true
                message: 'Choisissez une des propositions.'
        -
            name: espace2
            type: spacer
        -
            name: teledetection
            label: 'Qu''indique la longueur d''onde d''un canal d''une image satellite ?'
            type: radio
            default: null
            options:
                taille: 'La taille de l''image au sol'
                echelle: 'L''échelle de l''image'
                valeur: 'Le type de valeurs mesurées par le capteur : couleurs ou rayonnement'
            validate:
                required: true
                message: 'Choisissez un des propositions.'
        -
            name: espace3
            type: spacer
        -
            name: geocodage
            label: 'Que permet le géocodage ?'
            type: radio
            default: null
            options:
                adresses: 'De convertir des adresses au format texte en des coordonnées géographiques'
                calage: 'De caler une image pour lui donner une position et des dimensions géographiques'
                rectification: 'De rectifier une image pour en corriger les déformations'
            validate:
                required: true
                message: 'Choisissez une des propositions.'
        -
            name: espace4
            type: spacer
        -
            name: calage
            label: 'A quoi faut-il faire attention lorsque l''on choisit des points de référence pour caler une image ?'
            type: radio
            default: null
            options:
                repartition: 'La répartition des points sur la surface de l''image'
                alignement: 'L''alignement des points entre eux'
                positionnement: 'Le positionnement des points sur les bornes de référence de l''IGN'
            validate:
                required: true
                message: 'Choisissez une des propositions.'
        -
            name: espace5
            type: spacer
        -
            name: londes
            label: 'A quoi peuvent servir les acquisitions d''images satellites dans des longueurs d''onde non visibles ?'
            type: checkboxes
            options:
                vege: 'A estimer l''activité végétale'
                precision: 'A augmenter la résolution de l''image'
                meteo: 'A mesurer la pluviométrie'
                relief: 'A mesurer le relief d''une région        '
                suivre: 'A suivre des moyens de transport'
                bathy: 'A estimer la profondeur des océans'
            validate:
                required: true
                message: 'Choisissez <i>toutes</i> les propositions valables.'
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
            message: 'Vos réponses au quizz sur l''acquisition n°1.'
        -
            display: acq1_quizz
---

## L'acquisition : quizz