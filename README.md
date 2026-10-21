# OUBAYGESTION - Gestion Commerciale, Stocks, Caisse & Gouvernance d'Entreprise 📊

Application SaaS complète, multi-rôles et modulaire, spécialement conçue pour les commerces de gros et de détail, quincailleries, distributeurs et points de vente.

---

## 🔐 Comptes Utilisateurs & Profils de Démonstration

L'application intègre un système d'authentification et de gestion des rôles :

| Profil / Rôle | Email de connexion | Mot de passe | Permissions & Périmètre |
|---|---|---|---|
| **Directeur Général / Gérant** | `bassingaobed6.com` | `Obed@123` | Accès total : Direction, P&L, validation de clôture, paramétrage, gestion des équipes |
| **Caissière Principale** | `caisse@boutique.com` | `caisse123` | Saisie des ventes, recouvrement de dettes, enregistrement des dépenses, clôture journalière |
| **Responsable Magasin & Stocks** | `stock@boutique.com` | `stock123` | Gestion des arrivages/entrées, inventaire physique, alertes stocks et fournisseurs |

> **Astuce :** Vous pouvez vous connecter soit manuellement avec l'email et le mot de passe, soit en **1 clic** via la boîte de dialogue de connexion rapide. Vous pouvez également ajouter de nouveaux collaborateurs dans l'onglet **Paramètres & Équipes**.

---

## 🧭 Architecture des Modules & Sections

L'application est structurée en **9 sections professionnelles distinctes** accessibles via la barre de navigation :

### 1. 📦 Ventes & Stocks des Produits
Tableau dynamique de saisie quotidienne comprenant exactement les colonnes requises :
- **ID** : Référence unique (ex: `PRD-001`).
- **Désignation** : Nom complet du produit.
- **Stock (Initial)** : Stock présent au lever de rideau.
- **Entrer (+)** : Arrivages et réapprovisionnements du jour.
- **Totaux** : Stock total disponible (`Stock Initial + Entrer`).
- **Ventes (-)** : Nombre d'unités vendues dans la journée.
- **Prix Unitaire** : Tarif de vente unitaire.
- **Reste** : Stock physique restant calculé automatiquement (`Totaux - Ventes`).
- **Montant Vente** : Chiffre d'affaires brut généré (`Ventes × Prix Unitaire`).
- *Bonus :* Alertes sur stock bas, recherche instantanée et ajout rapide de produits avec coût d'achat pour le calcul de marge.

### 2. 💸 Dépenses Journalières (Sorties de Caisse)
- Enregistrement immédiat des charges opérationnelles (Motif, Montant, Catégorie : Transport, Alimentation, Factures, Fournitures, Salaires, Loyer, etc.).
- Jauge de répartition budgétaire par catégorie.
- Déduction comptable automatique du versement net de caisse.

### 3. 💳 Crédits & Recouvrements des Dettes
- **Qui a payé sa dette aujourd'hui :** Tableau des encaissements du jour indiquant clairement le client, l'heure, le montant payé, le reste à payer après ce paiement, et l'agent encaisseur.
- **Formulaire d'encaissement direct :** Calcul et affichage en temps réel du reste dû avant validation.
- **Octroi de nouveaux crédits :** Enregistrement des ventes à crédit (non perçues en cash).
- **Registre des créances clients :** Suivi de l'ensemble des clients débiteurs avec solde restant et statut (Soldé, Partiel, Impayé).

### 4. 📈 Analyses des Ventes (DataViz Recharts)
- Graphique multi-courbes interactif comparant l'évolution des ventes par **Désignation de produit** sur 7 jours.
- Filtres personnalisables permettant d'isoler ou de superposer les produits.
- Classement Top 5 des produits par chiffre d'affaires et part de contribution.

### 5. 💰 Bilan & Rentabilité Commerciale (P&L & Trésorerie)
- **Chiffre d'Affaires Brut (CA)**.
- **Coût d'Achat des Marchandises Vendues (COGS)**.
- **Marge Brute Commerciale** en valeur monétaire et en pourcentage (%).
- **Résultat Net d'Exploitation (Bénéfice Réel)** après déduction de toutes les dépenses.
- Tableau de réconciliation des flux de trésorerie liquide (Cash direct + dettes recouvrées - dépenses).

### 6. 👥 Clients (CRM & Fidélité)
- Base de données clients centralisée avec coordonnées, catégorie (VIP, Grossiste, Entreprise BTP, Particulier).
- Suivi du volume d'achats cumulés et de l'encours de crédit par client.

### 7. 🤝 Fournisseurs & Commandes
- Répertoire des partenaires et usines (contact, téléphone, produits fournis).
- Suivi des soldes dus aux fournisseurs (dettes d'approvisionnement) et des délais moyens de livraison.

### 8. 📑 Audit & Historique des Clôtures
- Journal immuable de toutes les sessions journalières clôturées.
- Vérification des écarts de caisse constatés (conforme, excédent, déficit) avec heure de clôture et signataire.

### 9. ⚙️ Paramètres & Gestion des Équipes
- Paramétrage de la boutique (Nom de l'entreprise, Slogan, Devise [FCFA, EUR, USD, GNF], TVA, Seuil de stock).
- Gestion des utilisateurs (Création de nouveaux profils avec assignation de rôle).

---

## 🧮 Formule Comptable de Fin de Journée (Versement Net)

$$\text{Cash Direct} = \text{Total Ventes Brut} - \text{Ventes Accordées à Crédit Aujourd'hui}$$
$$\text{Total Liquidités Entrantes} = \text{Cash Direct} + \text{Dettes Antérieures Recouvrées Aujourd'hui}$$
$$\mathbf{\text{Montant Net à Verser (Caisse)}} = \mathbf{\text{Total Liquidités Entrantes} - \text{Dépenses du Jour}}$$

---

## ⚡ Installation & Démarrage Local

```bash
# 1. Se positionner dans le dossier
cd C:\Users\HP\Desktop\saas-gestion-ventes

# 2. Installer les dépendances (si ce n'est pas déjà fait)
npm install

# 3. Démarrer l'application locale
npm run dev
```

Rendez-vous sur **`http://localhost:3000`**.
rendez-vous sur **'http://192.168.56.1:3000'**.
