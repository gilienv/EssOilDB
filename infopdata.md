# Infopdata (plant records)

```
count(*): 3247
ipid	int(11)	NO	PRI		auto_increment
pid	int(11)	YES	MUL		// key for plant in plantdata
locid	int(11)	YES	MUL		// key for location in locationdata
pfid	int(11)	YES	MUL		// key for plant family id in plantfamilydata (possible redundant)
pgid	int(11)	YES	MUL		// key for plant group id in plantgroupdata (plant or weed) 
doiid	int(11)	YES	MUL		// key for doi(bibliographic record) in plantdoidata 
scid	int(11)	YES	MUL		// key for sample collection data id in samplecollectiondata
pinfofileid	varchar(50)	YES			/*** Field to be deleted after inseting Compound_data ***/
```
```
<sample data>
1	45	402	1	1	1	32	JEAcakoprtu2002Roo
2	45	160	1	1	1	34	JEAcaceli2003lea
3	45	160	1	1	1	34	JEAcaceli2003Rhi
4	45	337	1	1	1	41	JEAcain2003Lea
5	45	337	1	1	1	41	JEAcain2003Rhi
6	45	639	1	1	1	99	JEAcaqu2008Ste
7	44	71	2	1	1	99	JEAchbair2002Fem
8	44	71	2	1	1	99	JEAchbair2002Mal
9	71	770	3	1	1	99	JEAsatu2014bul
10	352	134	4	1	1	37	JECamciin2002Aer
```

