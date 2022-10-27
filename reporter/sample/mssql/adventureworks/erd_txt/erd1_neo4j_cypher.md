MATCH (n) DETACH DELETE n ;

// TABLES ENTITIES 

CREATE (sales_salestaxrate:Table {title:'salestaxrate', table_schema:'sales', is_orphan_table:'0'})
CREATE (sales_personcreditcard:Table {title:'personcreditcard', table_schema:'sales', is_orphan_table:'0'})
CREATE (person_personphone:Table {title:'personphone', table_schema:'person', is_orphan_table:'0'})
CREATE (sales_salesterritory:Table {title:'salesterritory', table_schema:'sales', is_orphan_table:'0'})
CREATE (person_phonenumbertype:Table {title:'phonenumbertype', table_schema:'person', is_orphan_table:'0'})
CREATE (production_product:Table {title:'product', table_schema:'production', is_orphan_table:'0'})
CREATE (sales_salesterritoryhistory:Table {title:'salesterritoryhistory', table_schema:'sales', is_orphan_table:'0'})
CREATE (production_scrapreason:Table {title:'scrapreason', table_schema:'production', is_orphan_table:'0'})
CREATE (humanresources_shift:Table {title:'shift', table_schema:'humanresources', is_orphan_table:'0'})
CREATE (production_productcategory:Table {title:'productcategory', table_schema:'production', is_orphan_table:'0'})
CREATE (purchasing_shipmethod:Table {title:'shipmethod', table_schema:'purchasing', is_orphan_table:'0'})
CREATE (production_productcosthistory:Table {title:'productcosthistory', table_schema:'production', is_orphan_table:'0'})
CREATE (production_productdescription:Table {title:'productdescription', table_schema:'production', is_orphan_table:'0'})
CREATE (sales_shoppingcartitem:Table {title:'shoppingcartitem', table_schema:'sales', is_orphan_table:'0'})
CREATE (production_productdocument:Table {title:'productdocument', table_schema:'production', is_orphan_table:'0'})
CREATE (dbo_databaselog:Table {title:'databaselog', table_schema:'dbo', is_orphan_table:'1'})
CREATE (production_productinventory:Table {title:'productinventory', table_schema:'production', is_orphan_table:'0'})
CREATE (sales_specialoffer:Table {title:'specialoffer', table_schema:'sales', is_orphan_table:'0'})
CREATE (dbo_errorlog:Table {title:'errorlog', table_schema:'dbo', is_orphan_table:'1'})
CREATE (production_productlistpricehistory:Table {title:'productlistpricehistory', table_schema:'production', is_orphan_table:'0'})
CREATE (person_address:Table {title:'address', table_schema:'person', is_orphan_table:'0'})
CREATE (sales_specialofferproduct:Table {title:'specialofferproduct', table_schema:'sales', is_orphan_table:'0'})
CREATE (production_productmodel:Table {title:'productmodel', table_schema:'production', is_orphan_table:'0'})
CREATE (person_addresstype:Table {title:'addresstype', table_schema:'person', is_orphan_table:'0'})
CREATE (person_stateprovince:Table {title:'stateprovince', table_schema:'person', is_orphan_table:'0'})
CREATE (production_productmodelillustration:Table {title:'productmodelillustration', table_schema:'production', is_orphan_table:'0'})
CREATE (dbo_awbuildversion:Table {title:'awbuildversion', table_schema:'dbo', is_orphan_table:'1'})
CREATE (production_productmodelproductdescriptionculture:Table {title:'productmodelproductdescriptionculture', table_schema:'production', is_orphan_table:'0'})
CREATE (production_billofmaterials:Table {title:'billofmaterials', table_schema:'production', is_orphan_table:'0'})
CREATE (sales_store:Table {title:'store', table_schema:'sales', is_orphan_table:'0'})
CREATE (production_productphoto:Table {title:'productphoto', table_schema:'production', is_orphan_table:'0'})
CREATE (production_productproductphoto:Table {title:'productproductphoto', table_schema:'production', is_orphan_table:'0'})
CREATE (production_transactionhistory:Table {title:'transactionhistory', table_schema:'production', is_orphan_table:'0'})
CREATE (production_productreview:Table {title:'productreview', table_schema:'production', is_orphan_table:'0'})
CREATE (person_businessentity:Table {title:'businessentity', table_schema:'person', is_orphan_table:'0'})
CREATE (production_transactionhistoryarchive:Table {title:'transactionhistoryarchive', table_schema:'production', is_orphan_table:'1'})
CREATE (production_productsubcategory:Table {title:'productsubcategory', table_schema:'production', is_orphan_table:'0'})
CREATE (person_businessentityaddress:Table {title:'businessentityaddress', table_schema:'person', is_orphan_table:'0'})
CREATE (purchasing_productvendor:Table {title:'productvendor', table_schema:'purchasing', is_orphan_table:'0'})
CREATE (person_businessentitycontact:Table {title:'businessentitycontact', table_schema:'person', is_orphan_table:'0'})
CREATE (production_unitmeasure:Table {title:'unitmeasure', table_schema:'production', is_orphan_table:'0'})
CREATE (purchasing_vendor:Table {title:'vendor', table_schema:'purchasing', is_orphan_table:'0'})
CREATE (person_contacttype:Table {title:'contacttype', table_schema:'person', is_orphan_table:'0'})
CREATE (sales_countryregioncurrency:Table {title:'countryregioncurrency', table_schema:'sales', is_orphan_table:'0'})
CREATE (person_countryregion:Table {title:'countryregion', table_schema:'person', is_orphan_table:'0'})
CREATE (production_workorder:Table {title:'workorder', table_schema:'production', is_orphan_table:'0'})
CREATE (purchasing_purchaseorderdetail:Table {title:'purchaseorderdetail', table_schema:'purchasing', is_orphan_table:'0'})
CREATE (sales_creditcard:Table {title:'creditcard', table_schema:'sales', is_orphan_table:'0'})
CREATE (production_culture:Table {title:'culture', table_schema:'production', is_orphan_table:'0'})
CREATE (production_workorderrouting:Table {title:'workorderrouting', table_schema:'production', is_orphan_table:'0'})
CREATE (sales_currency:Table {title:'currency', table_schema:'sales', is_orphan_table:'0'})
CREATE (purchasing_purchaseorderheader:Table {title:'purchaseorderheader', table_schema:'purchasing', is_orphan_table:'0'})
CREATE (sales_currencyrate:Table {title:'currencyrate', table_schema:'sales', is_orphan_table:'0'})
CREATE (sales_customer:Table {title:'customer', table_schema:'sales', is_orphan_table:'0'})
CREATE (humanresources_department:Table {title:'department', table_schema:'humanresources', is_orphan_table:'0'})
CREATE (production_document:Table {title:'document', table_schema:'production', is_orphan_table:'0'})
CREATE (sales_salesorderdetail:Table {title:'salesorderdetail', table_schema:'sales', is_orphan_table:'0'})
CREATE (person_emailaddress:Table {title:'emailaddress', table_schema:'person', is_orphan_table:'0'})
CREATE (humanresources_employee:Table {title:'employee', table_schema:'humanresources', is_orphan_table:'0'})
CREATE (sales_salesorderheader:Table {title:'salesorderheader', table_schema:'sales', is_orphan_table:'0'})
CREATE (humanresources_employeedepartmenthistory:Table {title:'employeedepartmenthistory', table_schema:'humanresources', is_orphan_table:'0'})
CREATE (humanresources_employeepayhistory:Table {title:'employeepayhistory', table_schema:'humanresources', is_orphan_table:'0'})
CREATE (sales_salesorderheadersalesreason:Table {title:'salesorderheadersalesreason', table_schema:'sales', is_orphan_table:'0'})
CREATE (sales_salesperson:Table {title:'salesperson', table_schema:'sales', is_orphan_table:'0'})
CREATE (production_illustration:Table {title:'illustration', table_schema:'production', is_orphan_table:'0'})
CREATE (humanresources_jobcandidate:Table {title:'jobcandidate', table_schema:'humanresources', is_orphan_table:'0'})
CREATE (production_location:Table {title:'location', table_schema:'production', is_orphan_table:'0'})
CREATE (person_password:Table {title:'password', table_schema:'person', is_orphan_table:'0'})
CREATE (sales_salespersonquotahistory:Table {title:'salespersonquotahistory', table_schema:'sales', is_orphan_table:'0'})
CREATE (person_person:Table {title:'person', table_schema:'person', is_orphan_table:'0'})
CREATE (sales_salesreason:Table {title:'salesreason', table_schema:'sales', is_orphan_table:'0'})

