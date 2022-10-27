
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



entity "<&grid-three-up>** Sales.SalesTaxRate**" as Sales.SalesTaxRate { 
  + **(pk) SalesTaxRateID : int**
  --
  - TaxType : tinyint
  - TaxRate : smallmoney
  - Name : nvarchar
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  --
  + **(fk) StateProvinceID : int**
  ==
  <&pie-chart>** stats**
      total rows : 29
      total cols : 7
      data size : 72 KB
      index size : 32 KB
  --
}


entity "<&grid-three-up>** Sales.PersonCreditCard**" as Sales.PersonCreditCard { 
  + **(pk) BusinessEntityID : int**
  + **(pk) CreditCardID : int**
  --
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 19,118
      total cols : 3
      data size : 584 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** Person.PersonPhone**" as Person.PersonPhone { 
  + **(pk) BusinessEntityID : int**
  + **(pk) PhoneNumber : nvarchar**
  + **(pk) PhoneNumberTypeID : int**
  --
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 19,972
      total cols : 4
      data size : 1,288 KB
      index size : 976 KB
  --
}


entity "<&grid-three-up>** Sales.SalesTerritory**" as Sales.SalesTerritory { 
  + **(pk) TerritoryID : int**
  --
  - Name : nvarchar
  - Group : nvarchar
  - SalesYTD : money
  - SalesLastYear : money
  - CostYTD : money
  - CostLastYear : money
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  --
  + **(fk) CountryRegionCode : nvarchar**
  ==
  <&pie-chart>** stats**
      total rows : 10
      total cols : 10
      data size : 72 KB
      index size : 32 KB
  --
}


entity "<&grid-three-up>** Person.PhoneNumberType**" as Person.PhoneNumberType { 
  + **(pk) PhoneNumberTypeID : int**
  --
  - Name : nvarchar
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 3
      total cols : 3
      data size : 72 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** Production.Product**" as Production.Product { 
  + **(pk) ProductID : int**
  --
  - Name : nvarchar
  - ProductNumber : nvarchar
  - MakeFlag : bit
  - FinishedGoodsFlag : bit
  - Color : nvarchar
  - SafetyStockLevel : smallint
  - ReorderPoint : smallint
  - StandardCost : money
  - ListPrice : money
  - Size : nvarchar
  - Weight : decimal
  - DaysToManufacture : int
  - ProductLine : nchar
  - Class : nchar
  - Style : nchar
  - SellStartDate : datetime
  - SellEndDate : datetime
  - DiscontinuedDate : datetime
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  --
  + **(fk) ProductSubcategoryID : int**
  + **(fk) ProductModelID : int**
  + **(fk) SizeUnitMeasureCode : nchar**
  + **(fk) WeightUnitMeasureCode : nchar**
  ==
  <&pie-chart>** stats**
      total rows : 504
      total cols : 25
      data size : 264 KB
      index size : 112 KB
  --
}


entity "<&grid-three-up>** Sales.SalesTerritoryHistory**" as Sales.SalesTerritoryHistory { 
  + **(pk) BusinessEntityID : int**
  + **(pk) TerritoryID : int**
  + **(pk) StartDate : datetime**
  --
  - EndDate : datetime
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 17
      total cols : 6
      data size : 72 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** Production.ScrapReason**" as Production.ScrapReason { 
  + **(pk) ScrapReasonID : smallint**
  --
  - Name : nvarchar
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 16
      total cols : 3
      data size : 72 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** HumanResources.Shift**" as HumanResources.Shift { 
  + **(pk) ShiftID : tinyint**
  --
  - Name : nvarchar
  - StartTime : time
  - EndTime : time
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 3
      total cols : 5
      data size : 72 KB
      index size : 32 KB
  --
}


entity "<&grid-three-up>** Production.ProductCategory**" as Production.ProductCategory { 
  + **(pk) ProductCategoryID : int**
  --
  - Name : nvarchar
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 4
      total cols : 4
      data size : 72 KB
      index size : 32 KB
  --
}


entity "<&grid-three-up>** Purchasing.ShipMethod**" as Purchasing.ShipMethod { 
  + **(pk) ShipMethodID : int**
  --
  - Name : nvarchar
  - ShipBase : money
  - ShipRate : money
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 5
      total cols : 6
      data size : 72 KB
      index size : 32 KB
  --
}


