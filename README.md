## VBS Timer
### Éditeur : Video Bridge Solutions  
### ⬇️ Téléchargements (Releases) : 
https://github.com/VideoBridgeSolutions/VBS-Timer/releases


### 💡 Demandes de fonctionnalités : 
https://github.com/VideoBridgeSolutions/VBS-Timer/issues


# VBS Timer — Manuel utilisateur (FR)

* * *

## Présentation

**VBS Timer** est un **timer et une horloge de show** conçus pour **l'événementiel et la production audiovisuelle**  
(conférences, régie plateau, broadcast, retours orateurs, régies).

Il pilote une **sortie timer plein écran** pendant que l'opérateur prépare la suite dans un **aperçu séparé** : rien n'arrive au public sans un envoi explicite.

### Fonctions principales

*   Modes compte à rebours, chrono, horloge et « jusqu'à une heure » (fin à HH:mm)
    
*   **Préparation** et **LIVE** indépendants : modifier et tester sans toucher à ce qui est à l'antenne
    
*   Presets en un clic : Préparer / Charger / Lancer
    
*   Sorties LIVE : **NOIR / HORLOGE / TIMER**, avec fondus
    
*   Seuils d'alerte orange / rouge et comportement de fin configurable
    
*   Personnalisation visuelle complète (polices, couleurs, barres, habillages, animations), globale ou par preset
    
*   Sortie plein écran sur un second écran, sortie **NDI®**, fond vidéo (NDI ou carte de capture)
    
*   Pilotage **Stream Deck** en USB natif (sans logiciel Elgato), plugin Elgato et module Companion
    
*   Événements **OSC** sortants et API HTTP locale
    
*   Fichiers de show portables (`.vbstimer`)
    
*   Interface en français / anglais
    

**Objectif :** un timer fiable à l'antenne — rapide à mettre en place, impossible à modifier par erreur.

* * *

## Statut

VBS Timer 2.0 est actuellement publié en version **alpha**.

*   Validez-le sur vos propres machines (écrans, NDI, Stream Deck) avant de l'utiliser en production
    
*   Signalez tout problème dans **Issues** en indiquant le numéro de version exact
    

* * *

## Prérequis et environnement recommandé

### Système

*   Windows 10 ou Windows 11 (x64)
    
*   macOS (Apple Silicon ou Intel)
    
*   Aucun droit administrateur requis (installation par utilisateur sous Windows)
    

### Environnement recommandé

*   Un second écran ou un vidéoprojecteur pour la sortie timer
    
*   Optionnel : NDI® Runtime officiel (ndi.video) pour la sortie et l'entrée NDI
    
*   Optionnel : FFmpeg installé et accessible dans le PATH pour les cartes de capture
    
*   Optionnel : Elgato Stream Deck (Mini, MK.2 / Standard, XL, +, Neo)
    

* * *

## Installation

### Windows

1.  Téléchargez la dernière version `VBS_Timer_<version>_Windows_x64_Setup.exe` dans la section **Releases**
    
2.  Lancez l'installateur et suivez l'assistant
    
3.  VBS Timer est ajouté au menu Démarrer et au bureau
    

L'installateur n'est pas encore signé : Windows SmartScreen peut demander une confirmation (**Informations complémentaires → Exécuter quand même**).

### Installation silencieuse (optionnel)

`VBS_Timer_<version>_Windows_x64_Setup.exe /S`

### macOS

1.  Téléchargez la dernière version `VBS_Timer_<version>_macOS_<arch>.dmg` (`arm64` pour Apple Silicon, `x64` pour Intel)
    
2.  Ouvrez l'image et glissez **VBS Timer** dans **Applications**
    
3.  Premier lancement : l'application n'est pas encore notarisée. Si macOS la bloque, ouvrez **Réglages Système → Confidentialité et sécurité** puis cliquez sur **Ouvrir quand même**
    

### Désinstallation

*   Windows : **Paramètres → Applications → VBS Timer → Désinstaller**
    
