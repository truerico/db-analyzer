
@startuml
skinparam titleBorderRoundCorner 15
skinparam titleBorderThickness 2
skinparam titleBorderColor black
skinparam titleBackgroundColor #DDDDDD
title **:: view erd1 © ::**
!theme _none_
skinparam shadowing False
left to right direction
skinparam linetype polyline
skinparam packageStyle rectangle
hide circle


entity "<&grid-three-up>** Person.vAdditionalContactInfo**" as Person.vAdditionalContactInfo { 
  - BusinessEntityID : int
  - FirstName : Name
  - MiddleName : Name
  - LastName : Name
  - TelephoneNumber : nvarchar
  - TelephoneSpecialInstructions : nvarchar
  - Street : nvarchar
  - City : nvarchar
  - StateProvince : nvarchar
  - PostalCode : nvarchar
  - CountryRegion : nvarchar
  - HomeAddressSpecialInstructions : nvarchar
  - EMailAddress : nvarchar
  - EMailSpecialInstructions : nvarchar
  - EMailTelephoneNumber : nvarchar
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 10
      total cols : 17
  --
}


entity "<&grid-three-up>** HumanResources.vEmployee**" as HumanResources.vEmployee { 
  - BusinessEntityID : int
  - Title : nvarchar
  - FirstName : Name
  - MiddleName : Name
  - LastName : Name
  - Suffix : nvarchar
  - JobTitle : nvarchar
  - PhoneNumber : Phone
  - PhoneNumberType : Name
  - EmailAddress : nvarchar
  - EmailPromotion : int
  - AddressLine1 : nvarchar
  - AddressLine2 : nvarchar
  - City : nvarchar
  - StateProvinceName : Name
  - PostalCode : nvarchar
  - CountryRegionName : Name
  - AdditionalContactInfo : xml
  ==
  <&pie-chart>** stats**
      total rows : 290
      total cols : 18
  --
}


entity "<&grid-three-up>** HumanResources.vEmployeeDepartment**" as HumanResources.vEmployeeDepartment { 
  - BusinessEntityID : int
  - Title : nvarchar
  - FirstName : Name
  - MiddleName : Name
  - LastName : Name
  - Suffix : nvarchar
  - JobTitle : nvarchar
  - Department : Name
  - GroupName : Name
  - StartDate : date
  ==
  <&pie-chart>** stats**
      total rows : 290
      total cols : 10
  --
}


entity "<&grid-three-up>** HumanResources.vEmployeeDepartmentHistory**" as HumanResources.vEmployeeDepartmentHistory { 
  - BusinessEntityID : int
  - Title : nvarchar
  - FirstName : Name
  - MiddleName : Name
  - LastName : Name
  - Suffix : nvarchar
  - Shift : Name
  - Department : Name
  - GroupName : Name
  - StartDate : date
  - EndDate : date
  ==
  <&pie-chart>** stats**
      total rows : 296
      total cols : 11
  --
}


entity "<&grid-three-up>** Sales.vIndividualCustomer**" as Sales.vIndividualCustomer { 
  - BusinessEntityID : int
  - Title : nvarchar
  - FirstName : Name
  - MiddleName : Name
  - LastName : Name
  - Suffix : nvarchar
  - PhoneNumber : Phone
  - PhoneNumberType : Name
  - EmailAddress : nvarchar
  - EmailPromotion : int
  - AddressType : Name
  - AddressLine1 : nvarchar
  - AddressLine2 : nvarchar
  - City : nvarchar
  - StateProvinceName : Name
  - PostalCode : nvarchar
  - CountryRegionName : Name
  - Demographics : xml
  ==
  <&pie-chart>** stats**
      total rows : 18,508
      total cols : 18
  --
}


