# Vigilo
Embedded systems project INFO2055-1

1. Contexte du projet

Ce projet s'inscrit dans le cadre d'un cours sur les systèmes embarqués. Il vise à concevoir et implémenter un système combinant matériel et logiciel à l’aide d’un microcontrôleur PIC16F, des capteurs et des actionneurs, tout en respectant des contraintes temps réel à l’aide des interruptions.

2. Organisation du projet

Séances d'exercices : Introduction à l'électronique appliquée, programmation embarquée et architecture logicielle.
Travaux pratiques : Prise en main du PIC16F, écriture de code pour des périphériques.
Projet principal : Conception et implémentation d'un système embarqué intégrant plusieurs tâches simultanées.

3. Exigences techniques

Utilisation d’un microcontrôleur PIC16F.
Intégration d'au moins un capteur et un actionneur.
Gestion de tâches en temps réel via des interruptions.
Conception d’une architecture logicielle optimisée pour les contraintes embarquées.
Documenter et justifier les choix matériels et logiciels.

4. Livrables et évaluation

Documents techniques : Rapports décrivant l’architecture matérielle et logicielle, validation des capteurs/actionneurs et tests réalisés.
Démonstration finale : Présentation du projet fonctionnel.
Évaluation : Qualité du développement matériel/logiciel, gestion des contraintes temps réel, capacité d’analyse et de résolution de problèmes.

5. Exemples de projets précédents

Pince automatisée pour drone : Détection et prise d’objets en vol.
Boîte aux lettres automatisée : Détection et stockage sécurisé du courrier.
Robot micro-mouse : Navigation autonome dans un labyrinthe.

6. Conseils et avertissements

Ne pas sous-estimer le temps d’apprentissage de l’électronique embarquée.
Expérimenter et documenter les erreurs plutôt que d’essayer de les cacher.
Éviter le plagiat (utilisation directe de tutoriels existants).
Respecter les délais de remise sous peine de pénalités.


🚗 Projet de Voiture Autonome – PIC16F1789

📌 Objectif du projet

Ce projet vise à concevoir et programmer une voiture autonome capable de détecter et d’éviter des obstacles en ajustant sa trajectoire grâce à un microcontrôleur PIC16F1789. Pour cela, la voiture intègre plusieurs capteurs, actionneurs et un système de gestion temps réel basé sur des interruptions.

🛠️ Matériel utilisé

Microcontrôleur : 
  PIC16F1789

Actionneurs :
  2 moteurs DC 12V
  2 servomoteurs (direction et frein)
  1 contrôleur de moteur en pont
  
Capteurs :
  2 capteurs à ultrasons (détection avant/arrière)
  2 capteurs infrarouges (détection latérale)
  1 émetteur et 1 récepteur infrarouge
  
Alimentation : 
  4 piles 1.5V (6V total) + régulateur de tension

🖥️ Répartition du travail

Le projet est divisé en plusieurs tâches logicielles, chacune ayant une priorité définie :

1️⃣ Contrôle des moteurs (τ1) - Priorité haute

Gestion des moteurs DC via PWM pour déplacer la voiture.
Ajustement de la direction en fonction des obstacles détectés.

2️⃣ Acquisition des données capteurs (τ2) - Interruption prioritaire

Mesure des distances avec les capteurs ultrasons.
Détection des obstacles latéraux avec les capteurs infrarouges.
Vérification des conditions de stationnement.

3️⃣ Contrôle des servomoteurs (τ3) - Priorité moyenne

Ajustement de l’angle des roues pour changer de direction.
Activation du frein via un servomoteur.

4️⃣ Acquisition des données moteurs (τ4) - Priorité basse

Surveillance de la vitesse et de la distance parcourue.
Utilisation d’un convertisseur ADC pour récupérer les signaux analogiques.

⚡ Gestion du Temps Réel

Utilisation d’un RTOS (Real-Time Operating System) pour assurer un ordonnancement optimal des tâches.
Interruption sur l’acquisition des capteurs pour garantir une détection immédiate des obstacles.
Mécanisme de préemption pour donner la priorité à la sécurité et aux corrections de trajectoire.

📌 Conclusion

Ce projet est une application pratique des systèmes embarqués et de la programmation bas niveau en assembleur sur un PIC16F1789. Il combine gestion matérielle, contrôle moteur et traitement en temps réel pour réaliser un système autonome efficace.
