## Neo4J
[Official website](https://neo4j.com/)

Neo4j is a [Graph database](https://neo4j.com/developer/graph-database/), based in NoSQL, used to relate data in a non pre-defined model

### Basic actions

* Create model with value
```
CREATE (n:Person:Swedish)
```

* Update model
```
Match(p) where ID(p)=4 SET p.name = 'John';
```

* Delete model
```
Match(p) where ID(p)=4 DELETE p;
```

* Create relationship
```
MATCH (a:Swedish),(b:Swedish)
WHERE ID(a)<>ID(b)
CREATE (a)-[r:COUNTRYMAN]->(b)
RETURN r
```

* Delete relationship
```
MATCH n-[rel:COUNTRYMAN]->r delete rel
```

* Set/remove label from node
```
MATCH (n:Swedish) SET n:Spanish REMOVE n :Swedish
```