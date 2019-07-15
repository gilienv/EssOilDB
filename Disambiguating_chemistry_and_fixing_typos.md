### API

- [OPSIN] (https://opsin.ch.cam.ac.uk) - Web API.

- [OPSIN] (https://bitbucket.org/dan2097/opsin/downloads/) - Local (stand-alone) API.

- [PubChem] (https://pubchem.ncbi.nlm.nih.gov/idexchange/idexchange.cgi) - Web API. Services for PubChem queries and downloads.

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
  
  ` -o - command-line argument parameter for output option.
     namesin.txt - input file containing compound name list.
     inchiout.txt - output file containing inchi code.
     `
  
  
  
  
- 