entity "<&grid-three-up>** Production.ProductCostHistory**" as Production.ProductCostHistory { 
  + **(pk) ProductID : int**
  + **(pk) StartDate : datetime**
  --
  - EndDate : datetime
  - StandardCost : money
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 395
      total cols : 5
      data size : 200 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** Production.ProductDescription**" as Production.ProductDescription { 
  + **(pk) ProductDescriptionID : int**
  --
  - Description : nvarchar
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 762
      total cols : 4
      data size : 264 KB
      index size : 40 KB
  --
}


entity "<&grid-three-up>** Sales.ShoppingCartItem**" as Sales.ShoppingCartItem { 
  + **(pk) ShoppingCartItemID : int**
  --
  - ShoppingCartID : nvarchar
  - Quantity : int
  - DateCreated : datetime
  - ModifiedDate : datetime
  --
  + **(fk) ProductID : int**
  ==
  <&pie-chart>** stats**
      total rows : 3
      total cols : 6
      data size : 72 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** Production.ProductDocument**" as Production.ProductDocument { 
  + **(pk) ProductID : int**
  + **(pk) DocumentNode : hierarchyid**
  --
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 32
      total cols : 3
      data size : 72 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** Production.ProductInventory**" as Production.ProductInventory { 
  + **(pk) ProductID : int**
  + **(pk) LocationID : smallint**
  --
  - Shelf : nvarchar
  - Bin : tinyint
  - Quantity : smallint
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 1,069
      total cols : 7
      data size : 200 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** Sales.SpecialOffer**" as Sales.SpecialOffer { 
  + **(pk) SpecialOfferID : int**
  --
  - Description : nvarchar
  - DiscountPct : smallmoney
  - Type : nvarchar
  - Category : nvarchar
  - StartDate : datetime
  - EndDate : datetime
  - MinQty : int
  - MaxQty : int
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 16
      total cols : 11
      data size : 72 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** Production.ProductListPriceHistory**" as Production.ProductListPriceHistory { 
  + **(pk) ProductID : int**
  + **(pk) StartDate : datetime**
  --
  - EndDate : datetime
  - ListPrice : money
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 395
      total cols : 5
      data size : 200 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** Person.Address**" as Person.Address { 
  + **(pk) AddressID : int**
  --
  - AddressLine1 : nvarchar
  - AddressLine2 : nvarchar
  - City : nvarchar
  - PostalCode : nvarchar
  - SpatialLocation : geography
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  --
  + **(fk) StateProvinceID : int**
  ==
  <&pie-chart>** stats**
      total rows : 19,614
      total cols : 9
      data size : 2,824 KB
      index size : 2,544 KB
  --
}


entity "<&grid-three-up>** Sales.SpecialOfferProduct**" as Sales.SpecialOfferProduct { 
  + **(pk) SpecialOfferID : int**
  + **(pk) ProductID : int**
  --
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 538
      total cols : 4
      data size : 200 KB
      index size : 48 KB
  --
}


entity "<&grid-three-up>** Production.ProductModel**" as Production.ProductModel { 
  + **(pk) ProductModelID : int**
  --
  - Name : nvarchar
  - CatalogDescription : xml
  - Instructions : xml
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 128
      total cols : 6
      data size : 336 KB
      index size : 32 KB
  --
}


entity "<&grid-three-up>** Person.AddressType**" as Person.AddressType { 
  + **(pk) AddressTypeID : int**
  --
  - Name : nvarchar
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 6
      total cols : 4
      data size : 72 KB
      index size : 32 KB
  --
}


entity "<&grid-three-up>** Person.StateProvince**" as Person.StateProvince { 
  + **(pk) StateProvinceID : int**
  --
  - StateProvinceCode : nchar
  - IsOnlyStateProvinceFlag : bit
  - Name : nvarchar
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  --
  + **(fk) TerritoryID : int**
  + **(fk) CountryRegionCode : nvarchar**
  ==
  <&pie-chart>** stats**
      total rows : 181
      total cols : 8
      data size : 200 KB
      index size : 48 KB
  --
}


