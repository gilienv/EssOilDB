# EssOilDB
Restructuring of  Essential Oil Database

### DATABASE STRUCTURE  

## Main Objectives:

1. Separate current infoP and infoC into more rational tables - CREATE SUB TABLES - [MANISH]
2. Separate Observational Data from Factual Data [VINITA AND MANISH]
3. Create NEW Tables - for Synonyms, Bibliography and Locations [AMBARISH]

--------------

## Table1. Observations [MANISH & VINITA]
This should contain "Plant Profile data" - What plant makes what. The Table will have:
* ProfileCode (An ID that matches all compounds found in ONE SINGLE Expt)
* PlantName: (Binomial Name) or KEY
* CompoundName: IUPAC or KEY
* CompoundAmountEmitted: Percentage Value 
* PlantPartEmissionSource: 
* TimeOfExpt: Ususally the YEAR
* Bibliography - DOI Number 
* LocationofExpt- Location


## Table2. Plant Fact Table [VINITA]

This should contain EVERYTHING one may wish to know about a certain plant:
* PlantName (From Table1)
* Synonym
* Taxonomic Family
* Genus
* Species
* PlantHabit ( For eg. is this a Tree/Shrub/Herb etc) 
* LinkToWiki

## Table3. Compound Fact Table [VINITA]
This should contain EVERYTHING one may wish to know about a certain compound:
* CompoundName (From Table1)
* Synonym
* ChemicalFamily
* KnownBiologicalActivity
* SMILESCode
* LinkToPubChem
* LinkToWiki/CheBI/Others
* ImageOfStructure
* LinkToGene/KEGGPathway 

## Table4. Bibliography Table [AMBARISH]
* DOI
* Author names
* Journal Name
* Article Title
* Volume/Issue/Chapter Number
* PageNumber
* LinkToCrossRef
* DOI-LinkToArticle

## Table5. Location Table [AMBARISH]
* LocationofExpt- LocationID
* Location-LinkToGoogleMaps
* Country
* State
* City/Town/Village
* Cooridinates
