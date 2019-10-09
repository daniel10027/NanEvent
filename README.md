# [BASE DE DONNÉE NAN EVENT](https://github.com)

## Nombre de table :6


[x] Evenements

- id_event INT PRIMARY KEY AUTOINCREMENT,
- nom_event VARCHAR,
- date_debut DATE,
- date_fin DATE,
- id_commune INT FOREIGN KEY REFERENCES commune(id),
- id_categorie INT FOREIGN KEY REFERENCES categorie(id),
- statut VARCHAR,
- description VARCHAR,
- lieu VARCHAR

[x] Users

- id INT PRIMARY KEY AUTOINCREMENT,