// VIEWS 

CREATE (person_vadditionalcontactinfo:View {title:'vadditionalcontactinfo', view_schema:'person' })
CREATE (humanresources_vemployee:View {title:'vemployee', view_schema:'humanresources' })
CREATE (humanresources_vemployeedepartment:View {title:'vemployeedepartment', view_schema:'humanresources' })
CREATE (humanresources_vemployeedepartmenthistory:View {title:'vemployeedepartmenthistory', view_schema:'humanresources' })
CREATE (sales_vindividualcustomer:View {title:'vindividualcustomer', view_schema:'sales' })
CREATE (sales_vpersondemographics:View {title:'vpersondemographics', view_schema:'sales' })
CREATE (humanresources_vjobcandidate:View {title:'vjobcandidate', view_schema:'humanresources' })
CREATE (humanresources_vjobcandidateemployment:View {title:'vjobcandidateemployment', view_schema:'humanresources' })
CREATE (humanresources_vjobcandidateeducation:View {title:'vjobcandidateeducation', view_schema:'humanresources' })
CREATE (production_vproductanddescription:View {title:'vproductanddescription', view_schema:'production' })
CREATE (production_vproductmodelcatalogdescription:View {title:'vproductmodelcatalogdescription', view_schema:'production' })
CREATE (production_vproductmodelinstructions:View {title:'vproductmodelinstructions', view_schema:'production' })
CREATE (sales_vsalesperson:View {title:'vsalesperson', view_schema:'sales' })
CREATE (sales_vsalespersonsalesbyfiscalyears:View {title:'vsalespersonsalesbyfiscalyears', view_schema:'sales' })
CREATE (person_vstateprovincecountryregion:View {title:'vstateprovincecountryregion', view_schema:'person' })
CREATE (sales_vstorewithdemographics:View {title:'vstorewithdemographics', view_schema:'sales' })
CREATE (sales_vstorewithcontacts:View {title:'vstorewithcontacts', view_schema:'sales' })
CREATE (sales_vstorewithaddresses:View {title:'vstorewithaddresses', view_schema:'sales' })
CREATE (purchasing_vvendorwithcontacts:View {title:'vvendorwithcontacts', view_schema:'purchasing' })
CREATE (purchasing_vvendorwithaddresses:View {title:'vvendorwithaddresses', view_schema:'purchasing' })

