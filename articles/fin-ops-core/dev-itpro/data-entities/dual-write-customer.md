---
title: 集成客户主控
description: 本主题介绍 Finance and Operations 与 Common Data Service 之间的客户数据集成。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6c8c94eb8ff04d489eb24b7e0f4642aef20a3b18
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182040"
---
## <a name="integrated-customer-master"></a>集成客户主控

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

客户记录通常主控在多个应用程序中。 例如，销售活动可通过 Sales 应用程序获取商业客户记录，而电子商务和零售则可通过 Finance and Operations 应用程序获取客户记录。 无论客户记录源自何处，都跨越应用程序边界和基础结构差异在后台集成。 集成客户主控可以帮助处理多主控场景，并提供客户对 Dynamics 365 应用程序套件丰富的见解。

## <a name="customer-data-flow"></a>客户数据流

*客户*是应用程序中精心定义的概念。 因此，客户数据的集成包括在这两个应用程序之间协调客户概念。 下图显示客户数据流。

![客户数据流](media/dual-write-customer-data-flow.png)

客户可以大致分为两类：商业/组织客户和消费者/最终用户。 这两种类型的客户存储在 Finance and Operations 和 Common Data Service 中并以不同方式处理。

在 Finance and Operations 中，商业/组织客户和消费者/最终用户在名为 **CustTable** (CustomerCustomerV3Entity) 的一个表中主控，并根据**类型**属性分类。 （如果**类型**设置为**组织**，则客户为商业/组织客户，如果**类型**设置为**个人**，则客户为消费者/最终用户。）主联系人信息通过 SMMContactPersonEntity 实体处理。

在 Common Data Service 中，商业/组织客户在“客户”实体中主控，并在 **RelationshipType** 属性设置为**客户**时标识为客户。 消费者/最终用户和联系人均通过联系人实体表示。 为了提供客户/最终用户与联系人之间的清晰界限，**联系人**实体有一个布尔值标记，名称为 **Sellable**。 如果 **Sellable** 为 **True**，则联系人为消费者/最终用户，可以为该联系人创建报价单和订单。 如果 **Sellable** 为 **False**，则联系人只是客户的主要联系人。

如果非适销联系人参与报价单或订单流程，则 **Sellable** 设置为 **True** 以将该联系人标记为适销联系人。 已成为适销联系人的联系人仍是适销联系人。

## <a name="templates"></a>模板

客户数据包括有关客户的所有信息，如客户组、地址、联系信息、付款配置文件、发票配置文件和会员状态。 客户数据交互期间，实体映射集合协同工作，如下表中所示。

Finance and Operations 应用    | 其他 Dynamics 365 应用
--------------------------|---------------------------------
客户 V3               | 科目
客户 V3               | 联系人
CDS 联系人 V2           | 联系人
客户组           | Msdyn\_customergroups
客户付款方式   | Msdyn\_customerpaymentmethods
会员卡              | Msdyn\_loyaltycards
付款计划          | Msdyn\_paymentschedules
付款计划          | Msdyn\_paymentschedulelines
付款日 CDS           | Msdyn\_paymentdays
付款日行 CDS     | Msdyn\_paymentdaylines
付款期限          | Msdyn\_paymentterms
名称词缀              | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="customer-v3-to-account"></a>客户 3 到帐户

此模板在 Finance and Operations 应用与 Common Data Service 之间同步商业客户和组织客户的客户主信息。

<!-- ![](media/dual-write-account-1.png) -->

<!-- ![](media/dual-write-account-2.png) -->

