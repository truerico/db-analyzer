
@startuml
skinparam titleBorderRoundCorner 15
skinparam titleBorderThickness 2
skinparam titleBorderColor black
skinparam titleBackgroundColor #DDDDDD
title **:: table erd1 © ::**
!theme _none_
skinparam shadowing False
left to right direction
skinparam linetype ortho
skinparam packageStyle rectangle
hide circle



entity "<&grid-three-up>** classicmodels.customers**" as classicmodels.customers { 
  + **(pk) customerNumber : int**
  --
  - customerName : varchar
  - contactLastName : varchar
  - contactFirstName : varchar
  - phone : varchar
  - addressLine1 : varchar
  - addressLine2 : varchar
  - city : varchar
  - state : varchar
  - postalCode : varchar
  - country : varchar
  - creditLimit : decimal
  --
  + **(fk) salesRepEmployeeNumber : int**
  ==
  <&pie-chart>** stats**
      total rows : 122
      total cols : 13
      data size : 16 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** classicmodels.employees**" as classicmodels.employees { 
  + **(pk) employeeNumber : int**
  --
  - lastName : varchar
  - firstName : varchar
  - extension : varchar
  - email : varchar
  - jobTitle : varchar
  --
  + **(fk) officeCode : varchar**
  + **(fk) reportsTo : int**
  ==
  <&pie-chart>** stats**
      total rows : 23
      total cols : 8
      data size : 16 KB
      index size : 33 KB
  --
}


entity "<&grid-three-up>** classicmodels.offices**" as classicmodels.offices { 
  + **(pk) officeCode : varchar**
  --
  - city : varchar
  - phone : varchar
  - addressLine1 : varchar
  - addressLine2 : varchar
  - state : varchar
  - country : varchar
  - postalCode : varchar
  - territory : varchar
  ==
  <&pie-chart>** stats**
      total rows : 7
      total cols : 9
      data size : 16 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** classicmodels.orderdetails**" as classicmodels.orderdetails { 
  + **(pk) orderNumber : int**
  + **(pk) productCode : varchar**
  --
  - quantityOrdered : int
  - priceEach : decimal
  - orderLineNumber : smallint
  ==
  <&pie-chart>** stats**
      total rows : 2,996
      total cols : 5
      data size : 164 KB
      index size : 82 KB
  --
}


entity "<&grid-three-up>** classicmodels.orders**" as classicmodels.orders { 
  + **(pk) orderNumber : int**
  --
  - orderDate : date
  - requiredDate : date
  - shippedDate : date
  - status : varchar
  - comments : text
  --
  + **(fk) customerNumber : int**
  ==
  <&pie-chart>** stats**
      total rows : 326
      total cols : 7
      data size : 49 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** classicmodels.payments**" as classicmodels.payments { 
  + **(pk) customerNumber : int**
  + **(pk) checkNumber : varchar**
  --
  - paymentDate : date
  - amount : decimal
  ==
  <&pie-chart>** stats**
      total rows : 273
      total cols : 4
      data size : 16 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** classicmodels.productlines**" as classicmodels.productlines { 
  + **(pk) productLine : varchar**
  --
  - textDescription : varchar
  - htmlDescription : mediumtext
  - image : mediumblob
  ==
  <&pie-chart>** stats**
      total rows : 7
      total cols : 4
      data size : 16 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** classicmodels.products**" as classicmodels.products { 
  + **(pk) productCode : varchar**
  --
  - productName : varchar
  - productScale : varchar
  - productVendor : varchar
  - productDescription : text
  - quantityInStock : smallint
  - buyPrice : decimal
  - MSRP : decimal
  --
  + **(fk) productLine : varchar**
  ==
  <&pie-chart>** stats**
      total rows : 110
      total cols : 9
      data size : 66 KB
      index size : 16 KB
  --
}

classicmodels.customers ||.d.o{ classicmodels.employees : salesrepemployeenumber
classicmodels.employees ||.l.o{ classicmodels.employees : reportsto
classicmodels.employees ||.u.o{ classicmodels.offices : officecode
classicmodels.orderdetails ||.r.o{ classicmodels.orders : ordernumber
classicmodels.orderdetails ||.d.o{ classicmodels.products : productcode
classicmodels.orders ||.l.o{ classicmodels.customers : customernumber
classicmodels.payments ||.u.o{ classicmodels.customers : customernumber
classicmodels.products ||.r.o{ classicmodels.productlines : productline

'# manual relation section 
tbl_aaa .. tbl_bbb

@enduml