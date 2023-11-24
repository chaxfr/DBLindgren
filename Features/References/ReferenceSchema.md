# Reference Schema
This document shall contain a definition for the schema used to export references  
from the database. In addition to "pure" references, it shall also be able to  
export incidents from the database into a table format.

# Reference export

# RIS.format

# Incident export

Användningsområden:
1. Export av .RIS-fil (där samtliga källor hänvisade till dyker upp en gång)
2. Skapande av fotnoter utifrån incidenter lagrade i databasen
3. Export i tabellform av samtliga incidenter associerade med ett större projekt

2&3 kan möjligtvis kombineras till en output

Referenstyper att stödja för de olika användningsområdena ovan:
1. Skannat arkivmaterial med associerad arkivreferens (arkiv/intermediate/volym)
2. Fristående dokument (pressklipp, årsredovisningar), saker som inte har en supertydlig referensram
3. Akademiska dokument (Journalartiklar, böcker, etc) saker som har en tydlig referens men som inte passar in i ett arkivformat.  