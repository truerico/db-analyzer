
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

(sales.\nsalestaxrate) as (sales_salestaxrate) << Table >>
(sales.\npersoncreditcard) as (sales_personcreditcard) << Table >>
(person.\npersonphone) as (person_personphone) << Table >>
(sales.\nsalesterritory) as (sales_salesterritory) << Table >>
(person.\nphonenumbertype) as (person_phonenumbertype) << Table >>
(production.\nproduct) as (production_product) << Table >>
(sales.\nsalesterritoryhistory) as (sales_salesterritoryhistory) << Table >>
(production.\nscrapreason) as (production_scrapreason) << Table >>
(humanresources.\nshift) as (humanresources_shift) << Table >>
(production.\nproductcategory) as (production_productcategory) << Table >>
(purchasing.\nshipmethod) as (purchasing_shipmethod) << Table >>
(production.\nproductcosthistory) as (production_productcosthistory) << Table >>
(production.\nproductdescription) as (production_productdescription) << Table >>
(sales.\nshoppingcartitem) as (sales_shoppingcartitem) << Table >>
(production.\nproductdocument) as (production_productdocument) << Table >>
(production.\nproductinventory) as (production_productinventory) << Table >>
(sales.\nspecialoffer) as (sales_specialoffer) << Table >>
(production.\nproductlistpricehistory) as (production_productlistpricehistory) << Table >>
(person.\naddress) as (person_address) << Table >>
(sales.\nspecialofferproduct) as (sales_specialofferproduct) << Table >>
(production.\nproductmodel) as (production_productmodel) << Table >>
(person.\naddresstype) as (person_addresstype) << Table >>
(person.\nstateprovince) as (person_stateprovince) << Table >>
(production.\nproductmodelillustration) as (production_productmodelillustration) << Table >>
(production.\nproductmodelproductdescriptionculture) as (production_productmodelproductdescriptionculture) << Table >>
(production.\nbillofmaterials) as (production_billofmaterials) << Table >>
(sales.\nstore) as (sales_store) << Table >>
(production.\nproductphoto) as (production_productphoto) << Table >>
(production.\nproductproductphoto) as (production_productproductphoto) << Table >>
(production.\ntransactionhistory) as (production_transactionhistory) << Table >>
(production.\nproductreview) as (production_productreview) << Table >>
(person.\nbusinessentity) as (person_businessentity) << Table >>
(production.\nproductsubcategory) as (production_productsubcategory) << Table >>
(person.\nbusinessentityaddress) as (person_businessentityaddress) << Table >>
(purchasing.\nproductvendor) as (purchasing_productvendor) << Table >>
(person.\nbusinessentitycontact) as (person_businessentitycontact) << Table >>
(production.\nunitmeasure) as (production_unitmeasure) << Table >>
(purchasing.\nvendor) as (purchasing_vendor) << Table >>
(person.\ncontacttype) as (person_contacttype) << Table >>
(sales.\ncountryregioncurrency) as (sales_countryregioncurrency) << Table >>
(person.\ncountryregion) as (person_countryregion) << Table >>
(production.\nworkorder) as (production_workorder) << Table >>
(purchasing.\npurchaseorderdetail) as (purchasing_purchaseorderdetail) << Table >>
(sales.\ncreditcard) as (sales_creditcard) << Table >>
(production.\nculture) as (production_culture) << Table >>
(production.\nworkorderrouting) as (production_workorderrouting) << Table >>
(sales.\ncurrency) as (sales_currency) << Table >>
(purchasing.\npurchaseorderheader) as (purchasing_purchaseorderheader) << Table >>
(sales.\ncurrencyrate) as (sales_currencyrate) << Table >>
(sales.\ncustomer) as (sales_customer) << Table >>
(humanresources.\ndepartment) as (humanresources_department) << Table >>
(production.\ndocument) as (production_document) << Table >>
(sales.\nsalesorderdetail) as (sales_salesorderdetail) << Table >>
(person.\nemailaddress) as (person_emailaddress) << Table >>
(humanresources.\nemployee) as (humanresources_employee) << Table >>
(sales.\nsalesorderheader) as (sales_salesorderheader) << Table >>
(humanresources.\nemployeedepartmenthistory) as (humanresources_employeedepartmenthistory) << Table >>
(humanresources.\nemployeepayhistory) as (humanresources_employeepayhistory) << Table >>
(sales.\nsalesorderheadersalesreason) as (sales_salesorderheadersalesreason) << Table >>
(sales.\nsalesperson) as (sales_salesperson) << Table >>
(production.\nillustration) as (production_illustration) << Table >>
(humanresources.\njobcandidate) as (humanresources_jobcandidate) << Table >>
(production.\nlocation) as (production_location) << Table >>
(person.\npassword) as (person_password) << Table >>
(sales.\nsalespersonquotahistory) as (sales_salespersonquotahistory) << Table >>
(person.\nperson) as (person_person) << Table >>
(sales.\nsalesreason) as (sales_salesreason) << Table >>