entity "<&grid-three-up>** Production.ProductModelIllustration**" as Production.ProductModelIllustration { 
  + **(pk) ProductModelID : int**
  + **(pk) IllustrationID : int**
  --
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 7
      total cols : 3
      data size : 72 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** Production.ProductModelProductDescriptionCulture**" as Production.ProductModelProductDescriptionCulture { 
  + **(pk) ProductModelID : int**
  + **(pk) ProductDescriptionID : int**
  + **(pk) CultureID : nchar**
  --
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 762
      total cols : 4
      data size : 200 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** Production.BillOfMaterials**" as Production.BillOfMaterials { 
  + **(pk) BillOfMaterialsID : int**
  --
  - StartDate : datetime
  - EndDate : datetime
  - BOMLevel : smallint
  - PerAssemblyQty : decimal
  - ModifiedDate : datetime
  --
  + **(fk) UnitMeasureCode : nchar**
  + **(fk) ProductAssemblyID : int**
  + **(fk) ComponentID : int**
  ==
  <&pie-chart>** stats**
      total rows : 2,679
      total cols : 9
      data size : 328 KB
      index size : 184 KB
  --
}


entity "<&grid-three-up>** Sales.Store**" as Sales.Store { 
  + **(pk) BusinessEntityID : int**
  --
  - Name : nvarchar
  - Demographics : xml
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  --
  + **(fk) SalesPersonID : int**
  ==
  <&pie-chart>** stats**
      total rows : 701
      total cols : 6
      data size : 904 KB
      index size : 72 KB
  --
}


entity "<&grid-three-up>** Production.ProductPhoto**" as Production.ProductPhoto { 
  + **(pk) ProductPhotoID : int**
  --
  - ThumbNailPhoto : varbinary
  - ThumbnailPhotoFileName : nvarchar
  - LargePhoto : varbinary
  - LargePhotoFileName : nvarchar
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 101
      total cols : 6
      data size : 2,512 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** Production.ProductProductPhoto**" as Production.ProductProductPhoto { 
  + **(pk) ProductID : int**
  + **(pk) ProductPhotoID : int**
  --
  - Primary : bit
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 504
      total cols : 4
      data size : 72 KB
      index size : 32 KB
  --
}


entity "<&grid-three-up>** Production.TransactionHistory**" as Production.TransactionHistory { 
  + **(pk) TransactionID : int**
  --
  - ReferenceOrderID : int
  - ReferenceOrderLineID : int
  - TransactionDate : datetime
  - TransactionType : nchar
  - Quantity : int
  - ActualCost : money
  - ModifiedDate : datetime
  --
  + **(fk) ProductID : int**
  ==
  <&pie-chart>** stats**
      total rows : 113,443
      total cols : 9
      data size : 6,408 KB
      index size : 3,632 KB
  --
}


entity "<&grid-three-up>** Production.ProductReview**" as Production.ProductReview { 
  + **(pk) ProductReviewID : int**
  --
  - ReviewerName : nvarchar
  - ReviewDate : datetime
  - EmailAddress : nvarchar
  - Rating : int
  - Comments : nvarchar
  - ModifiedDate : datetime
  --
  + **(fk) ProductID : int**
  ==
  <&pie-chart>** stats**
      total rows : 4
      total cols : 8
      data size : 200 KB
      index size : 40 KB
  --
}


entity "<&grid-three-up>** Person.BusinessEntity**" as Person.BusinessEntity { 
  + **(pk) BusinessEntityID : int**
  --
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 20,777
      total cols : 3
      data size : 840 KB
      index size : 552 KB
  --
}


entity "<&grid-three-up>** Production.ProductSubcategory**" as Production.ProductSubcategory { 
  + **(pk) ProductSubcategoryID : int**
  --
  - Name : nvarchar
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  --
  + **(fk) ProductCategoryID : int**
  ==
  <&pie-chart>** stats**
      total rows : 37
      total cols : 5
      data size : 72 KB
      index size : 32 KB
  --
}


entity "<&grid-three-up>** Person.BusinessEntityAddress**" as Person.BusinessEntityAddress { 
  + **(pk) BusinessEntityID : int**
  + **(pk) AddressID : int**
  + **(pk) AddressTypeID : int**
  --
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 19,614
      total cols : 5
      data size : 968 KB
      index size : 1,416 KB
  --
}


entity "<&grid-three-up>** Purchasing.ProductVendor**" as Purchasing.ProductVendor { 
  + **(pk) ProductID : int**
  + **(pk) BusinessEntityID : int**
  --
  - AverageLeadTime : int
  - StandardPrice : money
  - LastReceiptCost : money
  - LastReceiptDate : datetime
  - MinOrderQty : int
  - MaxOrderQty : int
  - OnOrderQty : int
  - ModifiedDate : datetime
  --
  + **(fk) UnitMeasureCode : nchar**
  ==
  <&pie-chart>** stats**
      total rows : 460
      total cols : 11
      data size : 200 KB
      index size : 48 KB
  --
}


