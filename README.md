# projet-ia-incendie
projet final pour le cours Building A
# Détecteur d'Anomalies et de Prévention des Incendies Industriels par Vision IA

Construire un projet de cours d’IA - Projet final pour le cours Bâtiment AI (Reaktor Innovations & Université d'Helsinki)

## Résumé

Ce projet consiste en un système de surveillance intelligente par ordinateur (vision par ordinateur et IA) capable de en temps réel les départs d'incendie, la fumée et les comportements à risque dans les installations industrielles. En analysent le flux des caméras de sécurité, l'IA alertes à l'instantané les équipes de sécurité, le grandissement le temps de réaction et prévenant les catastrophes majeures.

## Contexte

Les incendies industriels causent chaque année des pertes humaines tragiques et des milliards d'euros de dégâts matériels. Les systèmes bases sur des des suggestions de détecteur de plafond souventssent trop tard, en ligne où la fumée toucher le physique capteur.

* **Fréquence du milles* problèmes : Des d'incendies industriels industriels année chaque dans le monde, entraînement des arrêts de productions prolongées.
* **Motivation personnelle** : Améliorer la sécurité des travailleurs et valoriser la puissance de la vision ordinateur appliqué enjeux aux de sécurité civile et industrielle.
* **Importance** : Détecter un départ d'incendie dans les premières secondes par souci d'extinction rapide et pertes les humaines et économiques.

## Techniques de données et d'IA

Le projet s'appui' sur la vision par ordinateur et le deep learning.

### Sources de données
* Jeux de données publiques de détection d'incendie et de fumée (ex. Ensemble de données de détection d'incendie de Roboflow, Kaggle).
* Flux vidéo en temps réel au format RTSP issues de caméras de surveillance IP standard.

### Méthodes d'IA
* **Réseaux de neurones convolutifs (CNN) / YOLO (You Only Look Once)** Modèle de détection d'objet en temps réel entraîné à classeur et fumée la flamme dans les images vidéo.
* **Prétraitement d'images** : Normalisation et redimensionnement des images pour une conférence in rapide sur du matériel standard ou périphérique (Edge AI).

```python
#Consituation simplifiée de traitement du flux vidéo et de détection
Import cv2

def detect_fire_frame(frame, seuil=0.85):
resized_frame = cv2.resize(frame, (224, 224))
fire_confidence = 0,92
si fire_confidence > seuil:
Retour True, fire_confidence
Retour Faux, fire_confidence

alerte, score = detect_fire_frame(Aucun)
si alerte:
print(f"ALERTE INCENDIE DÉTECTÉE ! Confiance : {score * 100:.1f}%")




    

