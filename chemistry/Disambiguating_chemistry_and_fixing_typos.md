### API

- [OPSIN](https://opsin.ch.cam.ac.uk) - Web API.

- [OPSIN](https://bitbucket.org/dan2097/opsin/downloads/) - Local (stand-alone) API.

- [PubChem](https://pubchem.ncbi.nlm.nih.gov/idexchange/idexchange.cgi) - Web API. Services for PubChem queries and downloads.

### Run steps PubChem API

- Navigate to https://pubchem.ncbi.nlm.nih.gov/idexchange/idexchange.cgi link.

- Select for `CIDs` option into `Input ID list` section.

- Browse file containing list of compound names.

- Select for `same CID` option into `Operator Type` setion.

- To get CIDs select for `CIDs` into `Output IDs` section.

- To get inchi select for `InChIs` into `Output IDs` section.

- Select for `Two column file showing each input-output correspondence` into `Output Method` section.

- submit job.

### Run steps OPSIN API

- Form a .csv formatted file listing compounds.

- Run following command-line argument.

  `java -jar [jarfile.jar] -o inchi namesin.txt inchiout.txt`
  
  `-o - command-line argument parameter for output option.`
  
  `namesin.txt - input file containing compound name list.`
  
  `inchiout.txt - output file containing inchi code.`
  
  
  
  ### Output file description
  
  #### 100cnameOPSIN.csv
  
  Column description.
  
  `OPSIN_lookup_name` - OPSIN lookup for corresponding input compound names.
  
  `OPSIN_lookup_inchis` - generated inchis for the input compound name.
  
  `OPSIN_lookup_comments` - generated comment for not found.
  
  Statistics
  
  - count of input entries - 100.
  
  - count of found results - 35
  
  - count of not found results - 65
  
  
   #### 100cnamePubChem.csv
   
   Column description.
   
   `PubChem_lookup_name` - PubChem lookup for corresponding input compound names.
   
   `PubChem_lookup_cid` - generated cid for the input compound name. 
   
   `PubChem_lookup_inchis` - generated inchis for the input compound name.
    
     
     
   Statistics
  
  - count of input entries - 100.
  
  - count of found results - 85
  
  - count of not found results - 15
  
  
  Both files are merged to form single file `100PubchemAndOPSIN.csv` with additional column for EssOilDB_entry for compound names present into the database.   
  
 ---------------------------------------------------------------------------------------------------------------------------
  
## 16 July 2019, Tuesday.

### Run status - Batch_1, Batch_2, Batch_3, Batch_4 - complete.

#### Output file.

##### 500cnameWIKIDATABatch01234.csv

Column description.

- cname - compound name used for search query.

- wikidata - WIKIDATA id.

- wikidata_lookup_name - WIKIDATA lookup name ( addition to compound name as search query ).

- wikidata_lookup_comment - description generated by wikidata.

- wikipedia - wikipedia search string.

##### 500cnameWIKIDATABatch01234.tsv

##### 500PubChemBatch01234_inchisCID.csv

Column description.

- PubChem_lookup_name - compound name used for search query.

- PubChem_lookup_cid - generated Pubchem CID.

- PubChem_lookup_inchis - generated inchis by PubChem API.


##### 500PubChemBatch01234_inchisCID.tsv

##### 500cnameOPSINbatch01234_inchis.csv

Column description

- OPSIN_lookup_name - compound name used for search query.

- OPSIN_inchis - generated inchis by OPSIN.

- OPSIN_comments - generated comments for not found entries.

##### 500cnameOPSINbatch01234_inchis.tsv