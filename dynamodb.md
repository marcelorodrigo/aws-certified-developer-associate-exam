# DynamoDB

## Primary Keys
- Partition Key (HASH)
  - Partition key must be unique for each row
  - Works similar to a primary key in a RDBMS
- Partition Key + Sort Key (HASH + RANGE)
  -  Data is grouped by partition key
  -  You must combine both PK + SK to form a unique combination for each row

## Read/Write Capacity Units
You can switch between the modes every 24 hours:
- Provisioned Mode
  - You specify how much CU for read/write
  - You pay for provisioned resources, even if you're not using them
- OnDemand Mode
  - Read/Write CU are allocated accordingly your load
  - Pay for what you use, generally more expensive

### Write Capacity Units
- Represents one write per second of 1KB
- KB are always rounded up
- If item is bigger than 1KB, more WCU are needed

### Read Capacity Units
- Eventually consistent read (default): you may get data still not updated recently (ms)
- Strong consisten read: you always get updated data using parameter "ConsistentRead" whey querying, but consume 2x RCU
- **One RCU represents one Strong Consistent Read per second, or two Eventually Consistent Read per second, up to 4kb**