*   macOS : supprimez **VBS Timer** du dossier Applications
    

Les projets et préférences sont stockés hors du dossier d'installation et sont conservés.

* * *

## Démarrage et principes de fonctionnement

### Démarrage

*   VBS Timer s'ouvre sur la fenêtre opérateur principale
    
*   La sortie LIVE démarre sur **HORLOGE** par défaut (réglable dans Paramètres → Général → Au démarrage)
    
*   Une seule instance peut tourner : relancer l'application ramène la fenêtre existante au premier plan
    

### Philosophie générale

*   **La préparation ne touche jamais au LIVE** : ce que vous modifiez reste en aperçu jusqu'à l'envoi
    
*   Le décompte continue quelle que soit la charge de l'interface, du NDI ou de l'édition
    
*   La fenêtre de sortie externe ne peut pas être fermée ou réduite par erreur
    
*   Chaque action LIVE tient en un clic ou une touche Stream Deck
    

* * *

## Fenêtre principale

La fenêtre est organisée en quatre zones :

*   **Presets** (gauche) : la bibliothèque de timers
    
*   **Préparation** (centre) : grand aperçu 16:9 où l'on prépare le timer suivant
    
*   **LIVE** (droite) : retour 16:9 de ce qui est à l'antenne, avec l'inspecteur du preset en dessous
    
*   **Régie LIVE** (bas) : transport, ajustements et choix de la sortie
    

La barre des paramètres est en haut : un clic sur un onglet l'ouvre, un nouveau clic le replie.

Les poignées entre les trois colonnes se déplacent à la souris pour redimensionner les panneaux. Un double-clic sur une poignée rétablit les largeurs par défaut.

* * *

## Presets

### Actions

*   **Clic** sur un preset : le prépare dans l'aperçu (LIVE inchangé)
    
*   **Charger** : arme le preset au LIVE à sa durée initiale, sans le démarrer
    
*   **▶** : lance immédiatement le preset au LIVE
    
*   **Dupliquer** : crée une copie
    

### Réglages du preset

Sélectionnez un preset, puis **✎ Modifier ce preset** dans le panneau de droite :

