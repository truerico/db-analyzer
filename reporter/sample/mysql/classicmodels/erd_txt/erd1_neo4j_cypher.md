MATCH (n) DETACH DELETE n ;

// TABLES ENTITIES 

CREATE (classicmodels_customers:Table {title:'customers', table_schema:'classicmodels', is_orphan_table:'0'})
CREATE (classicmodels_employees:Table {title:'employees', table_schema:'classicmodels', is_orphan_table:'0'})
CREATE (classicmodels_offices:Table {title:'offices', table_schema:'classicmodels', is_orphan_table:'0'})
CREATE (classicmodels_orderdetails:Table {title:'orderdetails', table_schema:'classicmodels', is_orphan_table:'0'})
CREATE (classicmodels_orders:Table {title:'orders', table_schema:'classicmodels', is_orphan_table:'0'})
CREATE (classicmodels_payments:Table {title:'payments', table_schema:'classicmodels', is_orphan_table:'0'})
CREATE (classicmodels_productlines:Table {title:'productlines', table_schema:'classicmodels', is_orphan_table:'0'})
CREATE (classicmodels_products:Table {title:'products', table_schema:'classicmodels', is_orphan_table:'0'})

// VIEWS 

CREATE (classicmodels_aboveavgproducts:View {title:'aboveavgproducts', view_schema:'classicmodels' })
CREATE (classicmodels_bigsalesorder:View {title:'bigsalesorder', view_schema:'classicmodels' })
CREATE (classicmodels_customerorders:View {title:'customerorders', view_schema:'classicmodels' })
CREATE (classicmodels_customerorderstats:View {title:'customerorderstats', view_schema:'classicmodels' })
CREATE (classicmodels_customerpayments:View {title:'customerpayments', view_schema:'classicmodels' })
CREATE (classicmodels_daysofweek:View {title:'daysofweek', view_schema:'classicmodels' })
CREATE (classicmodels_saleperorder:View {title:'saleperorder', view_schema:'classicmodels' })

// VIEWS RELATED TABLES 

CREATE (classicmodels_aboveavgproducts)-[:MAKE_USE_OF {info:'classicmodels_products'}]->(classicmodels_products)
CREATE (classicmodels_bigsalesorder)-[:MAKE_USE_OF {info:'classicmodels_saleperorder'}]->(classicmodels_saleperorder)
CREATE (classicmodels_customerorders)-[:MAKE_USE_OF {info:'classicmodels_customers'}]->(classicmodels_customers)
CREATE (classicmodels_customerorders)-[:MAKE_USE_OF {info:'classicmodels_orderdetails'}]->(classicmodels_orderdetails)
CREATE (classicmodels_customerorders)-[:MAKE_USE_OF {info:'classicmodels_orders'}]->(classicmodels_orders)
CREATE (classicmodels_customerorderstats)-[:MAKE_USE_OF {info:'classicmodels_customers'}]->(classicmodels_customers)
CREATE (classicmodels_customerorderstats)-[:MAKE_USE_OF {info:'classicmodels_orders'}]->(classicmodels_orders)
CREATE (classicmodels_customerpayments)-[:MAKE_USE_OF {info:'classicmodels_customers'}]->(classicmodels_customers)
CREATE (classicmodels_customerpayments)-[:MAKE_USE_OF {info:'classicmodels_payments'}]->(classicmodels_payments)
CREATE (classicmodels_saleperorder)-[:MAKE_USE_OF {info:'classicmodels_orderdetails'}]->(classicmodels_orderdetails)

// FKEYS 

CREATE (classicmodels_employees)-[:FK {fk_columns:'salesrepemployeenumber'}]->(classicmodels_customers)
CREATE (classicmodels_employees)-[:FK {fk_columns:'reportsto'}]->(classicmodels_employees)
CREATE (classicmodels_offices)-[:FK {fk_columns:'officecode'}]->(classicmodels_employees)
CREATE (classicmodels_orders)-[:FK {fk_columns:'ordernumber'}]->(classicmodels_orderdetails)
CREATE (classicmodels_products)-[:FK {fk_columns:'productcode'}]->(classicmodels_orderdetails)
CREATE (classicmodels_customers)-[:FK {fk_columns:'customernumber'}]->(classicmodels_orders)
CREATE (classicmodels_customers)-[:FK {fk_columns:'customernumber'}]->(classicmodels_payments)
CREATE (classicmodels_productlines)-[:FK {fk_columns:'productline'}]->(classicmodels_products)
