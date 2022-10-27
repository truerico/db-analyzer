
@startuml
skinparam titleBorderRoundCorner 15
skinparam titleBorderThickness 2
skinparam titleBorderColor black
skinparam titleBackgroundColor #DDDDDD
title **:: use case © ::**
!theme _none_
skinparam shadowing False
left to right direction
skinparam linetype polyline
skinparam usecase {
BackgroundColor<< Table >> lightgrey
BackgroundColor<< View >> YellowGreen
}

' TABLES ENTITIES 

(dbo.\ndatabaselog) as (dbo_databaselog) << Table >>
(dbo.\nerrorlog) as (dbo_errorlog) << Table >>
(dbo.\nawbuildversion) as (dbo_awbuildversion) << Table >>
(production.\ntransactionhistoryarchive) as (production_transactionhistoryarchive) << Table >>


@enduml