# Knihovní systém SČMSD

# Library Management System ER Diagram

## About

This Entity-Relationship (ER) diagram represents the structure of a Library Management System. The system includes entities such as Student, Knihovna (Library), Kniha (Book), Exempláře (Copy), Správa Knihovního Fondu (Library Fund Management), Hlášení a Analýza (Reports and Analysis), Správa Uživatelských Účtů (User Account Management), and Oprávnění (Permissions).

The diagram illustrates the relationships between these entities, outlining key attributes and cardinalities.

## Entities

### Student
- PK_studentID
- studentJmeno
- studentPrijmeni
- email
- ...

### Knihovna
- PK_knihovnaID
- nazev
- adresa
- telefon
- ...

### Kniha
- PK_knihaID
- nazev
- autor
- zanr
- ...

### Exempláře
- PK_exemplarID
- FK_knihaID
- dostupnost
- ...

### Správa Knihovního Fondu
- PK_fondID
- FK_knihovnaID
- datumPridani
- ...

### Hlášení a Analýza
- PK_hlaseniID
- FK_knihovnaID
- datumVytvoreni
- ...

### Správa Uživatelských Účtů
- PK_uzivatelID
- FK_knihovnaID
- jmeno
- prijmeni
- heslo
- ...

### Oprávnění
- PK_opravneniID
- popis
- ...

## Relationships

- Student -(FK_studentID)-> Vyhledávání a Rezervace
- Knihovna -(FK_knihovnaID)-> Správa Knihovního Fondu
- Kniha -(FK_knihaID)-> Exempláře
- Knihovna -(FK_knihovnaID)-> Správa Uživatelských Účtů
- Oprávnění_Uživatel -(FK_uzivatelID)-> Správa Uživatelských Účtů

## Cardinality

- One-to-Many relationships denoted by "1" and "*".
