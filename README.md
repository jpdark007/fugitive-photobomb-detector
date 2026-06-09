# 🕵️‍♂️ Où est Xavier ?

> Traquez qui vous voulez dans vos photos ! Cette app Flutter 100% locale scanne les visages en arrière-plan. Cherchez Xavier Dupont de Ligonnès ou ajoutez n'importe quelle autre photo de référence. Vos données ne quittent jamais votre téléphone. Une expérience à la "Où est Charlie".

---

## ✨ Fonctionnalités principales

* 🔒 **100% Local (Privacy First) :** Aucun backend, aucune API distante. Vos photos, vos modèles IA et vos résultats ne quittent **jamais** votre téléphone.
* 🎯 **Recherche sur mesure :** Fourni avec un cas d'usage par défaut (XDDL), mais vous pouvez importer **n'importe quel visage de référence** depuis votre galerie pour lancer un scan.
* ⚡ **Haute Performance :** Utilisation des *Dart Isolates* pour exécuter les calculs matriciels complexes en arrière-plan sans bloquer l'interface utilisateur.
* 🖼️ **Analyse de masse :** Parcours intelligent de votre galerie locale grâce au package `photo_manager`.

## 🛠 Stack Technique

* **Framework :** [Flutter](https://flutter.dev/) (Dart)
* **Détection faciale :** `google_mlkit_face_detection` (version On-Device) pour extraire les *bounding boxes* des visages, même en arrière-plan.
* **Reconnaissance & Embeddings :** `tflite_flutter`. Utilisation d'un modèle léger (ex: MobileFaceNet) pour générer des vecteurs faciaux et calculer la distance cosinus/euclidienne.
* **Accès Galerie :** `photo_manager`

---

## 🚀 Installation & Démarrage

### Prérequis
* Un appareil physique Android (recommandé) ou un émulateur.

###⚠️ Limites Connues (Known Issues)
La reconnaissance faciale embarquée a ses limites, surtout sur des photos de vacances :

Faux positifs : Les visages lointains, flous, ou mal éclairés (typiques des arrière-plans) génèrent des embeddings de moins bonne qualité. L'application risque de trouver des correspondances erronées.

Profils : Les modèles légers on-device ont beaucoup de mal à identifier les visages qui ne sont pas de face.

Temps de traitement : Scanner une galerie de 15 000 photos prend du temps. Laissez l'application tourner et surveillez la jauge de progression.

### ⚖️ Avertissement & Disclaimer
Ce projet est une expérimentation technique et éducative. Il n'est en aucun cas un outil professionnel d'investigation ou d'application de la loi. Les résultats de correspondances (matchs) fournis par l'intelligence artificielle embarquée sont indicatifs et sujets à une forte marge d'erreur.

En utilisant cette application, vous vous engagez à respecter les lois de votre pays concernant la vie privée et l'utilisation de données biométriques.

### Screenshots
![Screenshot 7](./images/screen7.spot_me.jpg)
![Screenshot 1](./images/screen1.spot_me.jpg)
![Screenshot 2](./images/screen2.spot_me.jpg)
![Screenshot 3](./images/screen3.spot_me.jpg)
![Screenshot 4](./images/screen4.spot_me.jpg)
![Screenshot 5](./images/screen5.spot_me.jpg)
![Screenshot 6](./images/screen6.spot_me.jpg)
