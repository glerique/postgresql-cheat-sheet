# 🏗️ Gestion des schémas et structures PostgreSQL

## Schémas
Un schéma est une manière d'organiser les objets de base de données (tables, vues, fonctions, etc.) dans des espaces logiques distincts.

### Commandes de gestion des schémas
- **Créer un schéma** :
  ```sql
  CREATE SCHEMA nom_schema;
  ```
- **Supprimer un schéma** (et tous ses objets) :
  ```sql
  DROP SCHEMA nom_schema CASCADE;
  ```
- **Lister les schémas existants** :
  ```sql
  SELECT schema_name
  FROM information_schema.schemata;
  ```

---

## Tables
Les tables sont les structures principales pour stocker les données dans PostgreSQL.

### Créer une table
- Exemple de création d'une table simple :
  ```sql
  CREATE TABLE nom_table (
      id SERIAL PRIMARY KEY,
      nom VARCHAR(100),
      date_creation TIMESTAMP DEFAULT CURRENT_TIMESTAMP
  );
  ```

### Modifier une table
- **Ajouter une colonne** :
  ```sql
  ALTER TABLE nom_table ADD colonne INT;
  ```
- **Supprimer une colonne** :
  ```sql
  ALTER TABLE nom_table DROP COLUMN colonne;
  ```
- **Renommer une colonne** :
  ```sql
  ALTER TABLE nom_table RENAME COLUMN ancienne_colonne TO nouvelle_colonne;
  ```

### Supprimer une table
- **Supprimer une table** :
  ```sql
  DROP TABLE nom_table;
  ```
- **Supprimer une table uniquement si elle existe** :
  ```sql
  DROP TABLE IF EXISTS nom_table;
  ```

---

## Contraintes
Les contraintes permettent de garantir l'intégrité des données dans une table.

### Types de contraintes
- **Clé primaire** : Garantit l'unicité des lignes dans une table.
  ```sql
  ALTER TABLE nom_table ADD PRIMARY KEY (colonne);
  ```
- **Clé étrangère** : Définit une relation entre deux tables.
  ```sql
  ALTER TABLE nom_table
  ADD CONSTRAINT fk_nom_table
  FOREIGN KEY (colonne)
  REFERENCES autre_table (colonne);
  ```
- **Contrainte d'unicité** : Garantit qu'aucune valeur dupliquée n'existe dans une colonne.
  ```sql
  ALTER TABLE nom_table ADD UNIQUE (colonne);
  ```
- **Contrainte de vérification** : Définit une règle personnalisée.
  ```sql
  ALTER TABLE nom_table
  ADD CONSTRAINT check_positive
  CHECK (colonne > 0);
  ```

---

## Index
Les index améliorent les performances des requêtes en accélérant l'accès aux données.

### Commandes de gestion des index
- **Créer un index** :
  ```sql
  CREATE INDEX nom_index ON nom_table (colonne);
  ```
- **Créer un index unique** :
  ```sql
  CREATE UNIQUE INDEX nom_index_unique ON nom_table (colonne);
  ```
- **Supprimer un index** :
  ```sql
  DROP INDEX nom_index;
  ```

---

## Vues
Les vues sont des requêtes sauvegardées qui agissent comme des tables virtuelles.

### Commandes de gestion des vues
- **Créer une vue** :
  ```sql
  CREATE VIEW nom_vue AS
  SELECT colonne1, colonne2
  FROM nom_table
  WHERE condition;
  ```
- **Supprimer une vue** :
  ```sql
  DROP VIEW nom_vue;
  ```

---
