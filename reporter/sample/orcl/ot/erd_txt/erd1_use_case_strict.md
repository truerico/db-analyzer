
@startuml
skinparam titleBorderRoundCorner 15
skinparam titleBorderThickness 2
skinparam titleBorderColor black
skinparam titleBackgroundColor #DDDDDD
title **:: use case - rds copyright © ::**
!theme _none_
skinparam shadowing False
left to right direction
skinparam linetype ortho
skinparam usecase {
BackgroundColor<< Table >> lightgrey
BackgroundColor<< View >> YellowGreen
}

' TABLES ENTITIES 

(ot.\ncontacts) as (ot_contacts) << Table >>
(ot.\ncountries) as (ot_countries) << Table >>
(ot.\ncustomers) as (ot_customers) << Table >>
(ot.\nemployees) as (ot_employees) << Table >>
(ot.\ninventories) as (ot_inventories) << Table >>
(ot.\nlocations) as (ot_locations) << Table >>
(ot.\norders) as (ot_orders) << Table >>
(ot.\norder_items) as (ot_order_items) << Table >>
(ot.\nproducts) as (ot_products) << Table >>
(ot.\nproduct_categories) as (ot_product_categories) << Table >>
(ot.\nregions) as (ot_regions) << Table >>
(ot.\nwarehouses) as (ot_warehouses) << Table >>

' VIEWS 

(ot.\ncountry_locations) as (ot_country_locations) << View >>
(ot.\norder_details) as (ot_order_details) << View >>

' VIEWS RELATED OBJECTS 

(ot_country_locations)-d->(ot_countries)
(ot_country_locations)-l->(ot_locations)
(ot_order_details)-u->(ot_orders)
(ot_order_details)-r->(ot_order_items)

' FKEYS 

(ot_customers)-d->(ot_orders) 
(ot_product_categories)-l->(ot_products) 
(ot_locations)-u->(ot_warehouses) 
(ot_employees)-r->(ot_orders) 
(ot_employees)-d->(ot_employees) 
(ot_countries)-l->(ot_locations) 
(ot_products)-u->(ot_inventories) 
(ot_orders)-r->(ot_order_items) 
(ot_products)-d->(ot_order_items) 
(ot_customers)-l->(ot_contacts) 
(ot_regions)-u->(ot_countries) 
(ot_warehouses)-r->(ot_inventories) 


@enduml