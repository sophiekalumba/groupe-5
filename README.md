MEMBRES DU GROUPE
================

1. KATA MUSAMBU Delphine

# Système de pointage et production - Application console Java

## 📋 Contexte
Cette application Java console permet de gérer le suivi des opérateurs et des résultats de production (pièces conformes et rebuts) dans un environnement industriel. Elle permet d'enregistrer des opérateurs, de suivre leur production quotidienne, de calculer des indicateurs (taux de défaut) et de générer des rapports.

## 🚀 Fonctionnalités
- **Menu interactif** avec navigation
- **Gestion des opérateurs** (ajout, vérification)
- **Enregistrement de la production** avec validation
- **Affichage de la production du jour** avec totaux
- **Génération de rapports** journaliers (fichiers TXT)
- **Alertes** si taux de défaut > 5%
- **Validation complète** des entrées utilisateur

## 📁 Structure du projet

project-root/
│
├── src/ # Code source Java
│ ├── Main.java # Point d'entrée et menu
│ ├── OperatorManager.java # Gestion des opérateurs
│ ├── ProductionManager.java # Gestion de la production
│ ├── ReportGenerator.java # Génération de rapports
│ ├── FileUtils.java # Utilitaires fichiers
│ └── ValidationUtils.java # Validation des entrées
│
├── data/ # Données de l'application
│ ├── operators.txt # Liste des opérateurs
│ ├── production.csv # Historique de production
│ └── parts.txt # Catalogue des pièces (optionnel)
│
├── demo_data/ # Données de démonstration
├── README.md # Ce fichier
└── report_example.txt # Exemple de rapport généré

## ⚙️ Prérequis
- **Java SE 8+** (11 ou 17 recommandé)
- **Git** et un compte **GitHub**
- Environnement de développement (IntelliJ, Eclipse, VS Code, etc.)

## 🛠️ Installation et exécution

### 1. Cloner le dépôt
```bash
git clone https://github.com/votre-utilisateur/votre-projet.git
cd votre-projet

##Compiler et exécuter
##===================

cd src
javac *.java
java Main

operators.txt
=============
id;nom;poste
OP001;Jean Dupont;Assemblage
OP002;Marie Curie;Contrôle qualité

production.csv

date;operatorId;piece;qtyOK;qtyKO
2026-01-31;OP001;P001;100;2
2026-01-31;OP002;P002;150;1
parts.txt (optionnel)

P001;Pièce modèle A
P002;Pièce modèle B
🎮 Utilisation

==Menu principal :==

=== SYSTÈME DE POINTAGE & PRODUCTION ===
1. Ajouter un opérateur
2. Enregistrer une production
3. Afficher la production du jour
4. Générer un rapport du jour
5. Quitter
Choix : 
Fonctionnalités détaillées :
Ajouter un opérateur : Saisie de l'ID, nom et poste

Enregistrer production : Date, ID opérateur, pièce, quantités OK/KO

Afficher production : Totaux du jour avec détails par opérateur

Générer rapport : Crée un fichier report_YYYY-MM-DD.txt

Quitter : Ferme l'application

🧪 Tests manuels recommandés
Ajout d'opérateur avec ID existant → Refus

Production avec opérateur inconnu → Refus

qtyOK=0 et qtyKO=0 → Refus (évite division par zéro)

Taux de défaut > 5% → Affiche une alerte

Fichier rapport généré dans le dossier racine

🤝 Workflow GitHub
Branches : Chaque fonctionnalité dans feature/nom-module

Pull Requests : Obligatoires pour tout merge

Reviews : Au moins une review avant merge

Commits : Messages clairs et descriptifs

📈 Indicateurs calculés
Taux de défaut = (qtyKO / (qtyOK + qtyKO)) * 100

Total pièces produites = qtyOK + qtyKO

Efficacité = (qtyOK / (qtyOK + qtyKO)) * 100

🎯 Bonus implémentés (optionnel)
Classement des opérateurs par taux de défaut

Mode lecture seule

Validation des pièces via catalogue

📄 Licence
Projet éducatif - Institut Supérieur des Techniques Appliquées de Kolwezi

👥 Équipe
GROUPE 1 à 10 - Promotion de BAC II Informatique Industrielle

Date de remise : 06/02/2026