entity "<&grid-three-up>** Person.BusinessEntityContact**" as Person.BusinessEntityContact { 
  + **(pk) BusinessEntityID : int**
  + **(pk) PersonID : int**
  + **(pk) ContactTypeID : int**
  --
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 909
      total cols : 5
      data size : 200 KB
      index size : 128 KB
  --
}


entity "<&grid-three-up>** Production.UnitMeasure**" as Production.UnitMeasure { 
  + **(pk) UnitMeasureCode : nchar**
  --
  - Name : nvarchar
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 38
      total cols : 3
      data size : 72 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** Purchasing.Vendor**" as Purchasing.Vendor { 
  + **(pk) BusinessEntityID : int**
  --
  - AccountNumber : nvarchar
  - Name : nvarchar
  - CreditRating : tinyint
  - PreferredVendorStatus : bit
  - ActiveFlag : bit
  - PurchasingWebServiceURL : nvarchar
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 104
      total cols : 8
      data size : 200 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** Person.ContactType**" as Person.ContactType { 
  + **(pk) ContactTypeID : int**
  --
  - Name : nvarchar
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 20
      total cols : 3
      data size : 72 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** Sales.CountryRegionCurrency**" as Sales.CountryRegionCurrency { 
  + **(pk) CountryRegionCode : nvarchar**
  + **(pk) CurrencyCode : nchar**
  --
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 109
      total cols : 3
      data size : 72 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** Person.CountryRegion**" as Person.CountryRegion { 
  + **(pk) CountryRegionCode : nvarchar**
  --
  - Name : nvarchar
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 238
      total cols : 3
      data size : 200 KB
      index size : 32 KB
  --
}


entity "<&grid-three-up>** Production.WorkOrder**" as Production.WorkOrder { 
  + **(pk) WorkOrderID : int**
  --
  - OrderQty : int
  - StockedQty : int
  - ScrappedQty : smallint
  - StartDate : datetime
  - EndDate : datetime
  - DueDate : datetime
  - ModifiedDate : datetime
  --
  + **(fk) ProductID : int**
  + **(fk) ScrapReasonID : smallint**
  ==
  <&pie-chart>** stats**
      total rows : 72,591
      total cols : 10
      data size : 4,296 KB
      index size : 1,904 KB
  --
}


entity "<&grid-three-up>** Purchasing.PurchaseOrderDetail**" as Purchasing.PurchaseOrderDetail { 
  + **(pk) PurchaseOrderID : int**
  + **(pk) PurchaseOrderDetailID : int**
  --
  - DueDate : datetime
  - OrderQty : smallint
  - UnitPrice : money
  - LineTotal : money
  - ReceivedQty : decimal
  - RejectedQty : decimal
  - StockedQty : decimal
  - ModifiedDate : datetime
  --
  + **(fk) ProductID : int**
  ==
  <&pie-chart>** stats**
      total rows : 8,845
      total cols : 11
      data size : 584 KB
      index size : 176 KB
  --
}


entity "<&grid-three-up>** Sales.CreditCard**" as Sales.CreditCard { 
  + **(pk) CreditCardID : int**
  --
  - CardType : nvarchar
  - CardNumber : nvarchar
  - ExpMonth : tinyint
  - ExpYear : smallint
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 19,118
      total cols : 6
      data size : 1,608 KB
      index size : 816 KB
  --
}


entity "<&grid-three-up>** Production.Culture**" as Production.Culture { 
  + **(pk) CultureID : nchar**
  --
  - Name : nvarchar
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 8
      total cols : 3
      data size : 72 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** Production.WorkOrderRouting**" as Production.WorkOrderRouting { 
  + **(pk) WorkOrderID : int**
  + **(pk) ProductID : int**
  + **(pk) OperationSequence : smallint**
  --
  - ScheduledStartDate : datetime
  - ScheduledEndDate : datetime
  - ActualStartDate : datetime
  - ActualEndDate : datetime
  - ActualResourceHrs : decimal
  - PlannedCost : money
  - ActualCost : money
  - ModifiedDate : datetime
  --
  + **(fk) LocationID : smallint**
  ==
  <&pie-chart>** stats**
      total rows : 67,131
      total cols : 12
      data size : 5,640 KB
      index size : 1,080 KB
  --
}


