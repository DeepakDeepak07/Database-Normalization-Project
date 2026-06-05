🎵 Music Database Normalization Project (4NF)

## 📌 Project Overview

This project demonstrates the process of converting a **denormalized music dataset** into **Fourth Normal Form (4NF)**.  
The original dataset contained repeating groups and multi-valued attributes such as multiple songs, genres, and albums embedded within a single table.

The goal of this project is to:
- Remove multi-valued dependencies
- Eliminate redundancy
- Structure data into clean relational tables
- Achieve **Fourth Normal Form (4NF)**

---

## 🧱 Normalization Level

**Normalization Level:** Fourth Normal Form (4NF)

**Key Principle:**
- Eliminates multi-valued dependencies (e.g., multiple songs, genres, albums in one record)
- Ensures each table represents a single theme/entity

---

## 📂 Raw Unnormalized Data

### 🎤 Original Dataset (Unstructured Form)

```txt
Artists	City	State	Country	Year_Active	Genre	Songs	Albums

Coldplay	London	London	UK	1997	Alternative, Pop, Rock	(Yellow,4.29,Rock,2000-06-26),(Trouble,4 mins 31 secs, Rock,2000-10-23),(Clocks,5m 8s,Alternative,17-03-2003),(The Scientist,5.10,Alternative,2002-11-11),(In My Place,3.47,Alternative,2002-08-05),(God Put a Smile Upon Your Face, 4.58,Alternative,2003-07-01),(Higher Power,3.31,Pop,2021-05-07)	(Parachutes,2000-07-10,41.25), (A Rush of Blood to the Head,2002-26-08,54.06), (Music of the Spheres,2021-10-15,41.50)

Daft Punk	Paris	Île-de-France	France	1993	Electronic, House, Techno	(One More Time,5.20,House,2000-11-13),(Get Lucky,4.07,Funk,2013-04-19),(Around the World,7.10,Electronic,1997-04-07),(Lose Yourself to Dance,5.53,Funk,2013-08-13)	(Discovery,2001-03-12,60.50),(Homework,20-01-1997,73:53),(Random Access Memories,2013-05-17,74.39)

Pharrell Williams	Virginia Beach	Virginia	USA	1992	R&B, Hip-Hop, Pop	(Happy,3.55,Soul,2013-11-21),(Get Lucky,4.07,Funk,2013-04-19),(Can I Have It Like That,3.55,Hip-Hop,2005-10-10)	(Despicable Me 2: Original Motion Picture Soundtrack,2013-07-02,61.24),(In My Mind,2006-07-25,64.20)

Gwen Stefani	Fullerton	California	USA	2004	Rock, Pop	(Hollaback Girl,3.19,Pop,2005-03-22),(Can I Have It Like That,3.55,Hip-Hop,2005-10-10)	(Love. Angel. Music. Baby.,48.27,2004-11-12)

Taylor Swift	West Reading	Pennsylvania	USA	2003	Country, Folk, Pop	(Shake It Off,3.39,Pop,2014-08-14),(Blank Space,3.52,Pop,10-11-2014),(Style,3.51,Pop,2015-02-09)	(1989,2014-10-27,48.41)

Black Sabbath	Birmingham	West Midlands	UK	1968	Heavy Metal	(Paranoid,2.47,Heavy Metal,7/8/1970),(Iron Man,5.55,Heavy Metal,1971-10-01),(War Pigs,7.56,Heavy Metal,1970-09-18),(Black Sabbath,6.20,Heavy Metal,1970-02-13),(N.I.B.,6.06,Heavy Metal,1970-02-13)	(Paranoid,1970-09-18,41.51),(Black Sabbath,Feb 13 1970,38.08)
```
# 🧠 Database Normalization (4NF)

## 📌 Normalization Summary

| 🔢 Component | 📖 Description |
|--------------|----------------|
| 🧩 **Normalization Level** | Fourth Normal Form (4NF) |
| 🎯 **Key Principle** | Removed multi-valued dependencies such as Genres, Songs, and Albums from the original dataset |
| 👤 **Artists Table** | Stores artist-specific attributes only |
| 🌍 **Locations Table** | Stores unique city/state/country combinations |
| 🎼 **Genres Table** | Stores unique genre values |
| 🔗 **ArtistGenres Table** | Resolves many-to-many relationship between artists and genres |
| 🎵 **Songs Table** | Stores songs linked to artists using `ArtistID` |
| 💿 **Albums Table** | Stores albums linked to artists using `ArtistID` |

---

# 📊 Results (Visual Output)

## 1. Artists Table Output
![Artists Table](images/artists_table.png)

Displays cleaned artist records with normalized location references.

---

## 2. Songs Table Output
![Songs Table](images/songs_table.png)

Shows extracted song-level data with proper atomic attributes.

---

## 3. Albums Table Output
![Albums Table](images/albums_table.png)

Represents album data separated from artist entity for normalization compliance.

---

## 4. Genre Mapping (ArtistGenres)
![Artist Genres](images/artist_genres.png)

Displays many-to-many relationships between artists and musical genres.

---

## 5. Locations Table Output
![Locations Table](images/locations_table.png)

Stores unique location entries to eliminate redundancy.

---

# 📌 Conclusion

This project demonstrates how a denormalized dataset can be transformed into a **fully normalized 4NF relational model**, improving:

- Data consistency
- Reduced redundancy
- Query efficiency
- Structural integrity

---
