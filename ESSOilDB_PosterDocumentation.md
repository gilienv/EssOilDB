## TABLE 1.0

### TABLE NAME

- profile

### COLUMNS

- profile_id
- plant_id (FK)
- location_id (FK)
- biblio_id (FK)
- date_id (FK) => MOVE to VALUE
- legacy_profile_id (JEA*..)

- percent (NUMBER) or maybe range
- plantPart_id (FK) => MOVE to PROFILE
- condition_id (FK) => MOVE to PROFILE
- method_id (FK) => MOVE to PROFILE
  method VARCHAR not normalized
  
 ## TABLE 2.0

### TABLE NAME

- plant

### COLUMNS

- plant_id
- species (binomial)
- family_id (FK) MERGE ??
- habitat_id (FK) ?DISCARD?
- genus

- ADD Wikidata

## TABLE 3.0

### TABLE NAME

- location

### COLUMNS

- location_id
- name VARCHAR
- region
- country
- state
- city

*NEEDS NORMALISING to include region, country,

## TABLE 4.0

### TABLE NAME

- family

### COLUMNS

- family_id
- name

## TABLE 5.0

### TABLE NAME

- habit

### COLUMNS

- habitat_id
- habit


## TABLE 6.0

### TABLE NAME

- bibliography

### COLUMNS

- biblio_id
- doi
- doi_link
- title
- author
- journal
- volume
- year


## TABLE 7.0

### TABLE NAME

- collection_date

### COLUMNS

- collection_date_id
- value (DATE)
MERGE WITH PROFILE


## TABLE 8.0

### TABLE NAME

- composition

### COLUMNS

- composition_id
- profile_id (FK)
- compound_id (FK)
- percent (NUMBER) or maybe range
- plantPart_id (FK) => MOVE to PROFILE
- condition_id (FK) => MOVE to PROFILE
- method_id (FK) => MOVE to PROFILE

method VARCHAR not normalized


## TABLE 9.0

### TABLE NAME

- compound

### COLUMNS

- compound_id
- systemaric_name (?)
- trivial_name (???)
- smiles
- cas_no
- activity_id (FK) NEED TO DISCUSS - where does this come from?
- chemical_group_id (FK?) WHERE IS THIS?
- formula

## TABLE 10.0

### TABLE NAME

- plantpart

### COLUMNS

- plantpart_id
- name

## TABLE 11.0

### TABLE NAME

- activity

### COLUMNS

- activity_id
- name



## TABLE 12.0

### TABLE NAME

- condition

### COLUMNS

- condition_id
- condition VARCHAR not normalized



## TABLE 13.0

### TABLE NAME

- chemicalgroup

### COLUMNS

- chemical_group_id
- chemical_group_name VARCHAR not normalized



## TABLE 14.0

### TABLE NAME

- method

### COLUMNS

- method_id
- method VARCHAR not normalized 