*   Nom et mode (Compte à rebours, Chrono, Horloge, Jusqu'à une heure)
    
*   Durée ou heure de fin
    
*   Format d'affichage (Global, Auto, HH:MM:SS, MM:SS)
    
*   Seuils d'alerte en secondes (orange / rouge)
    
*   Message de fin
    
*   À la fin : Continuer en +, Figer à 00:00, Passer au noir, Passer à l'horloge
    
*   Afficher en LIVE au lancement
    
*   Adresses OSC optionnelles envoyées au départ du preset au LIVE et à sa fin
    

Les modifications sont validées avec **Enregistrer** ou abandonnées avec **Annuler**.

* * *

## Préparation et LIVE

### Préparation

*   Choisissez un preset ou réglez un timer rapide (durée ou heure de fin)
    
*   Testez-le dans l'aperçu (lancer, pause, remise à zéro) : le LIVE n'est pas affecté
    
*   **ENVOYER EN LIVE** envoie la préparation à la sortie. Un timer déjà lancé en préparation garde son décompte
    

### Régie LIVE

*   **DÉMARRER / PAUSE / REPRENDRE** : démarre au LIVE le timer sélectionné ou chargé
    
*   **STOP** : arrête le timer LIVE et le remet à sa durée
    
*   **RESET** : remet le timer LIVE à sa durée
    
*   **−10 / −5 / −1 / +1 / +5 / +10** : ajustent le timer LIVE en minutes
    
*   **NOIR** : passe au noir ; un second appui revient à ce qui était diffusé avant (TIMER ou HORLOGE)
    
*   **HORLOGE / TIMER** : choisit ce qu'affiche la sortie. Le timer continue de tourner quand il est masqué
    

* * *

## Sorties

### Sortie écran

Paramètres → **Sortie écran** :

*   Choisissez l'écran (nom lu depuis le moniteur quand il est disponible)
    
*   Activez la sortie physique : le timer s'affiche en plein écran sur cet écran
    
*   L'écran principal ne peut pas servir de sortie, pour protéger la fenêtre opérateur
    

### Fondus

Paramètres → Général → **Fondu Noir / Timer / Horloge** (en secondes, `0` = coupe franche).

### NDI® et vidéo

Paramètres → **Vidéo / NDI** :

*   **Sortie NDI** : diffuse la composition LIVE (1280×720) sous un nom NDI configurable
    
*   **Entrée vidéo** : une source NDI ou une carte de capture affichée derrière le timer / l'horloge
    
*   Le NOIR reste toujours noir
    
*   Vidéo uniquement, sans audio dans cette version
    

NDI® est une marque déposée de Vizrt NDI AB. Le NDI Runtime s'installe séparément.

* * *

## Personnaliser l'affichage

Utilisez **Personnaliser Timer** ou **Personnaliser Horloge** :

*   Cliquez sur les chiffres, le nom ou la barre, puis déplacez-les ou redimensionnez-les avec les poignées
    
*   Guides magnétiques : centres, bords et marges de sécurité de 5 %
    
*   **Shift** : garder les proportions · **Alt** : depuis le centre · **Ctrl / Cmd** : sans aimantation
    
*   Polices, couleurs, couleurs d'alerte / critique / dépassement
    
*   Styles et animations de barre, habillages (Studio clock, Anneau, Bandeau, Disque, Jauge 270°, Viseur, Niveau plein écran, Halo, Colonnes VU)
    
*   Effets sur les chiffres, halo, clignotement en dépassement, flash à zéro
    

La personnalisation se fait dans l'aperçu : la sortie LIVE n'est pas modifiée pendant l'édition. Cliquez sur **Appliquer** pour valider le design.

### Style global ou par preset

*   Par défaut, tous les presets utilisent le style Timer global
    
*   Un preset peut avoir son propre style (**Personnalisé pour ce preset**)
    
*   **Copier vers un preset…** réutilise un design, **Rétablir le style global** le supprime
    

* * *

## Projets

Menu **Fichier** (macOS : barre de menus) :

*   **Nouveau projet** : charge les presets par défaut
    
*   **Ouvrir… / Enregistrer / Enregistrer sous…** : fichiers `.vbstimer`
    

Un projet contient les presets, les styles et les options d'affichage d'un show.  
Il ne contient **pas** les réglages du poste (écrans, NDI, OSC, Stream Deck, langue) : un fichier de show passe d'une machine à l'autre sans risque.  
Ouvrir un projet ne modifie jamais ce qui est à l'antenne.

* * *

## Stream Deck

### USB natif (recommandé)

Paramètres → **Stream Deck** :

*   Pilotage USB direct, sans logiciel Elgato (quittez l'application Elgato avant)
    
*   Modèles pris en charge : Mini, MK.2 / Standard, XL, +, Neo (touches uniquement)
    
*   Détection automatique du modèle connecté, luminosité réglable
    
*   5 pages par modèle, avec navigation par défaut sur chaque page : **PAGE ▶** en page 1, **PAGE ▶** et **HOME** en pages 2 à 5
    

### Éditeur de touches

*   Glissez les commandes et les presets (PLAY / LOAD) sur les touches
    
*   Libellé et couleur personnalisables par touche
    
*   Les touches **Feedback** affichent l'état du LIVE et de la préparation (lecture seule)
    
*   L'état est affiché sur les touches : en cours, chargé, masqué, NOIR / HORLOGE / TIMER
    

### Plugin Elgato (optionnel)

Paramètres → Stream Deck → **Elgato ▸ Installer / Mettre à jour**, puis redémarrez l'application Stream Deck (version 7.5 ou plus récente).

### Bitfocus Companion

Un module Companion (expérimental) est disponible, avec actions, presets et feedbacks.

* * *

## OSC

### OSC sortant

Paramètres → **Sortie OSC** :

*   Hôte, port (par défaut `8000`) et préfixe (par défaut `/vbs/timer`)
    
*   **Tester l'envoi** envoie `/vbs/timer/test ping`
    

### Messages (LIVE uniquement)

`/vbs/timer/output <black|clock|timer>`  
`/vbs/timer/preset <id> <nom>`  
`/vbs/timer/transport <start|paused|stopped|reset>`  
`/vbs/timer/remaining <secondes>`  
`/vbs/timer/phase <warning|critical>`  
`/vbs/timer/ended <id> <sortie>`

Chaque preset peut aussi envoyer sa propre adresse au départ au LIVE et à zéro.

### Bonnes pratiques

*   La préparation n'envoie jamais d'OSC : seul le LIVE en émet
    
*   L'envoi OSC ne peut jamais ralentir ni arrêter le timer
    

* * *

## API locale

VBS Timer expose une API HTTP **uniquement sur la machine locale** (`127.0.0.1:43994`), utilisée par le plugin Stream Deck, Companion et VBS Timeline.

`GET  http://127.0.0.1:43994/v1/state`  
`GET  http://127.0.0.1:43994/v1/workspace`  
`GET  http://127.0.0.1:43994/v1/presets`  
`POST http://127.0.0.1:43994/v1/command`

Exemple :

`curl -X POST http://127.0.0.1:43994/v1/command -H "Content-Type: application/json" -d '{"action":"toggle-black"}'`

Actions principales : `start`, `pause`, `toggle`, `stop`, `reset`, `add` (`seconds`), `black`, `toggle-black`, `clock`, `timer`, `toggle-timer-clock`, `select` / `arm-timer` / `preset` (`presetId`), `take`, `take-start`.

* * *

## Bonnes pratiques d'exploitation

*   Préparez et testez chaque timer en Préparation avant le show
    
*   Utilisez **Charger** pour armer l'orateur suivant, puis **DÉMARRER** au top
    
*   Laissez la sortie sur HORLOGE ou NOIR entre deux sessions
    
*   Enregistrez le show en projet `.vbstimer` et gardez-en une copie sur la machine de secours
    
*   Vérifiez les pages Stream Deck et la sortie écran avant l'ouverture des portes
    

* * *

## Dépannage

### Timer invisible sur l'écran de sortie

*   Vérifiez Paramètres → Sortie écran : bon écran choisi et sortie activée
    
*   L'écran principal ne peut pas servir de sortie
    
*   Vérifiez que le LIVE n'est pas sur NOIR ou HORLOGE
    

### Stream Deck non détecté (USB natif)

*   Quittez l'application Elgato Stream Deck
    
*   Vérifiez que le contrôle USB natif est activé dans Paramètres → Stream Deck
    
*   Débranchez puis rebranchez le Stream Deck
    

### NDI indisponible

*   Installez le NDI® Runtime officiel, puis relancez VBS Timer
    
*   Vérifiez le pare-feu sur les deux machines
    

### Carte de capture absente de la liste

*   Installez FFmpeg et vérifiez qu'il est accessible dans le PATH
    

### L'application ne démarre pas

*   Un journal est écrit dans `%LOCALAPPDATA%\VideoBridgeSolutions\VBS.Timer\Logs\startup.log` (Windows)
    
*   Le chemin du journal est aussi affiché dans les messages d'erreur au démarrage
    

* * *

## Support, mises à jour et distribution

*   Les mises à jour sont disponibles dans **GitHub Releases**
    
*   Utilisez toujours la version du manuel correspondant à celle de l'application
    
*   Pour une demande de support, fournissez :
    
    *   la version exacte (affichée dans la barre de titre)
        
    *   une capture de la fenêtre principale
        
    *   le contexte d'exploitation (système, écrans, NDI, modèle de Stream Deck)
        
    *   le fichier `startup.log` si nécessaire
        

**Le code source n'est pas public.**

© Video Bridge Solutions — VBS Timer

* * *