entity "<&grid-three-up>** Sales.vPersonDemographics**" as Sales.vPersonDemographics { 
  - BusinessEntityID : int
  - TotalPurchaseYTD : money
  - DateFirstPurchase : datetime
  - BirthDate : datetime
  - MaritalStatus : nvarchar
  - YearlyIncome : nvarchar
  - Gender : nvarchar
  - TotalChildren : int
  - NumberChildrenAtHome : int
  - Education : nvarchar
  - Occupation : nvarchar
  - HomeOwnerFlag : bit
  - NumberCarsOwned : int
  ==
  <&pie-chart>** stats**
      total rows : 19,972
      total cols : 13
  --
}


entity "<&grid-three-up>** HumanResources.vJobCandidate**" as HumanResources.vJobCandidate { 
  - JobCandidateID : int
  - BusinessEntityID : int
  - Name.Prefix : nvarchar
  - Name.First : nvarchar
  - Name.Middle : nvarchar
  - Name.Last : nvarchar
  - Name.Suffix : nvarchar
  - Skills : nvarchar
  - Addr.Type : nvarchar
  - Addr.Loc.CountryRegion : nvarchar
  - Addr.Loc.State : nvarchar
  - Addr.Loc.City : nvarchar
  - Addr.PostalCode : nvarchar
  - EMail : nvarchar
  - WebSite : nvarchar
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 13
      total cols : 16
  --
}


entity "<&grid-three-up>** HumanResources.vJobCandidateEmployment**" as HumanResources.vJobCandidateEmployment { 
  - JobCandidateID : int
  - Emp.StartDate : datetime
  - Emp.EndDate : datetime
  - Emp.OrgName : nvarchar
  - Emp.JobTitle : nvarchar
  - Emp.Responsibility : nvarchar
  - Emp.FunctionCategory : nvarchar
  - Emp.IndustryCategory : nvarchar
  - Emp.Loc.CountryRegion : nvarchar
  - Emp.Loc.State : nvarchar
  - Emp.Loc.City : nvarchar
  ==
  <&pie-chart>** stats**
      total rows : 30
      total cols : 11
  --
}


entity "<&grid-three-up>** HumanResources.vJobCandidateEducation**" as HumanResources.vJobCandidateEducation { 
  - JobCandidateID : int
  - Edu.Level : nvarchar
  - Edu.StartDate : datetime
  - Edu.EndDate : datetime
  - Edu.Degree : nvarchar
  - Edu.Major : nvarchar
  - Edu.Minor : nvarchar
  - Edu.GPA : nvarchar
  - Edu.GPAScale : nvarchar
  - Edu.School : nvarchar
  - Edu.Loc.CountryRegion : nvarchar
  - Edu.Loc.State : nvarchar
  - Edu.Loc.City : nvarchar
  ==
  <&pie-chart>** stats**
      total rows : 16
      total cols : 13
  --
}


entity "<&grid-three-up>** Production.vProductAndDescription**" as Production.vProductAndDescription { 
  - ProductID : int
  - Name : Name
  - ProductModel : Name
  - CultureID : nchar
  - Description : nvarchar
  ==
  <&pie-chart>** stats**
      total rows : 1,764
      total cols : 5
  --
}


entity "<&grid-three-up>** Production.vProductModelCatalogDescription**" as Production.vProductModelCatalogDescription { 
  - ProductModelID : int
  - Name : Name
  - Summary : nvarchar
  - Manufacturer : nvarchar
  - Copyright : nvarchar
  - ProductURL : nvarchar
  - WarrantyPeriod : nvarchar
  - WarrantyDescription : nvarchar
  - NoOfYears : nvarchar
  - MaintenanceDescription : nvarchar
  - Wheel : nvarchar
  - Saddle : nvarchar
  - Pedal : nvarchar
  - BikeFrame : nvarchar
  - Crankset : nvarchar
  - PictureAngle : nvarchar
  - PictureSize : nvarchar
  - ProductPhotoID : nvarchar
  - Material : nvarchar
  - Color : nvarchar
  - ProductLine : nvarchar
  - Style : nvarchar
  - RiderExperience : nvarchar
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 6
      total cols : 25
  --
}


