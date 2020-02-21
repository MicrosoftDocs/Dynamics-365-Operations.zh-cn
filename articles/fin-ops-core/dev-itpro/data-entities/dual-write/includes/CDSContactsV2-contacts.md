## <a name="cds-contacts-v2-to-contacts"></a>CDS 联系人 V2 到联系人

此模板在 Finance and Operations 应用与 Common Data Service 之间同步数据。

源筛选器：(AssociatedContactType = 1)

反向源筛选器：msdyn_contactforvendor eq true and msdyn_sellable eq false and msdyn_contactpersonid ne ''

Finance and Operations 字段 | 映射类型 | 其他 Dynamics 365 字段 | 默认值
---|---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn_partynumber | 
ASSOCIATEDCONTACTTYPE | << | none | Vendor
FIRSTNAME | = | firstname | 
MIDDLENAME | = | middlename | 
LASTNAME | = | lastname | 
ASSOCIATEDCONTACTNUMBER | = | msdyn_vendorcontactid.msdyn_vendoraccountnumber | 
PRIMARYADDRESSCITY | = | address1_city | 
PRIMARYADDRESSCOUNTRYREGIONID | = | address1_country | 
PRIMARYADDRESSCOUNTYID | = | address1_county | 
PRIMARYFAXNUMBER | = | fax | 
PRIMARYADDRESSSTATEID | = | address1_stateorprovince | 
PRIMARYADDRESSSTREET | = | address1_line1 | 
PRIMARYADDRESSZIPCODE | = | address1_postalcode | 
PRIMARYPHONENUMBER | = | telephone1 | 
PRIMARYEMAILADDRESS | = | emailaddress1 | 
EMPLOYMENTDEPARTMENT | = | department | 
NOTES | = | description | 
GENDER | >< | gendercode | 
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid | 
PRIMARYURL | = | websiteurl | 
MARITALSTATUS | >< | familystatuscode | 
ISRECEIVINGDIRECTMAIL | >< | donotemail | 
EMPLOYMENTPROFESSION | = | jobtitle | 
SPOUSENAME | = | spousesname | 
none | >> | msdyn_contactforvendor | True
CONTACTPERSONID | = | msdyn_contactpersonid | 