' VIEWS 

(person.\nvadditionalcontactinfo) as (person_vadditionalcontactinfo) << View >>
(humanresources.\nvemployee) as (humanresources_vemployee) << View >>
(humanresources.\nvemployeedepartment) as (humanresources_vemployeedepartment) << View >>
(humanresources.\nvemployeedepartmenthistory) as (humanresources_vemployeedepartmenthistory) << View >>
(sales.\nvindividualcustomer) as (sales_vindividualcustomer) << View >>
(sales.\nvpersondemographics) as (sales_vpersondemographics) << View >>
(humanresources.\nvjobcandidate) as (humanresources_vjobcandidate) << View >>
(humanresources.\nvjobcandidateemployment) as (humanresources_vjobcandidateemployment) << View >>
(humanresources.\nvjobcandidateeducation) as (humanresources_vjobcandidateeducation) << View >>
(production.\nvproductanddescription) as (production_vproductanddescription) << View >>
(production.\nvproductmodelcatalogdescription) as (production_vproductmodelcatalogdescription) << View >>
(production.\nvproductmodelinstructions) as (production_vproductmodelinstructions) << View >>
(sales.\nvsalesperson) as (sales_vsalesperson) << View >>
(sales.\nvsalespersonsalesbyfiscalyears) as (sales_vsalespersonsalesbyfiscalyears) << View >>
(person.\nvstateprovincecountryregion) as (person_vstateprovincecountryregion) << View >>
(sales.\nvstorewithdemographics) as (sales_vstorewithdemographics) << View >>
(sales.\nvstorewithcontacts) as (sales_vstorewithcontacts) << View >>
(sales.\nvstorewithaddresses) as (sales_vstorewithaddresses) << View >>
(purchasing.\nvvendorwithcontacts) as (purchasing_vvendorwithcontacts) << View >>
(purchasing.\nvvendorwithaddresses) as (purchasing_vvendorwithaddresses) << View >>

' VIEWS RELATED OBJECTS 