源字段 | 映射类型 | 目标字段
---|---|---
CUSTOMERACCOUNT | = | accountnumber
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
CREDITLIMIT | = | creditlimit
DELIVERYADDRESSCITY | = | address1\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
DELIVERYADDRESSCOUNTY | = | address1\_county
DELIVERYADDRESSLATITUDE | \> | address1\_latitude
DELIVERYADDRESSLONGITUDE | \> | address1\_longitude
DELIVERYADDRESSZIPCODE | = | address1\_postalcode
ORGANIZATIONNAME | = | name
ORGANIZATIONNUMBEROFEMPLOYEES | = | numberofemployees
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTTWITTER | = | primarytwitterid
PRIMARYCONTACTURL | = | websiteurl
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | 描述
CREDITLIMITISMANDATORY | \>\< | msdyn\_creditlimitismandatory
CREDITRATING | = | msdyn\_creditrating
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
INVOICEACCOUNT | = | msdyn\_billingaccount.accountnumber
INVOICEADDRESS | \>\< | msdyn\_invoiceaddress
ISONETIMECUSTOMER | \>\< | msdyn\_onetimecustomer
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PAYMENTDAY | = | msdyn\_paymentday.msdyn\_name
PAYMENTMETHOD | = | msdyn\_customerpaymentmethod.msdyn\_name
PAYMENTSCHEDULE | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTTERMS | = | msdyn\_paymentterm.msdyn\_name
PAYMENTTERMSBASEDAYS | = | msdyn\_paymenttermsbasedays
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
PRIMARYCONTACTLINKEDIN | = | msdyn\_primarylinkedinid
TAXEXEMPTNUMBER | = | msdyn\_taxexemptnumber
VENDORACCOUNT | = | msdyn\_vendor.msdyn\_vendoraccountnumber
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
LANGUAGEID | \<\< | 无
DELIVERYADDRESSSTREET | = | address1\_line1
DELIVERYADDRESSSTATE | = | address1\_stateorprovince
无 | \>\> | address1\_addresstypecode
无 | \>\> | customertypecode
PARTYTYPE | \<\< | 无
PARTYNUMBER | = | msdyn\_partynumber

## <a name="customer-v3-to-contact"></a>客户 V3 到联系人

此模板在 Finance and Operations 与其他 Dynamics 365 应用之间同步消费者和最终用户的客户主数据。

<!-- ![](media/dual-write-contact-1.png) -->
<!-- ![](media/dual-write-contact-2.png) -->

源字段 | 映射类型 | 目标字段
---|---|---
无 | \>\> | msdyn\_sellable
PARTYTYPE | \<\< | 无
PARTYNUMBER | = | msdyn\_partynumber
CUSTOMERACCOUNT | = | msdyn\_contactpersonid
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
PERSONFIRSTNAME | = | firstname
PERSONLASTNAME | = | lastname
PERSONMIDDLENAME | = | middlename
PERSONPROFESSIONALTITLE | = | jobtitle
PERSONGENDER | \>\< | gendercode
PERSONMARITALSTATUS | \>\< | familystatuscode
LANGUAGEID | \<\< | 无
ADDRESSCITY | = | address1\_city
ADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
ADDRESSCOUNTY | = | address1\_county
ADDRESSLATITUDE | \> | address1\_latitude
ADDRESSLONGITUDE | \> | address1\_longitude
ADDRESSLOCATIONROLES | \<\< | 无
ADDRESSSTATE | = | address1\_stateorprovince
ADDRESSSTREET | = | address1\_line1
ADDRESSZIPCODE | = | address1\_postalcode
ADDRESSPOSTBOX | = | address1\_postofficebox
无 | \>\> | address1\_addresstypecode
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
无 | \>\> | address2\_addresstypecode
DELIVERYADDRESSCITY | = | address3\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address3\_country
DELIVERYADDRESSCOUNTY | = | address3\_county
DELIVERYADDRESSLATITUDE | \> | address3\_latitude
DELIVERYADDRESSLONGITUDE | \>\> | address3\_longitude
DELIVERYADDRESSSTATE | = | address3\_stateorprovince
DELIVERYADDRESSSTREET | = | address3\_line1
DELIVERYADDRESSZIPCODE | = | address3\_postalcode
无 | \>\> | address3\_addresstypecode
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTLINKEDIN | = | msdyn\_primaryinkedinid
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTER | = | msdyn\_primarytwitterid
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURL | = | websiteurl
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | 描述

## <a name="contacts"></a>联系人

此模板在 Finance and Operations 与其他 Dynamics 365 应用之间同步客户和供应商的所有第一、第二和第三联系人信息。