entity "<&grid-three-up>** Sales.Currency**" as Sales.Currency { 
  + **(pk) CurrencyCode : nchar**
  --
  - Name : nvarchar
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 105
      total cols : 3
      data size : 72 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** Purchasing.PurchaseOrderHeader**" as Purchasing.PurchaseOrderHeader { 
  + **(pk) PurchaseOrderID : int**
  --
  - RevisionNumber : tinyint
  - Status : tinyint
  - OrderDate : datetime
  - ShipDate : datetime
  - SubTotal : money
  - TaxAmt : money
  - Freight : money
  - TotalDue : money
  - ModifiedDate : datetime
  --
  + **(fk) EmployeeID : int**
  + **(fk) VendorID : int**
  + **(fk) ShipMethodID : int**
  ==
  <&pie-chart>** stats**
      total rows : 4,012
      total cols : 13
      data size : 456 KB
      index size : 144 KB
  --
}


entity "<&grid-three-up>** Sales.CurrencyRate**" as Sales.CurrencyRate { 
  + **(pk) CurrencyRateID : int**
  --
  - CurrencyRateDate : datetime
  - AverageRate : money
  - EndOfDayRate : money
  - ModifiedDate : datetime
  --
  + **(fk) FromCurrencyCode : nchar**
  + **(fk) ToCurrencyCode : nchar**
  ==
  <&pie-chart>** stats**
      total rows : 13,532
      total cols : 7
      data size : 840 KB
      index size : 424 KB
  --
}


entity "<&grid-three-up>** Sales.Customer**" as Sales.Customer { 
  + **(pk) CustomerID : int**
  --
  - AccountNumber : varchar
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  --
  + **(fk) PersonID : int**
  + **(fk) StoreID : int**
  + **(fk) TerritoryID : int**
  ==
  <&pie-chart>** stats**
      total rows : 19,820
      total cols : 7
      data size : 1,096 KB
      index size : 1,312 KB
  --
}


entity "<&grid-three-up>** HumanResources.Department**" as HumanResources.Department { 
  + **(pk) DepartmentID : smallint**
  --
  - Name : nvarchar
  - GroupName : nvarchar
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 16
      total cols : 4
      data size : 72 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** Production.Document**" as Production.Document { 
  + **(pk) DocumentNode : hierarchyid**
  --
  - DocumentLevel : smallint
  - Title : nvarchar
  - FolderFlag : bit
  - FileName : nvarchar
  - FileExtension : nvarchar
  - Revision : nchar
  - ChangeNumber : int
  - Status : tinyint
  - DocumentSummary : nvarchar
  - Document : varbinary
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  --
  + **(fk) Owner : int**
  ==
  <&pie-chart>** stats**
      total rows : 13
      total cols : 14
      data size : 464 KB
      index size : 64 KB
  --
}


entity "<&grid-three-up>** Sales.SalesOrderDetail**" as Sales.SalesOrderDetail { 
  + **(pk) SalesOrderID : int**
  + **(pk) SalesOrderDetailID : int**
  --
  - CarrierTrackingNumber : nvarchar
  - OrderQty : smallint
  - UnitPrice : money
  - UnitPriceDiscount : money
  - LineTotal : numeric
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  --
  + **(fk) ProductID : int**
  + **(fk) SpecialOfferID : int**
  ==
  <&pie-chart>** stats**
      total rows : 121,317
      total cols : 11
      data size : 9,992 KB
      index size : 5,824 KB
  --
}


entity "<&grid-three-up>** Person.EmailAddress**" as Person.EmailAddress { 
  + **(pk) BusinessEntityID : int**
  + **(pk) EmailAddressID : int**
  --
  - EmailAddress : nvarchar
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 19,972
      total cols : 5
      data size : 2,120 KB
      index size : 1,488 KB
  --
}


entity "<&grid-three-up>** HumanResources.Employee**" as HumanResources.Employee { 
  + **(pk) BusinessEntityID : int**
  --
  - NationalIDNumber : nvarchar
  - LoginID : nvarchar
  - OrganizationNode : hierarchyid
  - OrganizationLevel : smallint
  - JobTitle : nvarchar
  - BirthDate : date
  - MaritalStatus : nchar
  - Gender : nchar
  - HireDate : date
  - SalariedFlag : bit
  - VacationHours : smallint
  - SickLeaveHours : smallint
  - CurrentFlag : bit
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 290
      total cols : 16
      data size : 136 KB
      index size : 120 KB
  --
}


