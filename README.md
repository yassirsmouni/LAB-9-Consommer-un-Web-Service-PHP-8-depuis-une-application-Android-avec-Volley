# LAB-9-Consommer-un-Web-Service-PHP-8-depuis-une-application-Android-avec-Volley
# 📱 GEtudiant - Application Android

## 🎯 Objectif

L'application permet d'ajouter un étudiant dans une base de données MySQL nommée **school**, table **Etudiant**, en envoyant les données vers un service PHP local exécuté avec **XAMPP**.

---

## 🔄 Parcours de l'application

L'utilisateur ouvre l'application **GEtudiant**.  
L'écran principal propose deux actions :

- Ajouter un étudiant
- Voir la liste des étudiants

---

## ➕ Ajout d’un étudiant

Dans l’écran d’ajout, l’utilisateur saisit :

- Nom
- Prénom
- Ville (via un Spinner)
- Sexe (via deux RadioButton)

---

## 🚀 Envoi des données

Lorsque l’utilisateur clique sur le bouton **ADD** :

- L’application vérifie que les champs obligatoires sont remplis
- Une requête **POST** est envoyée via **Volley** vers :

### 📦 Paramètres envoyés :

- nom
- prenom
- ville
- sexe

---

## 📩 Réponse du serveur

- La réponse est au format **JSON**
- Elle est parsée avec **Gson**
- Elle est affichée dans **Logcat**
- Un **Toast** confirme le succès ou affiche une erreur

---

## 📋 Liste des étudiants

L’utilisateur peut afficher la liste des étudiants :

- Une requête **GET** est envoyée vers :

- Les données reçues sont affichées dans une **ListView**

---

## 🧪 Test rapide

1. Lancer **XAMPP**
2. Démarrer :
   - Apache
   - MySQL
3. Vérifier le projet PHP dans :

4. Lancer l’application sur l’émulateur Android
5. Ajouter un étudiant :
   - Nom : DUPONT
   - Prénom : Sara
   - Ville : Casablanca
   - Sexe : femme
6. Cliquer sur **ADD**
7. Vérifier :
   - Logcat (TAG : REPONSE)
   - phpMyAdmin (table Etudiant)

---

## ⚠️ Remarque

Dans l’émulateur Android :

représente le **localhost de la machine PC**.

C’est pour cela que les URLs utilisent `10.0.2.2` au lieu de `localhost`.

---

## 📌 Conclusion

Cette application permet de comprendre la communication entre une application Android et un backend PHP/MySQL en utilisant Volley et JSON.