// VIEWS RELATED TABLES 

CREATE (person_vadditionalcontactinfo)-[:MAKE_USE_OF {info:'person_person'}]->(person_person)
CREATE (humanresources_vemployee)-[:MAKE_USE_OF {info:'humanresources_employee'}]->(humanresources_employee)
CREATE (humanresources_vemployee)-[:MAKE_USE_OF {info:'person_address'}]->(person_address)
CREATE (humanresources_vemployee)-[:MAKE_USE_OF {info:'person_businessentityaddress'}]->(person_businessentityaddress)
CREATE (humanresources_vemployee)-[:MAKE_USE_OF {info:'person_countryregion'}]->(person_countryregion)
CREATE (humanresources_vemployee)-[:MAKE_USE_OF {info:'person_emailaddress'}]->(person_emailaddress)
CREATE (humanresources_vemployee)-[:MAKE_USE_OF {info:'person_person'}]->(person_person)
CREATE (humanresources_vemployee)-[:MAKE_USE_OF {info:'person_personphone'}]->(person_personphone)
CREATE (humanresources_vemployee)-[:MAKE_USE_OF {info:'person_phonenumbertype'}]->(person_phonenumbertype)
CREATE (humanresources_vemployee)-[:MAKE_USE_OF {info:'person_stateprovince'}]->(person_stateprovince)
CREATE (humanresources_vemployeedepartment)-[:MAKE_USE_OF {info:'humanresources_department'}]->(humanresources_department)
CREATE (humanresources_vemployeedepartment)-[:MAKE_USE_OF {info:'humanresources_employee'}]->(humanresources_employee)
CREATE (humanresources_vemployeedepartment)-[:MAKE_USE_OF {info:'humanresources_employeedepartmenthistory'}]->(humanresources_employeedepartmenthistory)
CREATE (humanresources_vemployeedepartment)-[:MAKE_USE_OF {info:'person_person'}]->(person_person)
CREATE (humanresources_vemployeedepartmenthistory)-[:MAKE_USE_OF {info:'humanresources_department'}]->(humanresources_department)
CREATE (humanresources_vemployeedepartmenthistory)-[:MAKE_USE_OF {info:'humanresources_employee'}]->(humanresources_employee)
CREATE (humanresources_vemployeedepartmenthistory)-[:MAKE_USE_OF {info:'humanresources_employeedepartmenthistory'}]->(humanresources_employeedepartmenthistory)
CREATE (humanresources_vemployeedepartmenthistory)-[:MAKE_USE_OF {info:'humanresources_shift'}]->(humanresources_shift)
CREATE (humanresources_vemployeedepartmenthistory)-[:MAKE_USE_OF {info:'person_person'}]->(person_person)
CREATE (sales_vindividualcustomer)-[:MAKE_USE_OF {info:'person_address'}]->(person_address)
CREATE (sales_vindividualcustomer)-[:MAKE_USE_OF {info:'person_addresstype'}]->(person_addresstype)
CREATE (sales_vindividualcustomer)-[:MAKE_USE_OF {info:'person_businessentityaddress'}]->(person_businessentityaddress)
CREATE (sales_vindividualcustomer)-[:MAKE_USE_OF {info:'person_countryregion'}]->(person_countryregion)
CREATE (sales_vindividualcustomer)-[:MAKE_USE_OF {info:'person_emailaddress'}]->(person_emailaddress)
CREATE (sales_vindividualcustomer)-[:MAKE_USE_OF {info:'person_person'}]->(person_person)
CREATE (sales_vindividualcustomer)-[:MAKE_USE_OF {info:'person_personphone'}]->(person_personphone)
CREATE (sales_vindividualcustomer)-[:MAKE_USE_OF {info:'person_phonenumbertype'}]->(person_phonenumbertype)
CREATE (sales_vindividualcustomer)-[:MAKE_USE_OF {info:'person_stateprovince'}]->(person_stateprovince)
CREATE (sales_vindividualcustomer)-[:MAKE_USE_OF {info:'sales_customer'}]->(sales_customer)
CREATE (sales_vpersondemographics)-[:MAKE_USE_OF {info:'person_person'}]->(person_person)
CREATE (humanresources_vjobcandidate)-[:MAKE_USE_OF {info:'humanresources_jobcandidate'}]->(humanresources_jobcandidate)
CREATE (humanresources_vjobcandidateemployment)-[:MAKE_USE_OF {info:'humanresources_jobcandidate'}]->(humanresources_jobcandidate)
CREATE (humanresources_vjobcandidateeducation)-[:MAKE_USE_OF {info:'humanresources_jobcandidate'}]->(humanresources_jobcandidate)
CREATE (production_vproductanddescription)-[:MAKE_USE_OF {info:'production_product'}]->(production_product)
CREATE (production_vproductanddescription)-[:MAKE_USE_OF {info:'production_productdescription'}]->(production_productdescription)
CREATE (production_vproductanddescription)-[:MAKE_USE_OF {info:'production_productmodel'}]->(production_productmodel)
CREATE (production_vproductanddescription)-[:MAKE_USE_OF {info:'production_productmodelproductdescriptionculture'}]->(production_productmodelproductdescriptionculture)
CREATE (production_vproductmodelcatalogdescription)-[:MAKE_USE_OF {info:'production_productmodel'}]->(production_productmodel)
CREATE (production_vproductmodelinstructions)-[:MAKE_USE_OF {info:'production_productmodel'}]->(production_productmodel)
CREATE (sales_vsalesperson)-[:MAKE_USE_OF {info:'humanresources_employee'}]->(humanresources_employee)
CREATE (sales_vsalesperson)-[:MAKE_USE_OF {info:'person_address'}]->(person_address)
CREATE (sales_vsalesperson)-[:MAKE_USE_OF {info:'person_businessentityaddress'}]->(person_businessentityaddress)
CREATE (sales_vsalesperson)-[:MAKE_USE_OF {info:'person_countryregion'}]->(person_countryregion)
CREATE (sales_vsalesperson)-[:MAKE_USE_OF {info:'person_emailaddress'}]->(person_emailaddress)
CREATE (sales_vsalesperson)-[:MAKE_USE_OF {info:'person_person'}]->(person_person)
CREATE (sales_vsalesperson)-[:MAKE_USE_OF {info:'person_personphone'}]->(person_personphone)
CREATE (sales_vsalesperson)-[:MAKE_USE_OF {info:'person_phonenumbertype'}]->(person_phonenumbertype)
CREATE (sales_vsalesperson)-[:MAKE_USE_OF {info:'person_stateprovince'}]->(person_stateprovince)
CREATE (sales_vsalesperson)-[:MAKE_USE_OF {info:'sales_salesperson'}]->(sales_salesperson)
CREATE (sales_vsalesperson)-[:MAKE_USE_OF {info:'sales_salesterritory'}]->(sales_salesterritory)
CREATE (sales_vsalespersonsalesbyfiscalyears)-[:MAKE_USE_OF {info:'humanresources_employee'}]->(humanresources_employee)
CREATE (sales_vsalespersonsalesbyfiscalyears)-[:MAKE_USE_OF {info:'person_person'}]->(person_person)
CREATE (sales_vsalespersonsalesbyfiscalyears)-[:MAKE_USE_OF {info:'sales_salesorderheader'}]->(sales_salesorderheader)
CREATE (sales_vsalespersonsalesbyfiscalyears)-[:MAKE_USE_OF {info:'sales_salesperson'}]->(sales_salesperson)
CREATE (sales_vsalespersonsalesbyfiscalyears)-[:MAKE_USE_OF {info:'sales_salesterritory'}]->(sales_salesterritory)
CREATE (person_vstateprovincecountryregion)-[:MAKE_USE_OF {info:'person_countryregion'}]->(person_countryregion)
CREATE (person_vstateprovincecountryregion)-[:MAKE_USE_OF {info:'person_stateprovince'}]->(person_stateprovince)
CREATE (sales_vstorewithdemographics)-[:MAKE_USE_OF {info:'sales_store'}]->(sales_store)
CREATE (sales_vstorewithcontacts)-[:MAKE_USE_OF {info:'person_businessentitycontact'}]->(person_businessentitycontact)
CREATE (sales_vstorewithcontacts)-[:MAKE_USE_OF {info:'person_contacttype'}]->(person_contacttype)
CREATE (sales_vstorewithcontacts)-[:MAKE_USE_OF {info:'person_emailaddress'}]->(person_emailaddress)
CREATE (sales_vstorewithcontacts)-[:MAKE_USE_OF {info:'person_person'}]->(person_person)
CREATE (sales_vstorewithcontacts)-[:MAKE_USE_OF {info:'person_personphone'}]->(person_personphone)
CREATE (sales_vstorewithcontacts)-[:MAKE_USE_OF {info:'person_phonenumbertype'}]->(person_phonenumbertype)
CREATE (sales_vstorewithcontacts)-[:MAKE_USE_OF {info:'sales_store'}]->(sales_store)
CREATE (sales_vstorewithaddresses)-[:MAKE_USE_OF {info:'person_address'}]->(person_address)
CREATE (sales_vstorewithaddresses)-[:MAKE_USE_OF {info:'person_addresstype'}]->(person_addresstype)
CREATE (sales_vstorewithaddresses)-[:MAKE_USE_OF {info:'person_businessentityaddress'}]->(person_businessentityaddress)
CREATE (sales_vstorewithaddresses)-[:MAKE_USE_OF {info:'person_countryregion'}]->(person_countryregion)
CREATE (sales_vstorewithaddresses)-[:MAKE_USE_OF {info:'person_stateprovince'}]->(person_stateprovince)
CREATE (sales_vstorewithaddresses)-[:MAKE_USE_OF {info:'sales_store'}]->(sales_store)
CREATE (purchasing_vvendorwithcontacts)-[:MAKE_USE_OF {info:'person_businessentitycontact'}]->(person_businessentitycontact)
CREATE (purchasing_vvendorwithcontacts)-[:MAKE_USE_OF {info:'person_contacttype'}]->(person_contacttype)
CREATE (purchasing_vvendorwithcontacts)-[:MAKE_USE_OF {info:'person_emailaddress'}]->(person_emailaddress)
CREATE (purchasing_vvendorwithcontacts)-[:MAKE_USE_OF {info:'person_person'}]->(person_person)
CREATE (purchasing_vvendorwithcontacts)-[:MAKE_USE_OF {info:'person_personphone'}]->(person_personphone)
CREATE (purchasing_vvendorwithcontacts)-[:MAKE_USE_OF {info:'person_phonenumbertype'}]->(person_phonenumbertype)
CREATE (purchasing_vvendorwithcontacts)-[:MAKE_USE_OF {info:'purchasing_vendor'}]->(purchasing_vendor)
CREATE (purchasing_vvendorwithaddresses)-[:MAKE_USE_OF {info:'person_address'}]->(person_address)
CREATE (purchasing_vvendorwithaddresses)-[:MAKE_USE_OF {info:'person_addresstype'}]->(person_addresstype)
CREATE (purchasing_vvendorwithaddresses)-[:MAKE_USE_OF {info:'person_businessentityaddress'}]->(person_businessentityaddress)
CREATE (purchasing_vvendorwithaddresses)-[:MAKE_USE_OF {info:'person_countryregion'}]->(person_countryregion)
CREATE (purchasing_vvendorwithaddresses)-[:MAKE_USE_OF {info:'person_stateprovince'}]->(person_stateprovince)
CREATE (purchasing_vvendorwithaddresses)-[:MAKE_USE_OF {info:'purchasing_vendor'}]->(purchasing_vendor)

