# Lab 02

## Domeniul ales

Domeniul este muzica: un catalog de piese din Spotify. Fiecare item este o piesa,
descrisa prin titlu, artist, album, gen, popularitate si caracteristicile audio calculate
de Spotify (`danceability`, `energy`, `valence`, `tempo` etc.).

## Sursa datelor

- Dataset: [Spotify Music Dataset](https://www.kaggle.com/datasets/solomonameh/spotify-music-dataset)

## Volumul datelor

Am redus setul la 1500 de piese

## Proprietatile inregistrate in Recombee

Am ales urmatoarele proprietati:

| Nr. | Proprietate | Tip de date | Descriere |
| :--- | :--- | :--- | :--- |
| 1 | `track_name` | `string` | Titlul piesei |
| 2 | `track_artist` | `string` | Artistul/artistii |
| 3 | `popularity` | `int` | Popularitatea pe Spotify (0–100) |
| 4 | `danceability` | `double` | Cat de potrivita este piesa pentru dans (0–1) |

## Trimiterea item-urilor in Recombee

Scriptul `recombee_items.py` citeste dataset-ul si trimite piesele in baza de date Recombee 
`mystore-dev`, in loturi (`Batch`) de cate 100 de cereri `SetItemValues`.

## Rezultat

Datele au fost incarcate cu succes in Recombee: **1500 de item-uri**, toate cu atributele
completate, vizibile in Recombee Admin UI la *Items*.
