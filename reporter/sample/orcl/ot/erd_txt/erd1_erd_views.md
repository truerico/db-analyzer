
@startuml
skinparam titleBorderRoundCorner 15
skinparam titleBorderThickness 2
skinparam titleBorderColor black
skinparam titleBackgroundColor #DDDDDD
title **:: view erd1 - rds copyright © ::**
!theme _none_
skinparam shadowing False
left to right direction
skinparam linetype ortho
skinparam packageStyle rectangle
hide circle


entity "<&grid-three-up>** OT.COUNTRY_LOCATIONS**" as OT.COUNTRY_LOCATIONS { 
  - COUNTRY_ID : CHAR
  - COUNTRY_NAME : VARCHAR2
  - REGION_ID : NUMBER
  - ADDRESS : VARCHAR2
  - POSTAL_CODE : VARCHAR2
  - STATE : VARCHAR2
  ==
  <&pie-chart>** stats**
      total rows : 23
      total cols : 6
  --
}


entity "<&grid-three-up>** OT.ORDER_DETAILS**" as OT.ORDER_DETAILS { 
  - ORDER_ID : NUMBER
  - CUSTOMER_ID : NUMBER
  - STATUS : VARCHAR2
  - SALESMAN_ID : NUMBER
  - ORDER_DATE : DATE
  - ITEM_ID : NUMBER
  - QUANTITY : NUMBER
  - UNIT_PRICE : NUMBER
  ==
  <&pie-chart>** stats**
      total rows : 665
      total cols : 8
  --
}
OT.COUNTRY_LOCATIONS ||.d.o{ OT.COUNTRIES
OT.COUNTRY_LOCATIONS ||.l.o{ OT.LOCATIONS
OT.ORDER_DETAILS ||.u.o{ OT.ORDERS
OT.ORDER_DETAILS ||.r.o{ OT.ORDER_ITEMS


'# manual relation section 
vw_aaa .. vw_bbb

@enduml