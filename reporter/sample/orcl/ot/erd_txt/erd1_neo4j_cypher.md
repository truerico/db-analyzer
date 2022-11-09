MATCH (n) DETACH DELETE n ;

// TABLES ENTITIES 

CREATE (ot_contacts:Table {title:'contacts', table_schema:'ot', is_orphan_table:'0'})
CREATE (ot_countries:Table {title:'countries', table_schema:'ot', is_orphan_table:'0'})
CREATE (ot_customers:Table {title:'customers', table_schema:'ot', is_orphan_table:'0'})
CREATE (ot_employees:Table {title:'employees', table_schema:'ot', is_orphan_table:'0'})
CREATE (ot_inventories:Table {title:'inventories', table_schema:'ot', is_orphan_table:'0'})
CREATE (ot_locations:Table {title:'locations', table_schema:'ot', is_orphan_table:'0'})
CREATE (ot_orders:Table {title:'orders', table_schema:'ot', is_orphan_table:'0'})
CREATE (ot_order_items:Table {title:'order_items', table_schema:'ot', is_orphan_table:'0'})
CREATE (ot_products:Table {title:'products', table_schema:'ot', is_orphan_table:'0'})
CREATE (ot_product_categories:Table {title:'product_categories', table_schema:'ot', is_orphan_table:'0'})
CREATE (ot_regions:Table {title:'regions', table_schema:'ot', is_orphan_table:'0'})
CREATE (ot_warehouses:Table {title:'warehouses', table_schema:'ot', is_orphan_table:'0'})

// VIEWS 

CREATE (ot_country_locations:View {title:'country_locations', view_schema:'ot' })
CREATE (ot_order_details:View {title:'order_details', view_schema:'ot' })

// VIEWS RELATED TABLES 

CREATE (ot_country_locations)-[:MAKE_USE_OF {info:'ot_countries'}]->(ot_countries)
CREATE (ot_country_locations)-[:MAKE_USE_OF {info:'ot_locations'}]->(ot_locations)
CREATE (ot_order_details)-[:MAKE_USE_OF {info:'ot_orders'}]->(ot_orders)
CREATE (ot_order_details)-[:MAKE_USE_OF {info:'ot_order_items'}]->(ot_order_items)

// FKEYS 

CREATE (ot_customers)-[:FK {fk_columns:'customer_id'}]->(ot_orders)
CREATE (ot_product_categories)-[:FK {fk_columns:'category_id'}]->(ot_products)
CREATE (ot_locations)-[:FK {fk_columns:'location_id'}]->(ot_warehouses)
CREATE (ot_employees)-[:FK {fk_columns:'employee_id'}]->(ot_orders)
CREATE (ot_employees)-[:FK {fk_columns:'employee_id'}]->(ot_employees)
CREATE (ot_countries)-[:FK {fk_columns:'country_id'}]->(ot_locations)
CREATE (ot_products)-[:FK {fk_columns:'product_id'}]->(ot_inventories)
CREATE (ot_orders)-[:FK {fk_columns:'order_id'}]->(ot_order_items)
CREATE (ot_products)-[:FK {fk_columns:'product_id'}]->(ot_order_items)
CREATE (ot_customers)-[:FK {fk_columns:'customer_id'}]->(ot_contacts)
CREATE (ot_regions)-[:FK {fk_columns:'region_id'}]->(ot_countries)
CREATE (ot_warehouses)-[:FK {fk_columns:'warehouse_id'}]->(ot_inventories)
