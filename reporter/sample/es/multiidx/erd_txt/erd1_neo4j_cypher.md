MATCH (n) DETACH DELETE n ;

// INDEX ENTITIES 

CREATE (db_logs:Index {alias_list:'' })
CREATE (db_movies:Index {alias_list:'' })
CREATE (db_accounts:Index {alias_list:'' })
CREATE (db_shakespeare:Index {alias_list:'' })

// FKEYS 

