## Super Key -> Candidate Key -> Primary Key

## [Data Normalisation and Denormalisation](https://youtu.be/W_5vn8TBLys)

| S.No. | Normalisation | Denormalisation |
|------|-------------|---------------|
| 1 | Reduces Redundancy | Adds Intentional Redundancy |
| 2 | Faster Writes (Faster Insert, Update, and Delete Operation) | Slower Writes |
| 3 | Slower Reads | Faster Reads (Faster Select Operation) |
| 4 | Optimised Disk Usuage | Wastage of Disk Space |
| 5 | More Joins needed while retriving of the data | Less Joins |
| 6 | Small and Many Tables |  Bigger and Less Tables |
| 7 | Application: OLTP (Where resouces are less)| OLAP (Where resources are easily accessible like in Cloud Computing era) |
 
## [Normal Forms](https://youtu.be/EGEwkad_llA)
| Normal Forms | Main Point |
|-----------------|--------|
| 1st Normal Form | No Multivalued attribute (Only single valued attribute)| 
| 2nd Normal Form | In 1st NF+ No Partial Dependency (Only Full Dependency)|
| 3rd Normal Form | In 2nd NF+No Transitive Dependency (No Non-Prime should determine non-prime (non-unique) |
| BCNF (Boyce - Codd Normal Form)| In 3rd NF+ L.H.S must be C.K or S.K | 
| 4th Normal Form | In BCNF + No Multivalued Dependency |
| 5th NF | In 4th NF + Loseless decomposition |

### Examples 
#### 1st Normal Form
Let we have a table of 3 columns.
| R.No. | Name | Course |
|------|-----|----|
| 1 | P | C, C++ |
| 2 | R | Python, C |

So, course attribute is multivalued attribute.
It will be difficult to retrieve the data having course of C++ only.
So, we can make 2 tables instead of this one:)
One is having both R.No and Name columns and 2nd is having both R.No. and course columns
| R.No. | Name |
|--------|------|
| 1 | P |
| 2 | R |

| R.No. | Course |
|-------|-------|
| 1 | C |
| 1 | C++ |
| 2 | Python |
| 2 | C |

#### 2nd Normal Form
Let the functional Dependency is 
- AB-> C
- AB Candidate Key
- C Non Unique attribute

So, it means proper subset of AB i.e A and B cannot make partial functional dependency with C alonely.
- A-> C
- B-> C
- cannot be functional dependencies.

#### 3rd Normal Form

Let X->Y->Z
where X is Candidate key
,Y is Non Prime
,Z is Non Prime 

Here Non prime is determining non prime, although, X is indirectly determining Z (Transitive Dependency).
It should not be there.

#### BCNF

Let the functional dependency is X-> Y. Here X should be super key or candidate key.

#### 4th Normal Form [(Link)](https://www.javatpoint.com/dbms-forth-normal-form)
#### 5th Normal Form [(Link)](https://www.javatpoint.com/dbms-fifth-normal-form)


## How to delete duplicate records from a table in SQL 

[https://youtu.be/Wlb4YKnZ75k](https://youtu.be/Wlb4YKnZ75k)




