(person_vadditionalcontactinfo)-d->(person_person)
(humanresources_vemployee)-l->(humanresources_employee)
(humanresources_vemployee)-u->(person_address)
(humanresources_vemployee)-r->(person_businessentityaddress)
(humanresources_vemployee)-d->(person_countryregion)
(humanresources_vemployee)-l->(person_emailaddress)
(humanresources_vemployee)-u->(person_person)
(humanresources_vemployee)-r->(person_personphone)
(humanresources_vemployee)-d->(person_phonenumbertype)
(humanresources_vemployee)-l->(person_stateprovince)
(humanresources_vemployeedepartment)-u->(humanresources_department)
(humanresources_vemployeedepartment)-r->(humanresources_employee)
(humanresources_vemployeedepartment)-d->(humanresources_employeedepartmenthistory)
(humanresources_vemployeedepartment)-l->(person_person)
(humanresources_vemployeedepartmenthistory)-u->(humanresources_department)
(humanresources_vemployeedepartmenthistory)-r->(humanresources_employee)
(humanresources_vemployeedepartmenthistory)-d->(humanresources_employeedepartmenthistory)
(humanresources_vemployeedepartmenthistory)-l->(humanresources_shift)
(humanresources_vemployeedepartmenthistory)-u->(person_person)
(sales_vindividualcustomer)-r->(person_address)
(sales_vindividualcustomer)-d->(person_addresstype)
(sales_vindividualcustomer)-l->(person_businessentityaddress)
(sales_vindividualcustomer)-u->(person_countryregion)
(sales_vindividualcustomer)-r->(person_emailaddress)
(sales_vindividualcustomer)-d->(person_person)
(sales_vindividualcustomer)-l->(person_personphone)
(sales_vindividualcustomer)-u->(person_phonenumbertype)
(sales_vindividualcustomer)-r->(person_stateprovince)
(sales_vindividualcustomer)-d->(sales_customer)
(sales_vpersondemographics)-l->(person_person)
(humanresources_vjobcandidate)-u->(humanresources_jobcandidate)
(humanresources_vjobcandidateemployment)-r->(humanresources_jobcandidate)
(humanresources_vjobcandidateeducation)-d->(humanresources_jobcandidate)
(production_vproductanddescription)-l->(production_product)
(production_vproductanddescription)-u->(production_productdescription)
(production_vproductanddescription)-r->(production_productmodel)
(production_vproductanddescription)-d->(production_productmodelproductdescriptionculture)
(production_vproductmodelcatalogdescription)-l->(production_productmodel)
(production_vproductmodelinstructions)-u->(production_productmodel)
(sales_vsalesperson)-r->(humanresources_employee)
(sales_vsalesperson)-d->(person_address)
(sales_vsalesperson)-l->(person_businessentityaddress)
(sales_vsalesperson)-u->(person_countryregion)
(sales_vsalesperson)-r->(person_emailaddress)
(sales_vsalesperson)-d->(person_person)
(sales_vsalesperson)-l->(person_personphone)
(sales_vsalesperson)-u->(person_phonenumbertype)
(sales_vsalesperson)-r->(person_stateprovince)
(sales_vsalesperson)-d->(sales_salesperson)
(sales_vsalesperson)-l->(sales_salesterritory)
(sales_vsalespersonsalesbyfiscalyears)-u->(humanresources_employee)
(sales_vsalespersonsalesbyfiscalyears)-r->(person_person)
(sales_vsalespersonsalesbyfiscalyears)-d->(sales_salesorderheader)
(sales_vsalespersonsalesbyfiscalyears)-l->(sales_salesperson)
(sales_vsalespersonsalesbyfiscalyears)-u->(sales_salesterritory)
(person_vstateprovincecountryregion)-r->(person_countryregion)
(person_vstateprovincecountryregion)-d->(person_stateprovince)
(sales_vstorewithdemographics)-l->(sales_store)
(sales_vstorewithcontacts)-u->(person_businessentitycontact)
(sales_vstorewithcontacts)-r->(person_contacttype)
(sales_vstorewithcontacts)-d->(person_emailaddress)
(sales_vstorewithcontacts)-l->(person_person)
(sales_vstorewithcontacts)-u->(person_personphone)
(sales_vstorewithcontacts)-r->(person_phonenumbertype)
(sales_vstorewithcontacts)-d->(sales_store)
(sales_vstorewithaddresses)-l->(person_address)
(sales_vstorewithaddresses)-u->(person_addresstype)
(sales_vstorewithaddresses)-r->(person_businessentityaddress)
(sales_vstorewithaddresses)-d->(person_countryregion)
(sales_vstorewithaddresses)-l->(person_stateprovince)
(sales_vstorewithaddresses)-u->(sales_store)
(purchasing_vvendorwithcontacts)-r->(person_businessentitycontact)
(purchasing_vvendorwithcontacts)-d->(person_contacttype)
(purchasing_vvendorwithcontacts)-l->(person_emailaddress)
(purchasing_vvendorwithcontacts)-u->(person_person)
(purchasing_vvendorwithcontacts)-r->(person_personphone)
(purchasing_vvendorwithcontacts)-d->(person_phonenumbertype)
(purchasing_vvendorwithcontacts)-l->(purchasing_vendor)
(purchasing_vvendorwithaddresses)-u->(person_address)
(purchasing_vvendorwithaddresses)-r->(person_addresstype)
(purchasing_vvendorwithaddresses)-d->(person_businessentityaddress)
(purchasing_vvendorwithaddresses)-l->(person_countryregion)
(purchasing_vvendorwithaddresses)-u->(person_stateprovince)
(purchasing_vvendorwithaddresses)-r->(purchasing_vendor)

