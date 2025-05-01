# Advanced Curiosity Tasks (Style: "How Do Big Systems...") 
-----------------------------

## Task 1: "How Do Big Systems Store Data?"
-  Do apps like Instagram, Uber, or Amazon use SQL databases or something
else?

	- Instagram -> uses PostgreSQL for relational data and Cassandra for large-scale data storage.
	- Uber -> uses MySQL for transactional data and Apache Cassandra for large-scale data storage.
	- Amazon -> uses a combination of Amazon RDS (Relational Database Service) for SQL databases and DynamoDB for NoSQL data storage.

- kind of database structure big companies use and why.

| Type              | Company   | Why                                   | 
|-------------------|-----------|---------------------------------------|
| Relational        | Instagram | Structured data, complex queries      |
| Non Relational    | Instagram | Large-scale data storage, flexibility |
| Relational        | Uber      | Transactional data, complex queries   |
| Non Relational    | Uber      | Scalability, flexibility              |
| Relational        | Amazon    | Transactional data, complex queries   |
| Non Relational    | Amazon    | Scalability, high availability        |

-  SQL Server useage in big companies.
	- SQL Server is used by companies like Microsoft, Dell, and Bank of America for its robust features, scalability, and integration with other Microsoft products.

- What Kinde of database dose instagram use?
	- Instagram uses a combination of PostgreSQL for relational data and Cassandra for large-scale data storage.

-------

## Task 2: "Do Video Games Use Databases?"

Yes, video games use databases to store player data, game state, and other information. They often use NoSQL databases like MongoDB or Redis for real-time data storage and retrieval.

- How do online games (like PUBG, Fortnite, etc.) store player progress, points, and
profiles?

	- Online games like PUBG and Fortnite use databases to store player progress, points, and profiles. They often use a combination of SQL and NoSQL databases for this purpose. For example, they might use MySQL for structured data like player profiles and MongoDB for unstructured data like game logs and events.

- Do Video Games use SQL databases or something else?
	- Yes, video games use SQL databases for structured data storage, but they also use NoSQL databases for unstructured data and real-time data processing. For example, many games use Redis for caching and real-time data storage, while using SQL databases like MySQL or PostgreSQL for player profiles and game state.
	
- Example of a game that uses a relational database.
	- Call of Duty Warzone uses a relational database to store player data, game state, and other structured information. It uses MySQL for this purpose.
	- Minecraft uses a relational database to store player data, game state, and other structured information. It uses MySQL for this purpose.

------------