<!-- ![](media/dual-write-contacts.png) -->

源字段 | 映射类型 | 目标字段
---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn\_partynumber
ASSOCIATEDCONTACTTYPE | \<\< | 无
FIRSTNAME | = | firstname
MIDDLENAME | = | middlename
LASTNAME | = | lastname
ASSOCIATEDCONTACTNUMBER | = | msdyn\_vendorcontactid.msdyn\_vendoraccountnumber
PRIMARYADDRESSCITY | = | address1\_city
PRIMARYADDRESSCOUNTRYREGIONID | = | address1\_country
PRIMARYADDRESSCOUNTYID | = | address1\_county
PRIMARYFAXNUMBER | = | fax
PRIMARYADDRESSSTATEID | = | address1\_stateorprovince
PRIMARYADDRESSSTREET | = | address1\_line1
PRIMARYADDRESSZIPCODE | = | address1\_postalcode
PRIMARYPHONENUMBER | = | telephone1
PRIMARYEMAILADDRESS | = | emailaddress1
EMPLOYMENTDEPARTMENT | = | 部门
NOTES | = | 描述
GENDER | \>\< | gendercode
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid
PRIMARYURL | = | websiteurl
MARITALSTATUS | \>\< | familystatuscode
ISRECEIVINGDIRECTMAIL | \>\< | donotemail
EMPLOYMENTPROFESSION | = | jobtitle
SPOUSENAME | = | spousesname
无 | \>\> | msdyn\_contactforvendor
无 | \>\> | msdyn\_contactpersonid

## <a name="customer-groups"></a>客户组

此模板在 Finance and Operations 与其他 Dynamics 365 应用之间同步客户组信息。

<!-- ![](media/dual-write-customer-groups.png) -->

源字段 | 映射类型 | 目标字段
---|---|---
CUSTOMERGROUPID | = | msdyn\_groupid
描述 | = | msdyn\_description
ISSALESTAXINCLUDEDINPRICE | \>\< | msdyn\_issalestaxincludedinprice
PAYMENTTERMID | = | msdyn\_paymenttermid.msdyn\_name
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymenttermname.msdyn\_name

## <a name="customer-payment-methods"></a>客户付款方式

此模板在 Finance and Operations 与其他 Dynamics 365 应用之间同步客户付款方式信息。

<!-- ![](media/dual-write-customer-payment-methods.png) -->

源字段 | 映射类型 | 目标字段
---|---|---
名称 | = | msdyn\_name
ACCOUNTTYPE | \>\< | msdyn\_accounttype
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingpostingenabled
ISSEPA | \>\< | msdyn\_issepa
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
描述 | = | msdyn\_description
PAYMENTTYPE | \>\< | msdyn\_paymenttype
CREATEANDDRAWBILLOFEXCHANGEDURINGINVOICEPOSTING | \>\< | msdyn\_invoiceupdate
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_enablepostdatescheckclearingposting
BILLOFEXCHANGEDRAFTTYPE | \>\< | msdyn\_billofexchangedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

## <a name="loyalty-cards"></a>会员卡

此模板在 Finance and Operations 与其他 Dynamics 365 应用之间同步客户会员卡信息。

<!-- ![](media/dual-write-loyalty-cards.png) -->

源字段 | 映射类型 | 目标字段
---|---|---
CARDNUMBER | = | msdyn\_cardnumber
CARDTENDERTYPE | \>\< | msdyn\_cardtendertype
PARTYNUMBER | = | msdyn\_partynumber
REPLACEMENTCARDNUMBER | \> | msdyn\_replacementcardnumber
OMOPERATINGUNITNUMBER | = | msdyn\_operatingunitnumber
LOYALTYENROLLMENTDATE | = | msdyn\_enrollmentdate

## <a name="payment-schedules"></a>付款计划

此模板在 Finance and Operations 与其他 Dynamics 365 应用之间同步客户和供应商的付款计划引用数据。

<!-- ![](media/dual-write-payment-schedules.png) -->