' FKEYS 

(person_person)-d->(humanresources_employee) : 'businessentityid' 
(humanresources_department)-l->(humanresources_employeedepartmenthistory) : 'departmentid' 
(humanresources_employee)-u->(humanresources_employeedepartmenthistory) : 'businessentityid' 
(humanresources_shift)-r->(humanresources_employeedepartmenthistory) : 'shiftid' 
(humanresources_employee)-d->(humanresources_employeepayhistory) : 'businessentityid' 
(humanresources_employee)-l->(humanresources_jobcandidate) : 'businessentityid' 
(person_stateprovince)-u->(person_address) : 'stateprovinceid' 
(person_address)-r->(person_businessentityaddress) : 'addressid' 
(person_addresstype)-d->(person_businessentityaddress) : 'addresstypeid' 
(person_businessentity)-l->(person_businessentityaddress) : 'businessentityid' 
(person_businessentity)-u->(person_businessentitycontact) : 'businessentityid' 
(person_contacttype)-r->(person_businessentitycontact) : 'contacttypeid' 
(person_person)-d->(person_businessentitycontact) : 'personid' 
(person_person)-l->(person_emailaddress) : 'businessentityid' 
(person_person)-u->(person_password) : 'businessentityid' 
(person_businessentity)-r->(person_person) : 'businessentityid' 
(person_person)-d->(person_personphone) : 'businessentityid' 
(person_phonenumbertype)-l->(person_personphone) : 'phonenumbertypeid' 
(person_countryregion)-u->(person_stateprovince) : 'countryregioncode' 
(sales_salesterritory)-r->(person_stateprovince) : 'territoryid' 
(production_product)-d->(production_billofmaterials) : 'productassemblyid' 
(production_product)-l->(production_billofmaterials) : 'componentid' 
(production_unitmeasure)-u->(production_billofmaterials) : 'unitmeasurecode' 
(humanresources_employee)-r->(production_document) : 'owner' 
(production_productmodel)-d->(production_product) : 'productmodelid' 
(production_productsubcategory)-l->(production_product) : 'productsubcategoryid' 
(production_unitmeasure)-u->(production_product) : 'sizeunitmeasurecode' 
(production_unitmeasure)-r->(production_product) : 'weightunitmeasurecode' 
(production_product)-d->(production_productcosthistory) : 'productid' 
(production_document)-l->(production_productdocument) : 'documentnode' 
(production_product)-u->(production_productdocument) : 'productid' 
(production_location)-r->(production_productinventory) : 'locationid' 
(production_product)-d->(production_productinventory) : 'productid' 
(production_product)-l->(production_productlistpricehistory) : 'productid' 
(production_illustration)-u->(production_productmodelillustration) : 'illustrationid' 
(production_productmodel)-r->(production_productmodelillustration) : 'productmodelid' 
(production_culture)-d->(production_productmodelproductdescriptionculture) : 'cultureid' 
(production_productdescription)-l->(production_productmodelproductdescriptionculture) : 'productdescriptionid' 
(production_productmodel)-u->(production_productmodelproductdescriptionculture) : 'productmodelid' 
(production_product)-r->(production_productproductphoto) : 'productid' 
(production_productphoto)-d->(production_productproductphoto) : 'productphotoid' 
(production_product)-l->(production_productreview) : 'productid' 
(production_productcategory)-u->(production_productsubcategory) : 'productcategoryid' 
(production_product)-r->(production_transactionhistory) : 'productid' 
(production_product)-d->(production_workorder) : 'productid' 
(production_scrapreason)-l->(production_workorder) : 'scrapreasonid' 
(production_location)-u->(production_workorderrouting) : 'locationid' 
(production_workorder)-r->(production_workorderrouting) : 'workorderid' 
(production_product)-d->(purchasing_productvendor) : 'productid' 
(production_unitmeasure)-l->(purchasing_productvendor) : 'unitmeasurecode' 
(purchasing_vendor)-u->(purchasing_productvendor) : 'businessentityid' 
(production_product)-r->(purchasing_purchaseorderdetail) : 'productid' 
(purchasing_purchaseorderheader)-d->(purchasing_purchaseorderdetail) : 'purchaseorderid' 
(humanresources_employee)-l->(purchasing_purchaseorderheader) : 'employeeid' 
(purchasing_shipmethod)-u->(purchasing_purchaseorderheader) : 'shipmethodid' 
(purchasing_vendor)-r->(purchasing_purchaseorderheader) : 'vendorid' 
(person_businessentity)-d->(purchasing_vendor) : 'businessentityid' 
(person_countryregion)-l->(sales_countryregioncurrency) : 'countryregioncode' 
(sales_currency)-u->(sales_countryregioncurrency) : 'currencycode' 
(sales_currency)-r->(sales_currencyrate) : 'fromcurrencycode' 
(sales_currency)-d->(sales_currencyrate) : 'tocurrencycode' 
(person_person)-l->(sales_customer) : 'personid' 
(sales_salesterritory)-u->(sales_customer) : 'territoryid' 
(sales_store)-r->(sales_customer) : 'storeid' 
(person_person)-d->(sales_personcreditcard) : 'businessentityid' 
(sales_creditcard)-l->(sales_personcreditcard) : 'creditcardid' 
(sales_salesorderheader)-u->(sales_salesorderdetail) : 'salesorderid' 
(sales_specialofferproduct)-r->(sales_salesorderdetail) : 'productid, specialofferid' 
(person_address)-d->(sales_salesorderheader) : 'billtoaddressid' 
(person_address)-l->(sales_salesorderheader) : 'shiptoaddressid' 
(purchasing_shipmethod)-u->(sales_salesorderheader) : 'shipmethodid' 
(sales_creditcard)-r->(sales_salesorderheader) : 'creditcardid' 
(sales_currencyrate)-d->(sales_salesorderheader) : 'currencyrateid' 
(sales_customer)-l->(sales_salesorderheader) : 'customerid' 
(sales_salesperson)-u->(sales_salesorderheader) : 'salespersonid' 
(sales_salesterritory)-r->(sales_salesorderheader) : 'territoryid' 
(sales_salesorderheader)-d->(sales_salesorderheadersalesreason) : 'salesorderid' 
(sales_salesreason)-l->(sales_salesorderheadersalesreason) : 'salesreasonid' 
(humanresources_employee)-u->(sales_salesperson) : 'businessentityid' 
(sales_salesterritory)-r->(sales_salesperson) : 'territoryid' 
(sales_salesperson)-d->(sales_salespersonquotahistory) : 'businessentityid' 
(person_stateprovince)-l->(sales_salestaxrate) : 'stateprovinceid' 
(person_countryregion)-u->(sales_salesterritory) : 'countryregioncode' 
(sales_salesperson)-r->(sales_salesterritoryhistory) : 'businessentityid' 
(sales_salesterritory)-d->(sales_salesterritoryhistory) : 'territoryid' 
(production_product)-l->(sales_shoppingcartitem) : 'productid' 
(production_product)-u->(sales_specialofferproduct) : 'productid' 
(sales_specialoffer)-r->(sales_specialofferproduct) : 'specialofferid' 
(person_businessentity)-d->(sales_store) : 'businessentityid' 
(sales_salesperson)-l->(sales_store) : 'salespersonid' 


@enduml