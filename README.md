# [BASE DE DONNÉE NAN EVENT](https://github.com)

# Nombre de table :6

### compagnie

### - id INT PRIMARY KEY AUTOINCREMENT,
- nom_compagnie VARCHAR,
- addresse VARCHAR,
- email VARCHAR,
- contact VARCHAR,
- password VARCHAR,

### commune
### - id INT PRIMARY KEY AUTOINCREMENT,
 - nom VARCHAR,


## events
### - id INT PRIMARY KEY AUTOINCREMENT,
- nom_event VARCHAR,
- date_debut DATE,
- date_fin DATE,
- id_commune INT FOREIGN KEY REFERENCES commune(id),
- id_categorie INT FOREIGN KEY REFERENCES categorie(id),
- statut VARCHAR,
- description VARCHAR,
- lieu VARCHAR

## commune_event
### - id INT PRIMARY KEY AUTOINCREMENT,
- id_event INT FOREIGN KEY REFERENCES event(id),
- id_commune INT FOREIGN KEY REFERENCES commune(id),

## users
### - id INT PRIMARY KEY AUTOINCREMENT,
- id_commune FOREIGN KEY REFERENCES commune(id)
- nom VARCHAR,
- prenom VARCHAR,
- email VARCHAR,
- contact VARCHAR,
- password VARCHAR


## categorie_event
### - id INT PRIMARY KEY AUTOINCREMENT,
 - nom VARCHAR,

 
 ## participants
 ### - id INT PRIMARY KEY AUTOINCREMENT,
 - id_user FOREIGN KEY REFERENCES users(id),
 - id_event FOREIGN KEY REFERENCES events(id)
 