entity "<&grid-three-up>** Production.vProductModelInstructions**" as Production.vProductModelInstructions { 
  - ProductModelID : int
  - Name : Name
  - Instructions : nvarchar
  - LocationID : int
  - SetupHours : decimal
  - MachineHours : decimal
  - LaborHours : decimal
  - LotSize : int
  - Step : nvarchar
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 131
      total cols : 11
  --
}


entity "<&grid-three-up>** Sales.vSalesPerson**" as Sales.vSalesPerson { 
  - BusinessEntityID : int
  - Title : nvarchar
  - FirstName : Name
  - MiddleName : Name
  - LastName : Name
  - Suffix : nvarchar
  - JobTitle : nvarchar
  - PhoneNumber : Phone
  - PhoneNumberType : Name
  - EmailAddress : nvarchar
  - EmailPromotion : int
  - AddressLine1 : nvarchar
  - AddressLine2 : nvarchar
  - City : nvarchar
  - StateProvinceName : Name
  - PostalCode : nvarchar
  - CountryRegionName : Name
  - TerritoryName : Name
  - TerritoryGroup : nvarchar
  - SalesQuota : money
  - SalesYTD : money
  - SalesLastYear : money
  ==
  <&pie-chart>** stats**
      total rows : 17
      total cols : 22
  --
}


entity "<&grid-three-up>** Sales.vSalesPersonSalesByFiscalYears**" as Sales.vSalesPersonSalesByFiscalYears { 
  - SalesPersonID : int
  - FullName : nvarchar
  - JobTitle : nvarchar
  - SalesTerritory : Name
  - 2002 : money
  - 2003 : money
  - 2004 : money
  ==
  <&pie-chart>** stats**
      total rows : 14
      total cols : 7
  --
}


entity "<&grid-three-up>** Person.vStateProvinceCountryRegion**" as Person.vStateProvinceCountryRegion { 
  - StateProvinceID : int
  - StateProvinceCode : nchar
  - IsOnlyStateProvinceFlag : Flag
  - StateProvinceName : Name
  - TerritoryID : int
  - CountryRegionCode : nvarchar
  - CountryRegionName : Name
  ==
  <&pie-chart>** stats**
      total rows : 181
      total cols : 7
  --
}


entity "<&grid-three-up>** Sales.vStoreWithDemographics**" as Sales.vStoreWithDemographics { 
  - BusinessEntityID : int
  - Name : Name
  - AnnualSales : money
  - AnnualRevenue : money
  - BankName : nvarchar
  - BusinessType : nvarchar
  - YearOpened : int
  - Specialty : nvarchar
  - SquareFeet : int
  - Brands : nvarchar
  - Internet : nvarchar
  - NumberEmployees : int
  ==
  <&pie-chart>** stats**
      total rows : 701
      total cols : 12
  --
}


entity "<&grid-three-up>** Sales.vStoreWithContacts**" as Sales.vStoreWithContacts { 
  - BusinessEntityID : int
  - Name : Name
  - ContactType : Name
  - Title : nvarchar
  - FirstName : Name
  - MiddleName : Name
  - LastName : Name
  - Suffix : nvarchar
  - PhoneNumber : Phone
  - PhoneNumberType : Name
  - EmailAddress : nvarchar
  - EmailPromotion : int
  ==
  <&pie-chart>** stats**
      total rows : 753
      total cols : 12
  --
}


entity "<&grid-three-up>** Sales.vStoreWithAddresses**" as Sales.vStoreWithAddresses { 
  - BusinessEntityID : int
  - Name : Name
  - AddressType : Name
  - AddressLine1 : nvarchar
  - AddressLine2 : nvarchar
  - City : nvarchar
  - StateProvinceName : Name
  - PostalCode : nvarchar
  - CountryRegionName : Name
  ==
  <&pie-chart>** stats**
      total rows : 712
      total cols : 9
  --
}


