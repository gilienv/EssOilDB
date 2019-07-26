#Compound Information found in Plant
```
count(*): 141329
icoid	int(11)	NO	PRI		auto_increment
ipid	int(11)	YES	MUL		//key for plant related information mapped in infopdata
coid	int(11)	YES	MUL		//key for compound data in compounddata
percent	varchar(20)	YES			
ppid	int(11)	YES	MUL		//key for plant part in plantpartdata
cagroup	varchar(500)	YES			//String containing information about compound activities mapped as key in compoundactivitydata joined by '#'
expcid	int(11)	YES	MUL		//key for experimental condition in expconditiondata
idfnid	int(11)	YES	MUL		//key for identification method in identificationdata
casid	int(11)	YES	MUL		//key for CAS no present in casdata
```
```
1	2391	800	3.2	14	145	474	27	1017
2	2391	2314	0.7	14	145	474	35	653
3	2391	2418	0.2	14	145	474	1	388
4	2391	2495	7.5	14	145	474	5	767
5	2391	2515	0.3	14	145	474	35	736
6	2391	2518	0.7	14	145	474	35	379
7	2391	2565	3.8	14	123#85#5#7#12#23#33#35#40#56#63#66#67#75#86#94#111#113#132#133#135#136#152#154#156#165#168#174#	474	24	565
8	2391	2587	0.3	14	157	474	14	233
9	2391	2598	2.5	14	157	474	25	1107
10	2391	2705	1.6	14	85#63#	474	35	928
```
								
            