// FKEYS 

CREATE (person_person)-[:FK {fk_columns:'businessentityid'}]->(humanresources_employee)
CREATE (humanresources_department)-[:FK {fk_columns:'departmentid'}]->(humanresources_employeedepartmenthistory)
CREATE (humanresources_employee)-[:FK {fk_columns:'businessentityid'}]->(humanresources_employeedepartmenthistory)
CREATE (humanresources_shift)-[:FK {fk_columns:'shiftid'}]->(humanresources_employeedepartmenthistory)
CREATE (humanresources_employee)-[:FK {fk_columns:'businessentityid'}]->(humanresources_employeepayhistory)
CREATE (humanresources_employee)-[:FK {fk_columns:'businessentityid'}]->(humanresources_jobcandidate)
CREATE (person_stateprovince)-[:FK {fk_columns:'stateprovinceid'}]->(person_address)
CREATE (person_address)-[:FK {fk_columns:'addressid'}]->(person_businessentityaddress)
CREATE (person_addresstype)-[:FK {fk_columns:'addresstypeid'}]->(person_businessentityaddress)
CREATE (person_businessentity)-[:FK {fk_columns:'businessentityid'}]->(person_businessentityaddress)
CREATE (person_businessentity)-[:FK {fk_columns:'businessentityid'}]->(person_businessentitycontact)
CREATE (person_contacttype)-[:FK {fk_columns:'contacttypeid'}]->(person_businessentitycontact)
CREATE (person_person)-[:FK {fk_columns:'personid'}]->(person_businessentitycontact)
CREATE (person_person)-[:FK {fk_columns:'businessentityid'}]->(person_emailaddress)
CREATE (person_person)-[:FK {fk_columns:'businessentityid'}]->(person_password)
CREATE (person_businessentity)-[:FK {fk_columns:'businessentityid'}]->(person_person)
CREATE (person_person)-[:FK {fk_columns:'businessentityid'}]->(person_personphone)
CREATE (person_phonenumbertype)-[:FK {fk_columns:'phonenumbertypeid'}]->(person_personphone)
CREATE (person_countryregion)-[:FK {fk_columns:'countryregioncode'}]->(person_stateprovince)
CREATE (sales_salesterritory)-[:FK {fk_columns:'territoryid'}]->(person_stateprovince)
CREATE (production_product)-[:FK {fk_columns:'productassemblyid'}]->(production_billofmaterials)
CREATE (production_product)-[:FK {fk_columns:'componentid'}]->(production_billofmaterials)
CREATE (production_unitmeasure)-[:FK {fk_columns:'unitmeasurecode'}]->(production_billofmaterials)
CREATE (humanresources_employee)-[:FK {fk_columns:'owner'}]->(production_document)
CREATE (production_productmodel)-[:FK {fk_columns:'productmodelid'}]->(production_product)
CREATE (production_productsubcategory)-[:FK {fk_columns:'productsubcategoryid'}]->(production_product)
CREATE (production_unitmeasure)-[:FK {fk_columns:'sizeunitmeasurecode'}]->(production_product)
CREATE (production_unitmeasure)-[:FK {fk_columns:'weightunitmeasurecode'}]->(production_product)
CREATE (production_product)-[:FK {fk_columns:'productid'}]->(production_productcosthistory)
CREATE (production_document)-[:FK {fk_columns:'documentnode'}]->(production_productdocument)
CREATE (production_product)-[:FK {fk_columns:'productid'}]->(production_productdocument)
CREATE (production_location)-[:FK {fk_columns:'locationid'}]->(production_productinventory)
CREATE (production_product)-[:FK {fk_columns:'productid'}]->(production_productinventory)
CREATE (production_product)-[:FK {fk_columns:'productid'}]->(production_productlistpricehistory)
CREATE (production_illustration)-[:FK {fk_columns:'illustrationid'}]->(production_productmodelillustration)
CREATE (production_productmodel)-[:FK {fk_columns:'productmodelid'}]->(production_productmodelillustration)
CREATE (production_culture)-[:FK {fk_columns:'cultureid'}]->(production_productmodelproductdescriptionculture)
CREATE (production_productdescription)-[:FK {fk_columns:'productdescriptionid'}]->(production_productmodelproductdescriptionculture)
CREATE (production_productmodel)-[:FK {fk_columns:'productmodelid'}]->(production_productmodelproductdescriptionculture)
CREATE (production_product)-[:FK {fk_columns:'productid'}]->(production_productproductphoto)
CREATE (production_productphoto)-[:FK {fk_columns:'productphotoid'}]->(production_productproductphoto)
CREATE (production_product)-[:FK {fk_columns:'productid'}]->(production_productreview)
CREATE (production_productcategory)-[:FK {fk_columns:'productcategoryid'}]->(production_productsubcategory)
CREATE (production_product)-[:FK {fk_columns:'productid'}]->(production_transactionhistory)
CREATE (production_product)-[:FK {fk_columns:'productid'}]->(production_workorder)
CREATE (production_scrapreason)-[:FK {fk_columns:'scrapreasonid'}]->(production_workorder)
CREATE (production_location)-[:FK {fk_columns:'locationid'}]->(production_workorderrouting)
CREATE (production_workorder)-[:FK {fk_columns:'workorderid'}]->(production_workorderrouting)
CREATE (production_product)-[:FK {fk_columns:'productid'}]->(purchasing_productvendor)
CREATE (production_unitmeasure)-[:FK {fk_columns:'unitmeasurecode'}]->(purchasing_productvendor)
CREATE (purchasing_vendor)-[:FK {fk_columns:'businessentityid'}]->(purchasing_productvendor)
CREATE (production_product)-[:FK {fk_columns:'productid'}]->(purchasing_purchaseorderdetail)
CREATE (purchasing_purchaseorderheader)-[:FK {fk_columns:'purchaseorderid'}]->(purchasing_purchaseorderdetail)
CREATE (humanresources_employee)-[:FK {fk_columns:'employeeid'}]->(purchasing_purchaseorderheader)
CREATE (purchasing_shipmethod)-[:FK {fk_columns:'shipmethodid'}]->(purchasing_purchaseorderheader)
CREATE (purchasing_vendor)-[:FK {fk_columns:'vendorid'}]->(purchasing_purchaseorderheader)
CREATE (person_businessentity)-[:FK {fk_columns:'businessentityid'}]->(purchasing_vendor)
CREATE (person_countryregion)-[:FK {fk_columns:'countryregioncode'}]->(sales_countryregioncurrency)
CREATE (sales_currency)-[:FK {fk_columns:'currencycode'}]->(sales_countryregioncurrency)
CREATE (sales_currency)-[:FK {fk_columns:'fromcurrencycode'}]->(sales_currencyrate)
CREATE (sales_currency)-[:FK {fk_columns:'tocurrencycode'}]->(sales_currencyrate)
CREATE (person_person)-[:FK {fk_columns:'personid'}]->(sales_customer)
CREATE (sales_salesterritory)-[:FK {fk_columns:'territoryid'}]->(sales_customer)
CREATE (sales_store)-[:FK {fk_columns:'storeid'}]->(sales_customer)
CREATE (person_person)-[:FK {fk_columns:'businessentityid'}]->(sales_personcreditcard)
CREATE (sales_creditcard)-[:FK {fk_columns:'creditcardid'}]->(sales_personcreditcard)
CREATE (sales_salesorderheader)-[:FK {fk_columns:'salesorderid'}]->(sales_salesorderdetail)
CREATE (sales_specialofferproduct)-[:FK {fk_columns:'productid, specialofferid'}]->(sales_salesorderdetail)
CREATE (person_address)-[:FK {fk_columns:'billtoaddressid'}]->(sales_salesorderheader)
CREATE (person_address)-[:FK {fk_columns:'shiptoaddressid'}]->(sales_salesorderheader)
CREATE (purchasing_shipmethod)-[:FK {fk_columns:'shipmethodid'}]->(sales_salesorderheader)
CREATE (sales_creditcard)-[:FK {fk_columns:'creditcardid'}]->(sales_salesorderheader)
CREATE (sales_currencyrate)-[:FK {fk_columns:'currencyrateid'}]->(sales_salesorderheader)
CREATE (sales_customer)-[:FK {fk_columns:'customerid'}]->(sales_salesorderheader)
CREATE (sales_salesperson)-[:FK {fk_columns:'salespersonid'}]->(sales_salesorderheader)
CREATE (sales_salesterritory)-[:FK {fk_columns:'territoryid'}]->(sales_salesorderheader)
CREATE (sales_salesorderheader)-[:FK {fk_columns:'salesorderid'}]->(sales_salesorderheadersalesreason)
CREATE (sales_salesreason)-[:FK {fk_columns:'salesreasonid'}]->(sales_salesorderheadersalesreason)
CREATE (humanresources_employee)-[:FK {fk_columns:'businessentityid'}]->(sales_salesperson)
CREATE (sales_salesterritory)-[:FK {fk_columns:'territoryid'}]->(sales_salesperson)
CREATE (sales_salesperson)-[:FK {fk_columns:'businessentityid'}]->(sales_salespersonquotahistory)
CREATE (person_stateprovince)-[:FK {fk_columns:'stateprovinceid'}]->(sales_salestaxrate)
CREATE (person_countryregion)-[:FK {fk_columns:'countryregioncode'}]->(sales_salesterritory)
CREATE (sales_salesperson)-[:FK {fk_columns:'businessentityid'}]->(sales_salesterritoryhistory)
CREATE (sales_salesterritory)-[:FK {fk_columns:'territoryid'}]->(sales_salesterritoryhistory)
CREATE (production_product)-[:FK {fk_columns:'productid'}]->(sales_shoppingcartitem)
CREATE (production_product)-[:FK {fk_columns:'productid'}]->(sales_specialofferproduct)
CREATE (sales_specialoffer)-[:FK {fk_columns:'specialofferid'}]->(sales_specialofferproduct)
CREATE (person_businessentity)-[:FK {fk_columns:'businessentityid'}]->(sales_store)
CREATE (sales_salesperson)-[:FK {fk_columns:'salespersonid'}]->(sales_store)