entity "<&grid-three-up>** Purchasing.vVendorWithContacts**" as Purchasing.vVendorWithContacts { 
  - BusinessEntityID : int
  - Name : Name
  - ContactType : Name
  - Title : nvarchar
  - FirstName : Name
  - MiddleName : Name
  - LastName : Name
  - Suffix : nvarchar
  - PhoneNumber : Phone
  - PhoneNumberType : Name
  - EmailAddress : nvarchar
  - EmailPromotion : int
  ==
  <&pie-chart>** stats**
      total rows : 156
      total cols : 12
  --
}


entity "<&grid-three-up>** Purchasing.vVendorWithAddresses**" as Purchasing.vVendorWithAddresses { 
  - BusinessEntityID : int
  - Name : Name
  - AddressType : Name
  - AddressLine1 : nvarchar
  - AddressLine2 : nvarchar
  - City : nvarchar
  - StateProvinceName : Name
  - PostalCode : nvarchar
  - CountryRegionName : Name
  ==
  <&pie-chart>** stats**
      total rows : 104
      total cols : 9
  --
}
Person.vAdditionalContactInfo ||.d.o{ Person.Person
HumanResources.vEmployee ||.l.o{ HumanResources.Employee
HumanResources.vEmployee ||.u.o{ Person.Address
HumanResources.vEmployee ||.r.o{ Person.BusinessEntityAddress
HumanResources.vEmployee ||.d.o{ Person.CountryRegion
HumanResources.vEmployee ||.l.o{ Person.EmailAddress
HumanResources.vEmployee ||.u.o{ Person.Person
HumanResources.vEmployee ||.r.o{ Person.PersonPhone
HumanResources.vEmployee ||.d.o{ Person.PhoneNumberType
HumanResources.vEmployee ||.l.o{ Person.StateProvince
HumanResources.vEmployeeDepartment ||.u.o{ HumanResources.Department
HumanResources.vEmployeeDepartment ||.r.o{ HumanResources.Employee
HumanResources.vEmployeeDepartment ||.d.o{ HumanResources.EmployeeDepartmentHistory
HumanResources.vEmployeeDepartment ||.l.o{ Person.Person
HumanResources.vEmployeeDepartmentHistory ||.u.o{ HumanResources.Department
HumanResources.vEmployeeDepartmentHistory ||.r.o{ HumanResources.Employee
HumanResources.vEmployeeDepartmentHistory ||.d.o{ HumanResources.EmployeeDepartmentHistory
HumanResources.vEmployeeDepartmentHistory ||.l.o{ HumanResources.Shift
HumanResources.vEmployeeDepartmentHistory ||.u.o{ Person.Person
Sales.vIndividualCustomer ||.r.o{ Person.Address
Sales.vIndividualCustomer ||.d.o{ Person.AddressType
Sales.vIndividualCustomer ||.l.o{ Person.BusinessEntityAddress
Sales.vIndividualCustomer ||.u.o{ Person.CountryRegion
Sales.vIndividualCustomer ||.r.o{ Person.EmailAddress
Sales.vIndividualCustomer ||.d.o{ Person.Person
Sales.vIndividualCustomer ||.l.o{ Person.PersonPhone
Sales.vIndividualCustomer ||.u.o{ Person.PhoneNumberType
Sales.vIndividualCustomer ||.r.o{ Person.StateProvince
Sales.vIndividualCustomer ||.d.o{ Sales.Customer
Sales.vPersonDemographics ||.l.o{ Person.Person
HumanResources.vJobCandidate ||.u.o{ HumanResources.JobCandidate
HumanResources.vJobCandidateEmployment ||.r.o{ HumanResources.JobCandidate
HumanResources.vJobCandidateEducation ||.d.o{ HumanResources.JobCandidate
Production.vProductAndDescription ||.l.o{ Production.Product
Production.vProductAndDescription ||.u.o{ Production.ProductDescription
Production.vProductAndDescription ||.r.o{ Production.ProductModel
Production.vProductAndDescription ||.d.o{ Production.ProductModelProductDescriptionCulture
Production.vProductModelCatalogDescription ||.l.o{ Production.ProductModel
Production.vProductModelInstructions ||.u.o{ Production.ProductModel
Sales.vSalesPerson ||.r.o{ HumanResources.Employee
Sales.vSalesPerson ||.d.o{ Person.Address
Sales.vSalesPerson ||.l.o{ Person.BusinessEntityAddress
Sales.vSalesPerson ||.u.o{ Person.CountryRegion
Sales.vSalesPerson ||.r.o{ Person.EmailAddress
Sales.vSalesPerson ||.d.o{ Person.Person
Sales.vSalesPerson ||.l.o{ Person.PersonPhone
Sales.vSalesPerson ||.u.o{ Person.PhoneNumberType
Sales.vSalesPerson ||.r.o{ Person.StateProvince
Sales.vSalesPerson ||.d.o{ Sales.SalesPerson
Sales.vSalesPerson ||.l.o{ Sales.SalesTerritory
Sales.vSalesPersonSalesByFiscalYears ||.u.o{ HumanResources.Employee
Sales.vSalesPersonSalesByFiscalYears ||.r.o{ Person.Person
Sales.vSalesPersonSalesByFiscalYears ||.d.o{ Sales.SalesOrderHeader
Sales.vSalesPersonSalesByFiscalYears ||.l.o{ Sales.SalesPerson
Sales.vSalesPersonSalesByFiscalYears ||.u.o{ Sales.SalesTerritory
Person.vStateProvinceCountryRegion ||.r.o{ Person.CountryRegion
Person.vStateProvinceCountryRegion ||.d.o{ Person.StateProvince
Sales.vStoreWithDemographics ||.l.o{ Sales.Store
Sales.vStoreWithContacts ||.u.o{ Person.BusinessEntityContact
Sales.vStoreWithContacts ||.r.o{ Person.ContactType
Sales.vStoreWithContacts ||.d.o{ Person.EmailAddress
Sales.vStoreWithContacts ||.l.o{ Person.Person
Sales.vStoreWithContacts ||.u.o{ Person.PersonPhone
Sales.vStoreWithContacts ||.r.o{ Person.PhoneNumberType
Sales.vStoreWithContacts ||.d.o{ Sales.Store
Sales.vStoreWithAddresses ||.l.o{ Person.Address
Sales.vStoreWithAddresses ||.u.o{ Person.AddressType
Sales.vStoreWithAddresses ||.r.o{ Person.BusinessEntityAddress
Sales.vStoreWithAddresses ||.d.o{ Person.CountryRegion
Sales.vStoreWithAddresses ||.l.o{ Person.StateProvince
Sales.vStoreWithAddresses ||.u.o{ Sales.Store
Purchasing.vVendorWithContacts ||.r.o{ Person.BusinessEntityContact
Purchasing.vVendorWithContacts ||.d.o{ Person.ContactType
Purchasing.vVendorWithContacts ||.l.o{ Person.EmailAddress
Purchasing.vVendorWithContacts ||.u.o{ Person.Person
Purchasing.vVendorWithContacts ||.r.o{ Person.PersonPhone
Purchasing.vVendorWithContacts ||.d.o{ Person.PhoneNumberType
Purchasing.vVendorWithContacts ||.l.o{ Purchasing.Vendor
Purchasing.vVendorWithAddresses ||.u.o{ Person.Address
Purchasing.vVendorWithAddresses ||.r.o{ Person.AddressType
Purchasing.vVendorWithAddresses ||.d.o{ Person.BusinessEntityAddress
Purchasing.vVendorWithAddresses ||.l.o{ Person.CountryRegion
Purchasing.vVendorWithAddresses ||.u.o{ Person.StateProvince
Purchasing.vVendorWithAddresses ||.r.o{ Purchasing.Vendor


'# manual relation section 
vw_aaa .. vw_bbb

@enduml