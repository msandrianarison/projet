# Mini-projet 442 - Mialitiana ANDRIANARISON : Lecteur MP3

## Pré-requis
- Télechargement de la librairie X-CUBE-AUDIO sur le site de st https://www.st.com/en/embedded-software/x-cube-audio.html
- Importation du projet MP3Player pour la carte STM32F7xx : Import -> General -> Import ac6 System Workbench for STM32 Project ->  Sélectionner le projet "MP3-STM32F746G-DISCO
- Fusion du dossier dans le workspace avec le dossier dans ce dépôt (la version zip ne pouvant pas être importée sous format ac6, le projet ne sera pas bien converti par l'IDE sinon).

## Fichiers principaux utilisés par la librairie 
  - Audio_MP3/Src/coders.c               Audio encoders/decoders abstraction layer
  - Audio_MP3/Src/fwkmempool.c           Audio framework memory pool tools
  - Audio_MP3/Src/main.c                 Main program
  - Audio_MP3/Src/mp3process.c           MP3 processing layer
  - Audio_MP3/Src/player.c               Audio MP3 file player (or WAV)
  - Audio_MP3/Src/stm32f7xx_it.c         Interrupt handlers
  - Audio_MP3/Src/system_stm32f7xx.c     STM32F4xx system source file
  - Audio_MP3/Src/usbh_conf.c            Board support package for the USB host library 	
  - Audio_MP3/Src/wavprocess.c           WAV processing layer
  - Audio_MP3/Inc/coders.h               Audio encoders/decoders abstraction layer header file
  - Audio_MP3/Inc/ffconf.h               FAT file system module configuration file  
  - Audio_MP3/Inc/fwkmempool.h           Audio framework memory pool header file  
  - Audio_MP3/Inc/main.h                 Main program header file
  - Audio_MP3/Inc/mp3process.c           MP3 processing layer header file  
  - Audio_MP3/Inc/player.h               Audio play header file  
  - Audio_MP3/Inc/stm32f7xx_hal_conf.h   HAL configuration file
  - Audio_MP3/Inc/stm32f7xx_it.h         Interrupt handlers header file
  - Audio_MP3/Inc/usbh_conf.h            USB driver Configuration file


  - Audio_MP3/Inc/wavprocess.h         WAV processing layer header file
