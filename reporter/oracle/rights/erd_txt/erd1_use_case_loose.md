
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


' VIEWS 

(rights.\ngtd_query_v) as (rights_gtd_query_v) << View >>
(rights.\ngtp_query_v) as (rights_gtp_query_v) << View >>
(rights.\ngtp_site_title_intranet_v) as (rights_gtp_site_title_intranet_v) << View >>
(rights.\ngtp_site_title_v) as (rights_gtp_site_title_v) << View >>
(rights.\ngtp_sit_tit_mediasphere_v) as (rights_gtp_sit_tit_mediasphere_v) << View >>
(rights.\nrig_contract_partenaire_v) as (rights_rig_contract_partenaire_v) << View >>
(rights.\nrig_contract_type_v) as (rights_rig_contract_type_v) << View >>
(rights.\nrig_dom_sale_qualifier_v) as (rights_rig_dom_sale_qualifier_v) << View >>
(rights.\nrig_market_v) as (rights_rig_market_v) << View >>
(rights.\nrig_or_contract_title_v) as (rights_rig_or_contract_title_v) << View >>
(rights.\nrig_partenaire_v) as (rights_rig_partenaire_v) << View >>
(rights.\nrig_part_relation_v) as (rights_rig_part_relation_v) << View >>
(rights.\nrig_sale_leaf_lang_v) as (rights_rig_sale_leaf_lang_v) << View >>
(rights.\nrig_sale_leaf_mark_v) as (rights_rig_sale_leaf_mark_v) << View >>
(rights.\nrig_sale_leaf_supp_v) as (rights_rig_sale_leaf_supp_v) << View >>
(rights.\nrig_sale_leaf_terr_v) as (rights_rig_sale_leaf_terr_v) << View >>
(rights.\nrig_support_v) as (rights_rig_support_v) << View >>
(rights.\nrig_title_partenaire_v) as (rights_rig_title_partenaire_v) << View >>
(rights.\nrig_title_relations_v) as (rights_rig_title_relations_v) << View >>
(rights.\nrig_tree_distributor_v) as (rights_rig_tree_distributor_v) << View >>
(rights.\nrig_tree_rights_v) as (rights_rig_tree_rights_v) << View >>

' VIEWS RELATED OBJECTS 

(rights_gtd_query_v)-d->(public_fmt_format)
(rights_gtd_query_v)-l->(rights_gtd_site_title)
(rights_gtd_query_v)-u->(public_syn_registery)
(rights_gtp_query_v)-r->(public_fmt_format)
(rights_gtp_query_v)-d->(rights_gtp_site_title)
(rights_gtp_query_v)-l->(public_syn_registery)
(rights_gtp_site_title_intranet_v)-u->(rights_gtd_site_title)
(rights_gtp_site_title_intranet_v)-r->(rights_gtp_site_title)
(rights_gtp_site_title_v)-d->(rights_gtd_site_title)
(rights_gtp_site_title_v)-l->(rights_gtp_site_title)
(rights_gtp_sit_tit_mediasphere_v)-u->(rights_gtd_site_title)
(rights_gtp_sit_tit_mediasphere_v)-r->(rights_gtp_site_title)
(rights_rig_contract_partenaire_v)-d->(rights_coll_rig_contract_partenaire_v)
(rights_rig_contract_type_v)-l->(rights_rig_contract_type)
(rights_rig_contract_type_v)-u->(rights_rig_contract_type_tl)
(rights_rig_dom_sale_qualifier_v)-r->(rights_rig_domain)
(rights_rig_dom_sale_qualifier_v)-d->(rights_rig_domain_tl)
(rights_rig_market_v)-l->(rights_rig_market)
(rights_rig_market_v)-u->(rights_rig_market_tl)
(rights_rig_or_contract_title_v)-r->(rights_rig_contract)
(rights_rig_or_contract_title_v)-d->(rights_rig_contract_section)
(rights_rig_or_contract_title_v)-l->(rights_rig_leaf_sale_qualifier)
(rights_rig_or_contract_title_v)-u->(rights_rig_leaf_title)
(rights_rig_or_contract_title_v)-r->(rights_rig_tree_rights_v)
(rights_rig_partenaire_v)-d->(rights_rig_contract_partenaire_v)
(rights_rig_part_relation_v)-l->(public_syn_registery_relation)
(rights_rig_sale_leaf_lang_v)-u->(rights_rig_extend_tlms)
(rights_rig_sale_leaf_lang_v)-r->(rights_rig_leaf_territory)
(rights_rig_sale_leaf_mark_v)-d->(rights_rig_extend_tlms)
(rights_rig_sale_leaf_mark_v)-l->(rights_rig_leaf_market)
(rights_rig_sale_leaf_supp_v)-u->(rights_rig_extend_tlms)
(rights_rig_sale_leaf_supp_v)-r->(rights_rig_leaf_support)
(rights_rig_sale_leaf_terr_v)-d->(rights_rig_extend_tlms)
(rights_rig_sale_leaf_terr_v)-l->(rights_rig_leaf_territory)
(rights_rig_support_v)-u->(rights_rig_support)
(rights_rig_support_v)-r->(rights_rig_support_tl)
(rights_rig_title_partenaire_v)-d->(rights_rig_contract_partenaire_v)
(rights_rig_title_relations_v)-l->(rights_rig_title_relations)
(rights_rig_title_relations_v)-u->(rights_rig_title_rights)
(rights_rig_tree_distributor_v)-r->(rights_rig_contract_section)
(rights_rig_tree_distributor_v)-d->(rights_rig_leaf_distributor)
(rights_rig_tree_distributor_v)-l->(rights_rig_tree_rights)
(rights_rig_tree_distributor_v)-u->(rights_rig_tree_structure)
(rights_rig_tree_rights_v)-r->(rights_rig_tree_rights)
(rights_rig_tree_rights_v)-d->(rights_rig_tree_structure)

' FKEYS 



@enduml