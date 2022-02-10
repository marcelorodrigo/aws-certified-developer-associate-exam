# DynamoDB

## Primary Keys
- Partition Key (HASH)
  - Partition key must be unique for each row
  - Works similar to a primary key in a RDBMS
- Partition Key + Sort Key (HASH + RANGE)
  -  Data is grouped by partition key
  -  You must combine both PK + SK to form a unique combination for each row
- 
