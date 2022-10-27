
@startuml
skinparam titleBorderRoundCorner 15
skinparam titleBorderThickness 2
skinparam titleBorderColor black
skinparam titleBackgroundColor #DDDDDD
title **:: table erd1 © ::**
!theme _none_
skinparam shadowing False
left to right direction
skinparam linetype polyline
skinparam packageStyle rectangle
hide circle



entity "<&grid-three-up>** dbo.DatabaseLog**" as dbo.DatabaseLog { 
  + **(pk) DatabaseLogID : int**
  --
  - PostTime : datetime
  - DatabaseUser : nvarchar
  - Event : nvarchar
  - Schema : nvarchar
  - Object : nvarchar
  - TSQL : nvarchar
  - XmlEvent : xml
  ==
  <&pie-chart>** stats**
      total rows : 1,596
      total cols : 8
      data size : 6,544 KB
      index size : 48 KB
  --
}


entity "<&grid-three-up>** dbo.ErrorLog**" as dbo.ErrorLog { 
  + **(pk) ErrorLogID : int**
  --
  - ErrorTime : datetime
  - UserName : nvarchar
  - ErrorNumber : int
  - ErrorSeverity : int
  - ErrorState : int
  - ErrorProcedure : nvarchar
  - ErrorLine : int
  - ErrorMessage : nvarchar
  ==
  <&pie-chart>** stats**
      total rows : 0
      total cols : 9
      data size : 0 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** dbo.AWBuildVersion**" as dbo.AWBuildVersion { 
  + **(pk) SystemInformationID : tinyint**
  --
  - Database Version : nvarchar
  - VersionDate : datetime
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 1
      total cols : 4
      data size : 72 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** Production.TransactionHistoryArchive**" as Production.TransactionHistoryArchive { 
  + **(pk) TransactionID : int**
  --
  - ProductID : int
  - ReferenceOrderID : int
  - ReferenceOrderLineID : int
  - TransactionDate : datetime
  - TransactionType : nchar
  - Quantity : int
  - ActualCost : money
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 89,253
      total cols : 9
      data size : 5,064 KB
      index size : 2,864 KB
  --
}


@enduml