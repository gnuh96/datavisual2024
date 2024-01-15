# Indexation File - Projet Technique Informatique & Web

Ce projet fait partie du module Visualisation des données.

## Auteur
NGUYEN Tuan Hung - 21006891

## Jeu de données : Film

- Les colonnes : Titre, Date de publication, Pays, Durée, Genre

- Request :

  ```
  SELECT ?film ?filmLabel ?publication_date ?genreLabel ?country_of_originLabel ?duration WHERE {
            SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en". }
            ?film wdt:P31 wd:Q11424.
            OPTIONAL { ?film wdt:P136 ?genre. }
            OPTIONAL { ?film wdt:P495 ?country_of_origin. }
            OPTIONAL { ?film wdt:P577 ?publication_date. }
            OPTIONAL { ?film wdt:P2047 ?duration. }
          }
          LIMIT 100
  ```


