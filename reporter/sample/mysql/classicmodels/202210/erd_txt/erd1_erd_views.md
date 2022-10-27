
@startuml
skinparam titleBorderRoundCorner 15
skinparam titleBorderThickness 2
skinparam titleBorderColor black
skinparam titleBackgroundColor #DDDDDD
title **:: view erd1 © ::**
!theme _none_
skinparam shadowing False
left to right direction
skinparam linetype ortho
skinparam packageStyle rectangle
hide circle


entity "<&grid-three-up>** classicmodels.aboveavgproducts**" as classicmodels.aboveavgproducts { 
  - productCode : varchar
  - productName : varchar
  - buyPrice : decimal
  ==
  <&pie-chart>** stats**
      total rows : 54
      total cols : 3
  --
}


entity "<&grid-three-up>** classicmodels.bigsalesorder**" as classicmodels.bigsalesorder { 
  - orderNumber : int
  - total : decimal
  ==
  <&pie-chart>** stats**
      total rows : 3
      total cols : 2
  --
}


entity "<&grid-three-up>** classicmodels.customerorders**" as classicmodels.customerorders { 
  - orderNumber : int
  - customerName : varchar
  - total : decimal
  ==
  <&pie-chart>** stats**
      total rows : 326
      total cols : 3
  --
}


entity "<&grid-three-up>** classicmodels.customerorderstats**" as classicmodels.customerorderstats { 
  - customerName : varchar
  - orderCount : bigint
  ==
  <&pie-chart>** stats**
      total rows : 98
      total cols : 2
  --
}


entity "<&grid-three-up>** classicmodels.customerpayments**" as classicmodels.customerpayments { 
  - customerName : varchar
  - checkNumber : varchar
  - paymentDate : date
  - amount : decimal
  ==
  <&pie-chart>** stats**
      total rows : 273
      total cols : 4
  --
}


entity "<&grid-three-up>** classicmodels.daysofweek**" as classicmodels.daysofweek { 
  - day : varchar
  ==
  <&pie-chart>** stats**
      total rows : 7
      total cols : 1
  --
}


entity "<&grid-three-up>** classicmodels.saleperorder**" as classicmodels.saleperorder { 
  - orderNumber : int
  - total : decimal
  ==
  <&pie-chart>** stats**
      total rows : 326
      total cols : 2
  --
}
classicmodels.aboveavgproducts ||.d.o{ classicmodels.products
classicmodels.bigsalesorder ||.l.o{ classicmodels.saleperorder
classicmodels.customerorders ||.u.o{ classicmodels.customers
classicmodels.customerorders ||.r.o{ classicmodels.orderdetails
classicmodels.customerorders ||.d.o{ classicmodels.orders
classicmodels.customerorderstats ||.l.o{ classicmodels.customers
classicmodels.customerorderstats ||.u.o{ classicmodels.orders
classicmodels.customerpayments ||.r.o{ classicmodels.customers
classicmodels.customerpayments ||.d.o{ classicmodels.payments
classicmodels.saleperorder ||.l.o{ classicmodels.orderdetails


'# manual relation section 
vw_aaa .. vw_bbb

@enduml