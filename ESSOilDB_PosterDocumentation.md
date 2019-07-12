## TABLE 1.0

### TABLE NAME

- profile - Table for plant profile.

### COLUMNS

- profile_id - Primary key. Auto-incremented.
- plant_id (FK) - Foreign key to plantdata. 
- location_id (FK) - Foreign key to locationdata.
- biblio_id (FK) - Foreign key to bibliographydata.
- date_id (FK) => MOVE to VALUE - Foreign key to samplecollectiontime.
- legacy_profile_id (JEA*..) - profile code for each plant.

- percent (NUMBER) or maybe range - Percentege of compound emmission.
- plantPart_id (FK) => MOVE to PROFILE  - Foreign key to plantpart.
- condition_id (FK) => MOVE to PROFILE - Foreign key to condition
- method_id (FK) => MOVE to PROFILE - Foreign key to method.
  method VARCHAR not normalized
  
 ## TABLE 2.0

### TABLE NAME

- plant - 

### COLUMNS

- plant_id - Primary key. Auto-incremented.
- species (binomial) - Plant species.
- family_id (FK) MERGE ?? - Plant family 
- habit_id (FK) ?DISCARD? - Plant habit
- genus - Plant genus.

- ADD Wikidata

## TABLE 3.0

### TABLE NAME

- location - Table for experiment location.

### COLUMNS

- location_id - id for each location/address
- name VARCHAR - location or address
- region - experiment city/town/village.
- state - state
- country - country


*NEEDS NORMALISING to include region, country,

## TABLE 4.0

### TABLE NAME

- family - Table for plant family.

### COLUMNS

- family_id - an id for each plant family.
- name - plant family name.

## TABLE 5.0

### TABLE NAME

- habit - Table for plant habit.

### COLUMNS

- habitat_id - an id for each plant habit.
- habit - plant habit.


## TABLE 6.0

### TABLE NAME

- bibliography - Table for bibliography.

### COLUMNS

- biblio_id - id for each bibliography.
- doi - doi number
- doi_link - weblink to doi.
- title - title of the article.
- author - author name.
- journal - name of the journal.
- volume - voulume
- year - year of publication.


## TABLE 7.0

### TABLE NAME

- collection_date - Table for experimental condition.

### COLUMNS

- collection_date_id - an id for sample collection date (year).
- value (DATE) - time of experiment.
MERGE WITH PROFILE


## TABLE 8.0

### TABLE NAME

- composition - Table for chemical composition (emmission).

### COLUMNS

- composition_id - an id for each record in the table.
- profile_id (FK) - profile code assigned to compound.
- compound_id (FK) - an id assigned to each compound.
- percent (NUMBER) or maybe range - percentage amount of chemical compound as their emission.
- plantPart_id (FK) => MOVE to PROFILE
- condition_id (FK) => MOVE to PROFILE
- method_id (FK) => MOVE to PROFILE

method VARCHAR not normalized


## TABLE 9.0

### TABLE NAME

- compoundmethod VARCHAR not normalized - Table for chemical compounds.

### COLUMNS

- compound_id - Primary key. Auto-incremented. an id assigned to each record into table
- systemaric_name (?) - compound name.
- trivial_name (???) - chemical name.
- smiles - SMILES code.
- cas_no - CAS number.
- activity_id (FK) NEED TO DISCUSS - where does this come from? - Foreign key to compound activity table. compound activity.
- chemical_group_id (FK?) WHERE IS THIS? - Foreign key to compoundgroupdata table. An id for each chemical compound group.
- formula - Chemical compound formula.

## TABLE 10.0

### TABLE NAME

- plantpart - Table for plant part.

### COLUMNS

- plantpart_id - Primary key. Auto-incremented. An id for each plant part.
- name - plant part name.

## TABLE 11.0

### TABLE NAME

- activity - Table for chemical compound activity.

### COLUMNS

- activity_id - Primary key of the table. Auto-incremented.
- name - compound activity name.



## TABLE 12.0

### TABLE NAME

- condition - Table for experimental condition.

### COLUMNS

- condition_id - Primary key. Auto-incremented.
- condition VARCHAR not normalized - Experimental condition.



## TABLE 13.0

### TABLE NAME

- chemicalgroup - Table for chemical compound group.

### COLUMNS

- chemical_group_id - Primary key. Auto-incremented. Chemical group id.
- chemical_group_name VARCHAR not normalized - Chemical group name.



## TABLE 14.0

### TABLE NAME

- method - Table for experimental methodology.

### COLUMNS

- method_id - Primary key. Auto-incremented. Experimental methodology id.
- method VARCHAR not normalized - Experimental methodology.