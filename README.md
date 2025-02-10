# Smart Waste Management

## Description
Smart Waste Management est une solution connectée permettant de surveiller le niveau de remplissage des poubelles en temps réel grâce à des capteurs. Elle vise à optimiser la gestion des déchets, notamment dans les restaurants, en réduisant le gaspillage et en améliorant les collectes.

## Technologies utilisées
- **Microcontrôleur** : ESP32 (programmation en C++ via Arduino IDE)
- **Capteurs** :
  - Capteur de poids **KIT0176**
  - Capteur de distance à ultrasons **HC-SR04**
- **Backend** : Firebase (stockage des données)
- **Frontend** : Angular (interface utilisateur)

## Fonctionnalités
- Mesure en temps réel du niveau de remplissage des poubelles
- Envoi des données vers Firebase
- Visualisation des données via une interface web Angular
- Notifications en cas de dépassement du seuil de remplissage

## Installation et exécution
### 1. Configuration du microcontrôleur
1. Installer **Arduino IDE** et ajouter les bibliothèques ESP32.
2. Installer les bibliothèques nécessaires :
   ```cpp
   #include <WiFi.h>
   #include <FirebaseESP32.h>
   #include <HX711.h> // Pour le capteur de poids
   #include <NewPing.h> // Pour le capteur à ultrasons
   ```
3. Flasher le code sur l’ESP32.

### 2. Déploiement de l’interface Angular
1. Installer les dépendances :
   ```bash
   npm install
   ```
2. Lancer le serveur de développement :
   ```bash
   ng serve
   ```
   Accéder à l’interface via `http://localhost:4200/`.

## Schéma de câblage
### Connexions du capteur de poids (KIT0176) avec l’ESP32
- **VCC** → 3V
- **SIG** → GPIO 4
- **GND** → GND

### Connexions du capteur de distance à ultrasons (HC-SR04) avec l’ESP32
- **VCC** → 5V
- **Trig** → GPIO 21
- **Echo** → GPIO 22
- **GND** → GND

## Problèmes rencontrés
- Adaptation aux contraintes matérielles et calibrage des capteurs.
- Ajustements constants de l’application Angular en fonction des tests.

## Auteur
- **Manal Herradi**
