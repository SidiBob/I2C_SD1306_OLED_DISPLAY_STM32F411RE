# Projet de Contrôle d'un Écran OLED SSD1306 avec STM32F411RE via I2C

Ce projet est une démonstration des capacités de la carte de développement STM32F411RE pour contrôler un écran OLED basé sur le pilote SSD1306 en utilisant la communication I2C.

Le code est développé avec l'environnement de développement STM32CubeIDE.

## Aperçu

Le programme principal (`main.c`) initialise le microcontrôleur et l'écran OLED, puis exécute une série de démonstrations graphiques :
1.  Affiche les chaînes de caractères "MICROPETA" et "BY NIZAR".
2.  Fait défiler l'affichage vers la droite, puis vers la gauche.
3.  Efface l'écran et affiche le nombre "2024".
4.  Dessine diverses formes géométriques : une ligne, un rectangle, un triangle et un cercle.

## Matériel Requis

*   Une carte de développement STM32 (par exemple, NUCLEO-F411RE).
*   Un écran OLED 128x64 pixels avec pilote SSD1306 et interface I2C.
*   Des câbles de connexion (jumper wires) pour relier l'écran à la carte STM32.

### Connexions

Connectez l'écran OLED à la carte STM32F411RE en utilisant les broches I2C. Vous pouvez vérifier les broches exactes dans le fichier de configuration STM32CubeMX (`.ioc`). Typiquement, pour l'I2C1 :
*   **SCL :** `PB8`
*   **SDA :** `PB9`
*   **VCC :** `5V` ou `3.3V` (selon l'écran)
*   **GND :** `GND`

## Logiciels Requis

*   [**STM32CubeIDE**](https://www.st.com/en/development-tools/stm32cubeide.html)

## Comment Utiliser

1.  **Clonez ou téléchargez** ce dépôt.
2.  **Ouvrez STM32CubeIDE** et importez le projet via `File > Import > General > Existing Projects into Workspace`.
3.  **Sélectionnez le répertoire racine** du projet (`I2C_SSD1306`).
4.  **Compilez le projet** en cliquant sur l'icône en forme de marteau (Build).
5.  **Téléversez le programme** sur votre carte STM32 en cliquant sur l'icône de lecture (Run).

## Structure du Projet

*   `I2C_SSD1306/Core/Src/main.c` : Le fichier principal contenant la logique de la démonstration.
*   `I2C_SSD1306/Core/Inc/ssd1306.h` : Fichier d'en-tête pour le pilote de l'écran SSD1306.
*   `I2C_SSD1306/Core/Src/ssd1306.c` : Implémentation du pilote de l'écran.
*   `I2C_SSD1306/Core/Inc/fonts.h` : Fichier d'en-tête pour les polices de caractères.
*   `I2C_SSD1306/Core/Src/fonts.c` : Implémentation des polices de caractères.
*   `I2C_SSD1306/I2C_SSD1306.ioc` : Fichier de configuration STM32CubeMX pour le projet. Vous pouvez l'ouvrir pour visualiser la configuration des broches et des périphériques.
