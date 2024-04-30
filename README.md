# Mini-projet 442 - Mialitiana ANDRIANARISON : Lecteur MP3

Le dépôt est accessible à l'adresse : https://github.com/msandrianarison/projet

## Objectif du projet : 
Emuler un lecteur mp3 sur le microcontrôleur STM32F746G : pouvoir écouter de la musique mp3 avec des écouteurs et avoir les contrôles basiques de n'importe quel baladeur mp3 : pause, stop, changement de musique, affichage du titre et contrôle du volume sonore.

## Pré-requis
- Télechargement de la librairie X-CUBE-AUDIO sur le site de st https://www.st.com/en/embedded-software/x-cube-audio.html
- Téléchargement de la version corrigée du MP3Player sur https://github.com/aroyer-qc/MP3-STM32F746G-DISCO.git
- Importation du projet MP3Player pour la carte STM32F7xx : Import -> General -> Import ac6 System Workbench for STM32 Project ->  Sélectionner le projet "MP3-STM32F746G-DISCO"
- Fusion du dossier dans le workspace avec le dossier dans ce dépôt (la version zip ne pouvant pas être importée sous format ac6, le projet ne sera pas bien converti par l'IDE sinon).

## Difficultés du projet 
Contrairement aux fichiers .wav, les fichiers mp3 ont subi une compression avec pertes, ce qui diminuent leurs tailles de fichiers, mais rend leurs lectures plus difficiles car on doit les décoder avant de les lire.
La bibliothèque X-CUBE-AUDIO fournit des fonctions (dans le fichier mp3process.c) pour décoder les données du fichier mp3 et pour gérer la lecture. L'acquisition des données peut-être résumé de la façon suivante :
- Initialisation des paramètres : fréquence d'échantillonnage, nombre de canaux et le débit binaire 
- Lecture des en-têtes
- Décodage des trames MP3 
- Détection du format de débit binaire variable (VBR)
- Calcul de la durée totale du flux
- Envoie des données PCM en sortie (format Pulse-code modulation)

## Amélioration possible
- Ajout d'un mode aléatoire
- Ajout d'une touche avance rapide / recul rapide
- Changement de la touche pause/play
