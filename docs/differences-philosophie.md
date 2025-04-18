# 🧭 PostgreSQL vs MySQL : Différences & Philosophie

## 📊 Tableau comparatif : PostgreSQL vs MySQL

| Critère                         | PostgreSQL                           | MySQL (MariaDB inclus)             |
|----------------------------------|--------------------------------------|------------------------------------|
| 🎯 Orientation                  | Orienté conformité SQL, extensible   | Orienté performance, simplicité    |
| 🧠 Philosophie                  | Respect strict des standards         | Pragmatisme, performance avant tout|
| 🔐 Sécurité des transactions   | ACID complet, MVCC avancé            | ACID partiel (selon moteur, ex: InnoDB) |
| 🧾 Types de données             | Riches (`UUID`, `JSONB`, `ARRAY`) | Moins riche (`JSON`, pas d’`ARRAY`)|
| 🔁 Concurrence                 | MVCC sans verrou global              | MVCC via InnoDB, plus limité       |
| 📦 Schémas                     | Oui, avec séparation logique         | Non, tout dans la base             |
| 🔍 Indexes & recherche texte   | Indexes avancés (`GIN`, `GiST`)      | Indexes classiques (`BTREE`, `FULLTEXT`)|
| 🔧 Extensions                  | Support officiel (`PostGIS`, `pg_trgm`, etc.) | Très limité ou inexistant        |
| 📚 Documentation               | Très complète et académique          | Plus orientée "quick start"        |
| 👥 Communauté                  | Forte dans les milieux techniques    | Très large, plus grand public      |

---

## 🐘 La philosophie de PostgreSQL

PostgreSQL est souvent vu comme **la "base de données des puristes"**. Elle est conçue autour de principes solides et robustes, pensés pour les projets sérieux et durables.

### Les grands piliers de sa philosophie :

- ✅ **Respect strict des standards SQL**
  PostgreSQL s’efforce de suivre les normes SQL ISO sans ajout arbitraire.

- 🧩 **Extensibilité native**
  Tu peux créer tes propres types de données, fonctions, opérateurs, index, langages embarqués (ex: PL/pgSQL, PL/Python...).

- 📦 **Organisation par schémas**
  Chaque base peut contenir plusieurs schémas, ce qui facilite l’isolation logique, la modularité, et le versionnage de données.

- 🔐 **Transactions fiables et sécurité des données**
  PostgreSQL implémente totalement ACID. Cela garantit l'intégrité même en cas de crash ou d'erreur réseau.

- 📚 **Documentation très complète**
  Chaque commande, type, fonction est documentée avec des exemples concrets.

- 🌍 **Philosophie open-source forte**
  La communauté PostgreSQL est très active, rigoureuse, et sensible à la qualité du code et des propositions.

---

