# 🐘 Commandes PostgreSQL utiles

Commandes PostgreSQL les plus fréquentes, pour manipuler, gérer et explorer ta base de données au quotidien.

---

## 🚀 Connexion à PostgreSQL

| Action                            | Commande                                                 |
|----------------------------------|----------------------------------------------------------|
| Se connecter à PostgreSQL        | `psql -U [utilisateur] -d [nom_bdd]`                     |
| Se connecter à une instance      | `psql -h [hôte] -p [port] -U [utilisateur] -d [nom_bdd]`  |
| Quitter `psql`                   | `\q`                                                     |

---

## Gestion des utilisateurs et permissions
- Créer un utilisateur : `CREATE USER nom_utilisateur WITH PASSWORD 'mot_de_passe';`
- Donner des permissions : `GRANT ALL PRIVILEGES ON base_de_donnees TO nom_utilisateur;`

## 🧭 Navigation dans les bases / tables

| Action                              | Commande                        |
|------------------------------------|---------------------------------|
| Lister toutes les bases            | `\l` ou `\list`                 |
| Lister les tables                  | `\dt`                           |
| Lister les schémas                 | `\dn`                           |
| Afficher les colonnes d'une table | `\d nom_table` ou `\dt+ nom_table` |
| Changer de base de données        | `\c nom_bdd`                    |

---



