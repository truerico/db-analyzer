
@startuml
skinparam titleBorderRoundCorner 15
skinparam titleBorderThickness 2
skinparam titleBorderColor black
skinparam titleBackgroundColor #DDDDDD
title **:: table erd1- rds copyright © ::**
!theme _none_
skinparam shadowing False
left to right direction
skinparam linetype ortho
skinparam packageStyle rectangle
hide circle



entity "<&grid-three-up>** OT.CONTACTS**" as OT.CONTACTS { 
  + **(pk) CONTACT_ID : NUMBER**
  --
  - FIRST_NAME : VARCHAR2
  - LAST_NAME : VARCHAR2
  - EMAIL : VARCHAR2
  - PHONE : VARCHAR2
  --
  + **(fk) CUSTOMER_ID : NUMBER**
  ==
  <&pie-chart>** stats**
      total rows : 319
      total cols : 6
      data size : 64 KB
      index size : 64 KB
  --
}


entity "<&grid-three-up>** OT.COUNTRIES**" as OT.COUNTRIES { 
  + **(pk) COUNTRY_ID : CHAR**
  --
  - COUNTRY_NAME : VARCHAR2
  --
  + **(fk) REGION_ID : NUMBER**
  ==
  <&pie-chart>** stats**
      total rows : 25
      total cols : 3
      data size : 64 KB
      index size : 64 KB
  --
}


entity "<&grid-three-up>** OT.CUSTOMERS**" as OT.CUSTOMERS { 
  + **(pk) CUSTOMER_ID : NUMBER**
  --
  - NAME : VARCHAR2
  - ADDRESS : VARCHAR2
  - WEBSITE : VARCHAR2
  - CREDIT_LIMIT : NUMBER
  ==
  <&pie-chart>** stats**
      total rows : 319
      total cols : 5
      data size : 64 KB
      index size : 64 KB
  --
}


entity "<&grid-three-up>** OT.EMPLOYEES**" as OT.EMPLOYEES { 
  + **(pk) EMPLOYEE_ID : NUMBER**
  --
  - FIRST_NAME : VARCHAR2
  - LAST_NAME : VARCHAR2
  - EMAIL : VARCHAR2
  - PHONE : VARCHAR2
  - HIRE_DATE : DATE
  - JOB_TITLE : VARCHAR2
  --
  + **(fk) MANAGER_ID : NUMBER**
  ==
  <&pie-chart>** stats**
      total rows : 107
      total cols : 8
      data size : 64 KB
      index size : 64 KB
  --
}


entity "<&grid-three-up>** OT.INVENTORIES**" as OT.INVENTORIES { 
  + **(pk) WAREHOUSE_ID : NUMBER**
  + **(pk) PRODUCT_ID : NUMBER**
  --
  - QUANTITY : NUMBER
  ==
  <&pie-chart>** stats**
      total rows : 1,112
      total cols : 3
      data size : 64 KB
      index size : 64 KB
  --
}


entity "<&grid-three-up>** OT.LOCATIONS**" as OT.LOCATIONS { 
  + **(pk) LOCATION_ID : NUMBER**
  --
  - ADDRESS : VARCHAR2
  - POSTAL_CODE : VARCHAR2
  - CITY : VARCHAR2
  - STATE : VARCHAR2
  --
  + **(fk) COUNTRY_ID : CHAR**
  ==
  <&pie-chart>** stats**
      total rows : 23
      total cols : 6
      data size : 64 KB
      index size : 64 KB
  --
}


entity "<&grid-three-up>** OT.ORDERS**" as OT.ORDERS { 
  + **(pk) ORDER_ID : NUMBER**
  --
  - STATUS : VARCHAR2
  - ORDER_DATE : DATE
  --
  + **(fk) CUSTOMER_ID : NUMBER**
  + **(fk) SALESMAN_ID : NUMBER**
  ==
  <&pie-chart>** stats**
      total rows : 105
      total cols : 5
      data size : 64 KB
      index size : 64 KB
  --
}


entity "<&grid-three-up>** OT.ORDER_ITEMS**" as OT.ORDER_ITEMS { 
  + **(pk) ITEM_ID : NUMBER**
  + **(pk) ORDER_ID : NUMBER**
  --
  - QUANTITY : NUMBER
  - UNIT_PRICE : NUMBER
  --
  + **(fk) PRODUCT_ID : NUMBER**
  ==
  <&pie-chart>** stats**
      total rows : 665
      total cols : 5
      data size : 64 KB
      index size : 64 KB
  --
}


entity "<&grid-three-up>** OT.PRODUCTS**" as OT.PRODUCTS { 
  + **(pk) PRODUCT_ID : NUMBER**
  --
  - PRODUCT_NAME : VARCHAR2
  - DESCRIPTION : VARCHAR2
  - STANDARD_COST : NUMBER
  - LIST_PRICE : NUMBER
  --
  + **(fk) CATEGORY_ID : NUMBER**
  ==
  <&pie-chart>** stats**
      total rows : 288
      total cols : 6
      data size : 64 KB
      index size : 64 KB
  --
}


entity "<&grid-three-up>** OT.PRODUCT_CATEGORIES**" as OT.PRODUCT_CATEGORIES { 
  + **(pk) CATEGORY_ID : NUMBER**
  --
  - CATEGORY_NAME : VARCHAR2
  ==
  <&pie-chart>** stats**
      total rows : 5
      total cols : 2
      data size : 64 KB
      index size : 64 KB
  --
}


entity "<&grid-three-up>** OT.REGIONS**" as OT.REGIONS { 
  + **(pk) REGION_ID : NUMBER**
  --
  - REGION_NAME : VARCHAR2
  ==
  <&pie-chart>** stats**
      total rows : 4
      total cols : 2
      data size : 64 KB
      index size : 64 KB
  --
}


entity "<&grid-three-up>** OT.WAREHOUSES**" as OT.WAREHOUSES { 
  + **(pk) WAREHOUSE_ID : NUMBER**
  --
  - WAREHOUSE_NAME : VARCHAR2
  --
  + **(fk) LOCATION_ID : NUMBER**
  ==
  <&pie-chart>** stats**
      total rows : 9
      total cols : 3
      data size : 64 KB
      index size : 64 KB
  --
}

OT.ORDERS ||.d.o{ OT.CUSTOMERS
OT.PRODUCTS ||.l.o{ OT.PRODUCT_CATEGORIES
OT.WAREHOUSES ||.u.o{ OT.LOCATIONS
OT.ORDERS ||.r.o{ OT.EMPLOYEES
OT.EMPLOYEES ||.d.o{ OT.EMPLOYEES
OT.LOCATIONS ||.l.o{ OT.COUNTRIES
OT.INVENTORIES ||.u.o{ OT.PRODUCTS
OT.ORDER_ITEMS ||.r.o{ OT.ORDERS
OT.ORDER_ITEMS ||.d.o{ OT.PRODUCTS
OT.CONTACTS ||.l.o{ OT.CUSTOMERS
OT.COUNTRIES ||.u.o{ OT.REGIONS
OT.INVENTORIES ||.r.o{ OT.WAREHOUSES

'# manual relation section 
tbl_aaa .. tbl_bbb

@enduml