源字段 | 映射类型 | 目标字段
---|---|---
名称 | = | msdyn\_name
描述 | = | msdyn\_description
ALLOCATIONMETHOD | \>\< | msdyn\_allocationmethod
PAYMENTFREQUENCYUNITS | \>\< | msdyn\_paymentfrequencyunit
PAYMENTFREQUENCY | = | msdyn\_paymentfrequency
NUMBEROFPAYMENTS | = | msdyn\_numberofpayments
FIXEDPAYMENTAMOUNT | = | msdyn\_fixedpaymentamount
MINIMUMPAYMENTAMOUNT | = | msdyn\_minimumpaymentamount
SALESTAXALLOCATIONMETHOD | \>\< | msdyn\_salestaxallocationmethod
注释 | = | msdyn\_note

## <a name="payment-schedule-lines"></a>付款计划行

在 Finance and Operations 与其他 Dynamics 365 应用之间同步客户和供应商的付款计划行引用数据。

<!-- ![](media/dual-write-payment-schedule-lines.png) -->

源字段 | 映射类型 | 目标字段
---|---|---
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTSCHEDULENAME | \> | msdyn\_name
LINENUMBER | = | msdyn\_linenumber
PERIODSAFTERDUEDATE | = | msdyn\_periodsafterduedate
PERCENTORAMOUNT | \>\< | msdyn\_percentoramount
PERCENTORAMOUNTVALUE | = | msdyn\_percentoramountvalue

## <a name="payment-days"></a>付款日

此模板在 Finance and Operations 与其他 Dynamics 365 应用之间同步客户和供应商的付款日引用数据。

<!-- ![](media/dual-write-payment-days.png) -->

源字段 | 映射类型 | 目标字段
---|---|---
名称 | = | msdyn\_name
描述 | = | msdyn\_description

## <a name="payment-day-lines"></a>付款天数行

此模板在 Finance and Operations 与其他 Dynamics 365 应用之间同步客户和供应商的付款日行引用数据。

<!-- ![](media/dual-write-payment-day-lines.png) -->

源字段 | 映射类型 | 目标字段
---|---|---
CDSINTEGRATIONKEY | = | msdyn\_paymentdaylineid
FREQUENCY | \>\< | msdyn\_frequency
DAYOFWEEK | \>\< | msdyn\_dayofweek
DAYOFMONTH | = | msdyn\_dayofmonth
名称 | = | msdyn\_paymentday.msdyn\_name

## <a name="payment-terms"></a>付款条款

此模板在 Finance and Operations 与其他 Dynamics 365 应用之间同步客户和供应商的付款期限引用数据。

<!-- ![](media/dual-write-payment-terms.png) -->

源字段 | 映射类型 | 目标字段
---|---|---
描述 | = | msdyn\_description
名称 | = | msdyn\_name
NUMBEROFMONTHS | = | msdyn\_numberofmonth
CUTOFFDAYOFMONTH | = | msdyn\_cutoffdayofmonth
ISCASHPAYMENT | \>\< | msdyn\_iscashpayment
NUMBEROFDAYS | = | msdyn\_days
ISCERTIFIEDCOMPANYCHECK | \>\< | msdyn\_iscertifiedcompanycheck
ISDEFAULTPAYMENTTERM | \>\< | msdyn\_isdefaultpaymentterm
CREDITCARDPAYMENTTYPE | \>\< | msdyn\_creditcardpaymenttype
CREDITCARDCREDITCHECKTYPE | \>\< | msdyn\_creditcardcreditchecktype
PAYMENTDAYNAME | = | msdyn\_paymentdayname.msdyn\_name
PAYMENTMETHODTYPE | \>\< | msdyn\_paymentmethodtype
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedulename.msdyn\_name

## <a name="name-affixes"></a>名称词缀

此模板在 Finance and Operations 与其他 Dynamics 365 应用之间同步客户和供应商的名称词缀引用数据。

<!-- ![](media/dual-write-name-affixes.png) -->

源字段 | 映射类型 | 目标字段
---|---|---
词缀 | = | msdyn\_affix
类型 | \>\< | msdyn\_affixtype
描述 | = | msdyn\_description