entity "<&grid-three-up>** Sales.SalesOrderHeader**" as Sales.SalesOrderHeader { 
  + **(pk) SalesOrderID : int**
  --
  - RevisionNumber : tinyint
  - OrderDate : datetime
  - DueDate : datetime
  - ShipDate : datetime
  - Status : tinyint
  - OnlineOrderFlag : bit
  - SalesOrderNumber : nvarchar
  - PurchaseOrderNumber : nvarchar
  - AccountNumber : nvarchar
  - CreditCardApprovalCode : varchar
  - SubTotal : money
  - TaxAmt : money
  - Freight : money
  - TotalDue : money
  - Comment : nvarchar
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  --
  + **(fk) CurrencyRateID : int**
  + **(fk) CustomerID : int**
  + **(fk) SalesPersonID : int**
  + **(fk) TerritoryID : int**
  + **(fk) BillToAddressID : int**
  + **(fk) ShipToAddressID : int**
  + **(fk) ShipMethodID : int**
  + **(fk) CreditCardID : int**
  ==
  <&pie-chart>** stats**
      total rows : 31,465
      total cols : 26
      data size : 5,576 KB
      index size : 2,632 KB
  --
}


entity "<&grid-three-up>** HumanResources.EmployeeDepartmentHistory**" as HumanResources.EmployeeDepartmentHistory { 
  + **(pk) BusinessEntityID : int**
  + **(pk) DepartmentID : smallint**
  + **(pk) ShiftID : tinyint**
  + **(pk) StartDate : date**
  --
  - EndDate : date
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 296
      total cols : 6
      data size : 200 KB
      index size : 32 KB
  --
}


entity "<&grid-three-up>** HumanResources.EmployeePayHistory**" as HumanResources.EmployeePayHistory { 
  + **(pk) BusinessEntityID : int**
  + **(pk) RateChangeDate : datetime**
  --
  - Rate : money
  - PayFrequency : tinyint
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 316
      total cols : 5
      data size : 200 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** Sales.SalesOrderHeaderSalesReason**" as Sales.SalesOrderHeaderSalesReason { 
  + **(pk) SalesOrderID : int**
  + **(pk) SalesReasonID : int**
  --
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 27,647
      total cols : 3
      data size : 776 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** Sales.SalesPerson**" as Sales.SalesPerson { 
  + **(pk) BusinessEntityID : int**
  --
  - SalesQuota : money
  - Bonus : money
  - CommissionPct : smallmoney
  - SalesYTD : money
  - SalesLastYear : money
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  --
  + **(fk) TerritoryID : int**
  ==
  <&pie-chart>** stats**
      total rows : 17
      total cols : 9
      data size : 72 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** Production.Illustration**" as Production.Illustration { 
  + **(pk) IllustrationID : int**
  --
  - Diagram : xml
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 5
      total cols : 3
      data size : 400 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** HumanResources.JobCandidate**" as HumanResources.JobCandidate { 
  + **(pk) JobCandidateID : int**
  --
  - Resume : xml
  - ModifiedDate : datetime
  --
  + **(fk) BusinessEntityID : int**
  ==
  <&pie-chart>** stats**
      total rows : 13
      total cols : 4
      data size : 400 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** Production.Location**" as Production.Location { 
  + **(pk) LocationID : smallint**
  --
  - Name : nvarchar
  - CostRate : smallmoney
  - Availability : decimal
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 14
      total cols : 5
      data size : 72 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** Person.Password**" as Person.Password { 
  + **(pk) BusinessEntityID : int**
  --
  - PasswordHash : varchar
  - PasswordSalt : varchar
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 19,972
      total cols : 5
      data size : 1,992 KB
      index size : 0 KB
  --
}


entity "<&grid-three-up>** Sales.SalesPersonQuotaHistory**" as Sales.SalesPersonQuotaHistory { 
  + **(pk) BusinessEntityID : int**
  + **(pk) QuotaDate : datetime**
  --
  - SalesQuota : money
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 163
      total cols : 5
      data size : 200 KB
      index size : 16 KB
  --
}


