
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

(rights.\ndatabasechangelog) as (rights_databasechangelog) << Table >>
(rights.\ndatabasechangeloglock) as (rights_databasechangeloglock) << Table >>
(rights.\nrig_matrix_lcd) as (rights_rig_matrix_lcd) << Table >>
(rights.\nrig_title_rights) as (rights_rig_title_rights) << Table >>
(rights.\nrig_title_streaming_cache) as (rights_rig_title_streaming_cache) << Table >>
(rights.\nrig_title_streaming_cache_old) as (rights_rig_title_streaming_cache_old) << Table >>
(rights.\nrig_title_streaming_log) as (rights_rig_title_streaming_log) << Table >>
(rights.\nrig_tree_rights) as (rights_rig_tree_rights) << Table >>


@enduml