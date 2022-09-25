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
 
## Normal Forms
| Normal Forms | Main Point |
|-----------------|--------|
| 1st Normal Form | No Multivalued attribute (Only single valued attribute)| 
| 2nd Normal Form | In 1st NF+ No Partial Dependency (Only Full Dependency)|
| 3rd Normal Form | In 2nd NF+No Transitive Dependency (No Non-Prime should determine non-prime (non-unique) |
| BCNF (Boyce - Codd Normal Form)| In 3rd NF+ L.H.S must be C.K or S.K | 
| 4th Normal Form | In BCNF + No Multivalued Dependency |
| 5th NF | In 4th NF + Loseless decomposition |