entity "<&grid-three-up>** Person.Person**" as Person.Person { 
  + **(pk) BusinessEntityID : int**
  --
  - PersonType : nchar
  - NameStyle : bit
  - Title : nvarchar
  - FirstName : nvarchar
  - MiddleName : nvarchar
  - LastName : nvarchar
  - Suffix : nvarchar
  - EmailPromotion : int
  - AdditionalContactInfo : xml
  - Demographics : xml
  - rowguid : uniqueidentifier
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 19,972
      total cols : 13
      data size : 30,536 KB
      index size : 1,376 KB
  --
}


entity "<&grid-three-up>** Sales.SalesReason**" as Sales.SalesReason { 
  + **(pk) SalesReasonID : int**
  --
  - Name : nvarchar
  - ReasonType : nvarchar
  - ModifiedDate : datetime
  ==
  <&pie-chart>** stats**
      total rows : 10
      total cols : 4
      data size : 72 KB
      index size : 0 KB
  --
}

HumanResources.Employee ||.d.o{ Person.Person : businessentityid
HumanResources.EmployeeDepartmentHistory ||.l.o{ HumanResources.Department : departmentid
HumanResources.EmployeeDepartmentHistory ||.u.o{ HumanResources.Employee : businessentityid
HumanResources.EmployeeDepartmentHistory ||.r.o{ HumanResources.Shift : shiftid
HumanResources.EmployeePayHistory ||.d.o{ HumanResources.Employee : businessentityid
HumanResources.JobCandidate ||.l.o{ HumanResources.Employee : businessentityid
Person.Address ||.u.o{ Person.StateProvince : stateprovinceid
Person.BusinessEntityAddress ||.r.o{ Person.Address : addressid
Person.BusinessEntityAddress ||.d.o{ Person.AddressType : addresstypeid
Person.BusinessEntityAddress ||.l.o{ Person.BusinessEntity : businessentityid
Person.BusinessEntityContact ||.u.o{ Person.BusinessEntity : businessentityid
Person.BusinessEntityContact ||.r.o{ Person.ContactType : contacttypeid
Person.BusinessEntityContact ||.d.o{ Person.Person : personid
Person.EmailAddress ||.l.o{ Person.Person : businessentityid
Person.Password ||.u.o{ Person.Person : businessentityid
Person.Person ||.r.o{ Person.BusinessEntity : businessentityid
Person.PersonPhone ||.d.o{ Person.Person : businessentityid
Person.PersonPhone ||.l.o{ Person.PhoneNumberType : phonenumbertypeid
Person.StateProvince ||.u.o{ Person.CountryRegion : countryregioncode
Person.StateProvince ||.r.o{ Sales.SalesTerritory : territoryid
Production.BillOfMaterials ||.d.o{ Production.Product : productassemblyid
Production.BillOfMaterials ||.l.o{ Production.Product : componentid
Production.BillOfMaterials ||.u.o{ Production.UnitMeasure : unitmeasurecode
Production.Document ||.r.o{ HumanResources.Employee : owner
Production.Product ||.d.o{ Production.ProductModel : productmodelid
Production.Product ||.l.o{ Production.ProductSubcategory : productsubcategoryid
Production.Product ||.u.o{ Production.UnitMeasure : sizeunitmeasurecode
Production.Product ||.r.o{ Production.UnitMeasure : weightunitmeasurecode
Production.ProductCostHistory ||.d.o{ Production.Product : productid
Production.ProductDocument ||.l.o{ Production.Document : documentnode
Production.ProductDocument ||.u.o{ Production.Product : productid
Production.ProductInventory ||.r.o{ Production.Location : locationid
Production.ProductInventory ||.d.o{ Production.Product : productid
Production.ProductListPriceHistory ||.l.o{ Production.Product : productid
Production.ProductModelIllustration ||.u.o{ Production.Illustration : illustrationid
Production.ProductModelIllustration ||.r.o{ Production.ProductModel : productmodelid
Production.ProductModelProductDescriptionCulture ||.d.o{ Production.Culture : cultureid
Production.ProductModelProductDescriptionCulture ||.l.o{ Production.ProductDescription : productdescriptionid
Production.ProductModelProductDescriptionCulture ||.u.o{ Production.ProductModel : productmodelid
Production.ProductProductPhoto ||.r.o{ Production.Product : productid
Production.ProductProductPhoto ||.d.o{ Production.ProductPhoto : productphotoid
Production.ProductReview ||.l.o{ Production.Product : productid
Production.ProductSubcategory ||.u.o{ Production.ProductCategory : productcategoryid
Production.TransactionHistory ||.r.o{ Production.Product : productid
Production.WorkOrder ||.d.o{ Production.Product : productid
Production.WorkOrder ||.l.o{ Production.ScrapReason : scrapreasonid
Production.WorkOrderRouting ||.u.o{ Production.Location : locationid
Production.WorkOrderRouting ||.r.o{ Production.WorkOrder : workorderid
Purchasing.ProductVendor ||.d.o{ Production.Product : productid
Purchasing.ProductVendor ||.l.o{ Production.UnitMeasure : unitmeasurecode
Purchasing.ProductVendor ||.u.o{ Purchasing.Vendor : businessentityid
Purchasing.PurchaseOrderDetail ||.r.o{ Production.Product : productid
Purchasing.PurchaseOrderDetail ||.d.o{ Purchasing.PurchaseOrderHeader : purchaseorderid
Purchasing.PurchaseOrderHeader ||.l.o{ HumanResources.Employee : employeeid
Purchasing.PurchaseOrderHeader ||.u.o{ Purchasing.ShipMethod : shipmethodid
Purchasing.PurchaseOrderHeader ||.r.o{ Purchasing.Vendor : vendorid
Purchasing.Vendor ||.d.o{ Person.BusinessEntity : businessentityid
Sales.CountryRegionCurrency ||.l.o{ Person.CountryRegion : countryregioncode
Sales.CountryRegionCurrency ||.u.o{ Sales.Currency : currencycode
Sales.CurrencyRate ||.r.o{ Sales.Currency : fromcurrencycode
Sales.CurrencyRate ||.d.o{ Sales.Currency : tocurrencycode
Sales.Customer ||.l.o{ Person.Person : personid
Sales.Customer ||.u.o{ Sales.SalesTerritory : territoryid
Sales.Customer ||.r.o{ Sales.Store : storeid
Sales.PersonCreditCard ||.d.o{ Person.Person : businessentityid
Sales.PersonCreditCard ||.l.o{ Sales.CreditCard : creditcardid
Sales.SalesOrderDetail ||.u.o{ Sales.SalesOrderHeader : salesorderid
Sales.SalesOrderDetail ||.r.o{ Sales.SpecialOfferProduct : productid, specialofferid
Sales.SalesOrderHeader ||.d.o{ Person.Address : billtoaddressid
Sales.SalesOrderHeader ||.l.o{ Person.Address : shiptoaddressid
Sales.SalesOrderHeader ||.u.o{ Purchasing.ShipMethod : shipmethodid
Sales.SalesOrderHeader ||.r.o{ Sales.CreditCard : creditcardid
Sales.SalesOrderHeader ||.d.o{ Sales.CurrencyRate : currencyrateid
Sales.SalesOrderHeader ||.l.o{ Sales.Customer : customerid
Sales.SalesOrderHeader ||.u.o{ Sales.SalesPerson : salespersonid
Sales.SalesOrderHeader ||.r.o{ Sales.SalesTerritory : territoryid
Sales.SalesOrderHeaderSalesReason ||.d.o{ Sales.SalesOrderHeader : salesorderid
Sales.SalesOrderHeaderSalesReason ||.l.o{ Sales.SalesReason : salesreasonid
Sales.SalesPerson ||.u.o{ HumanResources.Employee : businessentityid
Sales.SalesPerson ||.r.o{ Sales.SalesTerritory : territoryid
Sales.SalesPersonQuotaHistory ||.d.o{ Sales.SalesPerson : businessentityid
Sales.SalesTaxRate ||.l.o{ Person.StateProvince : stateprovinceid
Sales.SalesTerritory ||.u.o{ Person.CountryRegion : countryregioncode
Sales.SalesTerritoryHistory ||.r.o{ Sales.SalesPerson : businessentityid
Sales.SalesTerritoryHistory ||.d.o{ Sales.SalesTerritory : territoryid
Sales.ShoppingCartItem ||.l.o{ Production.Product : productid
Sales.SpecialOfferProduct ||.u.o{ Production.Product : productid
Sales.SpecialOfferProduct ||.r.o{ Sales.SpecialOffer : specialofferid
Sales.Store ||.d.o{ Person.BusinessEntity : businessentityid
Sales.Store ||.l.o{ Sales.SalesPerson : salespersonid

'# manual relation section 
tbl_aaa .. tbl_bbb

@enduml