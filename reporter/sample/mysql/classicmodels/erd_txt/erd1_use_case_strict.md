
@startuml
skinparam titleBorderRoundCorner 15
skinparam titleBorderThickness 2
skinparam titleBorderColor black
skinparam titleBackgroundColor #DDDDDD
title **:: use case © ::**
!theme _none_
skinparam shadowing False
left to right direction
skinparam linetype ortho
skinparam usecase {
BackgroundColor<< Table >> lightgrey
BackgroundColor<< View >> YellowGreen
}

' TABLES ENTITIES 

(classicmodels.\ncustomers) as (classicmodels_customers) << Table >>
(classicmodels.\nemployees) as (classicmodels_employees) << Table >>
(classicmodels.\noffices) as (classicmodels_offices) << Table >>
(classicmodels.\norderdetails) as (classicmodels_orderdetails) << Table >>
(classicmodels.\norders) as (classicmodels_orders) << Table >>
(classicmodels.\npayments) as (classicmodels_payments) << Table >>
(classicmodels.\nproductlines) as (classicmodels_productlines) << Table >>
(classicmodels.\nproducts) as (classicmodels_products) << Table >>

' VIEWS 

(classicmodels.\naboveavgproducts) as (classicmodels_aboveavgproducts) << View >>
(classicmodels.\nbigsalesorder) as (classicmodels_bigsalesorder) << View >>
(classicmodels.\ncustomerorders) as (classicmodels_customerorders) << View >>
(classicmodels.\ncustomerorderstats) as (classicmodels_customerorderstats) << View >>
(classicmodels.\ncustomerpayments) as (classicmodels_customerpayments) << View >>
(classicmodels.\ndaysofweek) as (classicmodels_daysofweek) << View >>
(classicmodels.\nsaleperorder) as (classicmodels_saleperorder) << View >>

' VIEWS RELATED OBJECTS 

(classicmodels_aboveavgproducts)-d->(classicmodels_products)
(classicmodels_bigsalesorder)-l->(classicmodels_saleperorder)
(classicmodels_customerorders)-u->(classicmodels_customers)
(classicmodels_customerorders)-r->(classicmodels_orderdetails)
(classicmodels_customerorders)-d->(classicmodels_orders)
(classicmodels_customerorderstats)-l->(classicmodels_customers)
(classicmodels_customerorderstats)-u->(classicmodels_orders)
(classicmodels_customerpayments)-r->(classicmodels_customers)
(classicmodels_customerpayments)-d->(classicmodels_payments)
(classicmodels_saleperorder)-l->(classicmodels_orderdetails)

' FKEYS 

(classicmodels_employees)-u->(classicmodels_customers) : 'salesrepemployeenumber' 
(classicmodels_employees)-r->(classicmodels_employees) : 'reportsto' 
(classicmodels_offices)-d->(classicmodels_employees) : 'officecode' 
(classicmodels_orders)-l->(classicmodels_orderdetails) : 'ordernumber' 
(classicmodels_products)-u->(classicmodels_orderdetails) : 'productcode' 
(classicmodels_customers)-r->(classicmodels_orders) : 'customernumber' 
(classicmodels_customers)-d->(classicmodels_payments) : 'customernumber' 
(classicmodels_productlines)-l->(classicmodels_products) : 'productline' 


@enduml