
@startuml
skinparam titleBorderRoundCorner 15
skinparam titleBorderThickness 2
skinparam titleBorderColor black
skinparam titleBackgroundColor #DDDDDD
title **:: use case - © ::**
!theme _none_
skinparam shadowing False
top to bottom direction
skinparam linetype ortho
skinparam usecase {
BackgroundColor<< Index >> lightgrey
BackgroundColor<< View >> YellowGreen
}

' TABLES ENTITIES 

(db_logs) as (db_logs) << Index >>
(db_movies) as (db_movies) << Index >>
(db_accounts) as (db_accounts) << Index >>
(db_shakespeare) as (db_shakespeare) << Index >>

' FKEYS 



'# manual relation section 
tbl_aaa .. tbl_bbb

@enduml