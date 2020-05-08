---
title: 实体依赖关系链（同步顺序）
description: 本主题指定创建初始数据时必须遵守的同步顺序。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: 9ae14703941b97308bca5845eeac3eb9b181ae75
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275479"
---
# <a name="entity-dependency-chain-synchronization-order"></a>实体依赖关系链（同步顺序）

[!include [banner](../../includes/banner.md)]

本主题指定如果不使用**初始同步**功能提供的实体依赖项，创建初始数据必须遵循的同步顺序。 如果您不使用**初始同步**，则必须分别运行每个实体映射。

## <a name="dynamics-365-supply-chain-management-entities"></a>Dynamics 365 Supply Chain Management 实体

Supply Chain Management 的以下实体将按其应该启用的顺序列出。

| 双写入页面上的映射名称 | Supply Chain Management 中的实体元数据名称 | Common Data Service 中的实体元数据名称 | 说明 |
|---|---|---|---|
| 单位...uoms                                                                      | UnitOfMeasureEntity                                    | uom                                          | |
| 单位转换...msdyn_unitofmeasureconversions                                 | UnitOfMeasureConversionEntity                          | msdyn_unitofmeasureconversion                | |
| 所有产品...msdyn_globalproducts                                               | EcoResEveryProductEntity                               | msdyn_globalproduct                          | |
| 产品维度组...msdyn_productdimensiongroups                           | EcoResProductDimensionGroupEntity                      | msdyn_productdimensiongroup                  | |
| 存储维度组...msdyn_productstoragedimensiongroups                    | EcoResStorageDimensionGroupEntity                      | msdyn_productstoragedimensiongroup           | |
| 跟踪维度组...msdyn_producttrackingdimensiongroups                  | EcoResTrackingDimensionGroupEntity                     | msdyn_producttrackingdimensiongroup          | |
| 颜色...msdyn_productcolors                                                      | EcoResProductColorEntity                               | msdyn_productcolor                           | |
| 大小...msdyn_productsizes                                                        | EcoResProductSizeEntity                                | msdyn_productsize                            | |
| 样式...msdyn_productstyles                                                      | EcoResProductStyleEntity                               | msdyn_productstyle                           | |
| 配置...msdyn_productconfigurations                                      | EcoResProductConfigurationEntity                       | msdyn_productconfiguration                   | |
| 发放的产品 V2...msdyn_sharedproductdetails                                 | EcoResReleasedProductV2Entity                          | msdyn_sharedproductdetail                    | |
| Common Data Service 发放的独特产品...products                         | EcoResReleasedDistinctProductCommon Data ServiceEntity | product / 产品                                      | |
| 产品编号标识条码...msdyn_productbarcodes                         | EcoResProductNumberIdentifiedBarcodeEntity             | msdyn_productbarcode                         | |
| 默认订单设置...msdyn_productdefaultordersettings                        | InventProductDefaultOrderSettingsEntity                | msdyn_productdefaultordersetting             | |
| 产品默认订单设置 V2...msdyn_productspecificdefaultordersettings     | InventProductSpecificOrderSettingsV2Entity             | msdyn_productspecificdefaultordersetting     | |
| 产品特定的单位转换...msdyn_productspecificunitofmeasureconversions | EcoResProductSpecificUnitConversionEntity              | msdyn_productspecificunitofmeasureconversion | |
| 站点...msdyn_operationalsites                                                    | InventOperationalSiteEntity                            | msdyn_operationalsite                        | |
| 仓库...msdyn_warehouses                                                     | InventWarehouseEntity                                  | msdyn_warehouse                              | 请参见[注释 1](#scm-notes)。 |
| 基础产品颜色...msdyn_sharedproductcolors                                 | EcoResProductMasterColorEntity                         | msdyn_sharedproductcolor                     | |
| 基础产品大小...msdyn_sharedproductsizes                                   | EcoResProductMasterSizeEntity                          | msdyn_sharedproductsize                      | |
| 基础产品样式...msdyn_sharedproductstyles                                 | EcoResProductMasterStyleEntity                         | msdyn_sharedproductstyle                     | |
| 基础产品配置...msdyn_sharedproductconfigurations                 | EcoResProductMasterConfigurationEntity                 | msdyn_sharedproductconfiguration             | |
| 产品类别...msdyn_productcategories                                      | EcoResProductCategoryEntity                            | msdyn_productcategory                        | 请参见[注释 2](#scm-notes)。 |
| 产品类别分配...msdyn_productcategoryassignments                   | EcoResProductCategoryAssignmentEntity                  | msdyn_productcategoryassignment              | |
| 产品类别层次结构...msdyn_productcategoryhierarchies                   | EcoResProductCategoryHierarchyEntity                   | msdyn_productcategoryhierarchy               | |
| 产品类别层次结构角色...msdyn_productcategoryhierarchyroles            | EcoResProductCategoryHierarchyRoleEntity               | msdyn_productcategoryhierarchyrole           | |
| 库存通道...msdyn_warehouseaisles                                           | WMSWarehouseAisleEntity                                | msdyn_warehouseaisle                         | |
| 仓库区域...msdyn_warehousezones                                            | WHSWarehouseZoneEntity                                 | msdyn_warehousezone                          | |
| 仓库区域组...msdyn_warehousezonegroups                                 | WHSWarehouseZoneGroupEntity                            | msdyn_warehousezonegroup                     | |
| 仓库库位...msdyn_inventorylocations                                    | WMSWarehouseLocationEntity                             | msdyn_inventorylocation                      | 请参见[注释 3](#scm-notes)。 |
| 仓库工作标题...msdyn_warehouseworkheaders                               | WHSWarehouseWorkHeaderEntity                           | msdyn_warehouseworkheader                    | |
| 仓库工作行...msdyn_warehouseworklines                                    | WHSWarehouseWorkLineEntity                             | msdyn_warehouseworklines                     | 请参见[注释 4](#scm-notes)。 |
| 交货方式...msdyn_shipvias                                                | DlvDeliveryModeEntity                                  | msdyn_shipvias                               | |
| 交货条款...msdyn_termsofdeliveries                                       | DeliveryTermsEntity                                    | msdyn_termsofdelivery                        | |
| 销售订单来源代码...msdyn_salesorderorigins                                | SalesOrderOriginEntity                                 | msdyn_salesorderorigin                       | |
| Common Data Service 销售订单标题...salesorders                             | SalesOrderHeaderCommon Data ServiceEntity              | salesorder                                   | |
| Common Data Service 销售订单行...salesorderdetails                         | SalesOrderLineCommon Data ServiceEntity                | salesorderdetails                            | |
| Common Data Service 销售报价单标题...quotes                               | SalesQuotationHeaderCommon Data ServiceEntity          | quote / 报价                                        | |
| Common Data Service 销售报价单行...quotedetails                          | SalesQuotationLineCommon Data ServiceEntity            | QuoteDetails                                 | |
| 销售发票抬头 V2...invoices                                               | SalesInvoiceHeaderV2Entity                             | invoice / 发票                                      | |
| 销售发票行 V2...invoicedetails                                           | SalesInvoiceLineV2Entity                               | invoicedetail                                | |

### <a name="mapping-specific-notes"></a><a id='scm-notes'></a>映射特定注释

1. 由于存在自依赖关系，您可能必须运行两次初始同步。
2. 默认情况下，由于父子关系（平台不处理“智能”排序），初始同步处于关闭状态。 因此，必须以正确的顺序（先是根类别，然后是子类别，再然后是子类别的子类别）手动同步现有产品类别（例如，通过更新类别的描述）。 转到**产品信息管理 \> 设置 \> 类别和属性 \> 类别层次结构**。 在**类别层次结构**页面上，您可以选择每个层次结构并查看其中的产品类别。
3. 空 **ItemNumberInLocation** 查找字段的映射以及第一个、第二个和第三个其他仓库区域会导致初始同步失败。 因此，这些映射现在已删除。
4. 空 **CaptureWeight** 字段的映射会导致初始同步失败。 因此，此映射现在已删除。

### <a name="setup-related-information"></a>设置相关信息

+ 首次在 Dynamics 365 中的模型驱动应用内的**产品**实体中创建记录时，它们的状态为**草稿**。 要将状态更改为**活动**，在模型驱动应用中转到**设置 \> 管理 \> 系统设置 \> Sales**，然后将**创建处于活动状态的产品**选项设置为**是**。
+ 如果在启用双写入之前，在 Dynamics 365 中的模型驱动应用或 Common Data Service 中的**产品**实体中创建记录，则只有在包括**公司**在内的整个密钥与 Finance and Operations 应用中的数据匹配时，这些记录才会被更新。
+ 同步**产品**实体是单向的，从 Finance and Operations 应用到 Common Data Service。 如果 Dynamics 365 中的模型驱动应用内**产品**实体中的映射字段已更新，此更新将在下一次从 Finance and Operations 应用同步时被覆盖。

### <a name="known-issues"></a>已知问题

- 当一个单位在 Finance and Operations 应用中被删除时发生错误。 当度量单位从 Finance and Operations 应用同步到 Common Data Service 时，特定类的第一个单位将创建为主单位，并禁止删除。

    **缓解方法：** 首先在 Common Data Service 中删除该单位。 然后可以在 Finance and Operations 应用中将其删除。

- 当一个运营站点在 Common Data Service 中被删除时发生错误。 错误消息显示：“信息日志：警告：无法删除主要地址。警告：无法删除实体记录，因为对以下数据源的验证失败：InventSiteLogisticsLocation (InventSiteLogisticsLocation)。” 此错误是由 Finance and Operations 应用中数据实体中的问题引起的。

    **缓解方法：** 您可以在 Finance and Operations 应用中删除该站点。 如果对应的双写入映射正在运行，该站点将被在 Common Data Service 中删除。

## <a name="dynamics-365-finance-entities"></a>Dynamics 365 Finance 实体

Dynamics 365 Finance 的以下实体将按其应该启用的顺序列出。

| 双写入页面上的映射名称 | Finance 中的实体元数据名称 | Common Data Service 中的实体元数据名称 | 说明 |
|---|---|---|---|
| 币种...transactioncurrencies                                            | CurrencyEntity                              | 货币                                   | |
| 汇率类型...msdyn_exchangeratetypes                                  | ExchangeRateTypeEntity                      | msdyn_exchangeratetype                     | |
| 汇率币种对...msdyn_currencyexchangeratepairs                 | ExchangeRateCurrencyPairEntity              | msdyn_currencyexchangeratepair             | |
| Common Data Service 汇率...msdyn_currencyexchangerates              | ExchangeRateCommon Data ServiceEntity       | msdyn_currencyexchangerate                 | 请参见[注释 1](#fin-notes)。 |
| 会计日历集成实体...msdyn_fiscalcalendars                    | FiscalCalendarEntity                        | msdyn_fiscalcalendar                       | |
| 会计日历年度集成实体...msdyn_fiscalcalendaryears           | FiscalCalendarYearEntity                    | msdyn_fiscalcalendaryear                   | |
| 会计日历期间...msdyn_fiscalcalendarperiods                          | FiscalPeriodEntity                          | msdyn_fiscalcalendarperiod                 | |
| 组织层次结构类型...msdyn_internalorganizationhierarchytypes        | OMOrganizationHierarchyTypeEntity           | msdyn_internalorganizationhierarchytype    | 请参见[注释 1](#fin-notes)。 |
| 组织层次结构目的...msdyn_internalorganizationhierarchypurposes | OMOrganizationHierarchyPurposeEntity        | msdyn_internalorganizationhierarchypurpose | 请参见[注释 1](#fin-notes)。 |
| 法人...msdyn_internalorganizations                                  | OMLegalEntity                               | msdyn_internalorganization                 | 请参见[注释 1](#fin-notes)。 |
| 法人...cdm_companies                                                | OMLegalEntity                               | cdm_company                                | |
| 运营单位...msdyn_internalorganizations                                  | OMOperatingUnitEntity                       | msdyn_internalorganization                 | 请参见[注释 1](#fin-notes)。 |
| 发布的组织层次结构...msdyn_internalorganizationhierarchies    | OMOrganizationHierarchyPublishedEntity      | msdyn_internalorganizationhierarchy        | 请参见[注释 1](#fin-notes)。 |
| 名称词缀...msdyn_nameaffixes                                              | DirNameAffixEntity                          | msdyn_nameaffix                            | |
| 付款日 Common Data Service...msdyn_paymentdays                          | PaymentDayCommon Data ServiceEntity         | msdyn_paymentday                           | |
| 付款日行 Common Data Service V2...msdyn_paymentdaylines              | PaymentDayLineCommon Data ServiceV2Entity   | msdyn_paymentdayline                       | |
| 付款计划...msdyn_paymentschedules                                     | PaymentScheduleEntity                       | msdyn_paymentschedule                      | |
| 付款计划行...msdyn_paymentschedulelines                           | PaymentScheduleLineEntity                   | msdyn_paymentscheduleline                  | |
| 付款期限...msdyn_paymentterms                                         | PaymentTermEntity                           | msdyn_paymentterm                          | |
| 客户付款方式...msdyn_customerpaymentmethods                        | CustomerPaymentMethodEntity                 | msdyn_customerpaymentmethod                | |
| 供应商付款方式...msdyn_vendorpaymentmethods                            | VendorPaymentMethodEntity                   | msdyn_vendorpaymentmethod                  | |
| 客户组...msdyn_customergroups                                        | CustCustomerGroupEntity                     | msdyn_customergroup                        | |
| 供应商组...msdyn_vendorgroups                                            | VendVendorGroupEntity                       | msdyn_vendorgroup                          | |
| 销售税组...msdyn_taxgroups                                            | TaxGroupEntity                              | msdyn_taxgroup                             | |
| 物料销售税组...msdyn_taxitemgroups                                   | TaxItemGroupEntity                          | msdyn_taxitemgroup                         | |
| 销售税分类账过账组 V2...msdyn_taxpostinggroups                   | TaxPostingGroupEntityV2                     | msdyn_taxpostinggroup                      | |
| 销售税免税代码实体 Common Data Service...msdyn_taxexemptcodes       | TaxExemptCodeCommon Data ServiceEntity      | msdyn_taxexemptcode                        | |
| 销售税主管机构...msdyn_taxauthorities                                  | TaxAuthorityEntity                          | msdyn_taxauthority                         | |
| 销售税代码...msdyn_taxcodes                                               | TaxCodeEntity                               | msdyn_taxcode                              | 请参见[注释 1](#fin-notes)。 |
| 财务维度格式...msdyn_financialdimensionformats                  | DimensionIntegrationFormatEntity            | msdyn_financialdimensionformat             | |
| 财务维度...msdyn_dimensionattributes                              | DimensionAttributeEntity                    | msdyn_dimensionattribute                   | |
| 预缴税金组...msdyn_withholdingtaxgroups                           | TaxWithholdingGroupEntity                   | msdyn_withholdingtaxgroup                  | |
| 预缴税金代码...msdyn_withholdingtaxcodes                             | TaxWithholdingTaxCodes                      | msdyn_withholdingtaxcode                   | |
| 会计科目表...msdyn_chartofaccountses                                   | LedgerChartOfAccountsEntity                 | msdyn_chartofaccounts                      | |
| 分类账...msdyn_ledgers                                                        | LedgerEntity                                | msdyn_ledger                               | 请参见[注释 1](#fin-notes)。 |
| 主科目类别...msdyn_mainaccountcategories                         | MainAccountCategoryEntity                   | msdyn_mainaccountcategory                  | |
| 主科目...msdyn_mainaccounts                                             | MainAccountEntity                           | msdyn_mainaccount                          | |
| 客户 V3...accounts                                                       | CustCustomerV3Entity                        | account / 科目                                    | 请参见[注释 2](#fin-notes)。 |
| 客户 V3...contacts                                                       | CustCustomerV3Entity                        | 联系人                                    | 请参见[注释 3](#fin-notes)。 |
| 供应商 V2...msdyn_vendors                                                    | VendVendorV2Entity                          | msdyn_vendor                               | 请参见[注释 2](#fin-notes)。 |
| Common Data Service 联系人 V2...contacts                                    | smmContactPersonCommon Data ServiceV2Entity | 联系人                                    | 请参见[注释 4](#fin-notes)。 |
| Common Data Service 联系人 V2...contacts                                    | smmContactPersonCommon Data ServiceV2Entity | 联系人                                    | 请参见[注释 5](#fin-notes)。 |

### <a name="mapping-specific-notes"></a><a id='fin-notes'></a>映射特定注释

1. 单向同步发生于 Finance and Operations 应用到 Common Data Service。
2. 由于存在自依赖关系，您可能必须运行多次初始同步。 使用 Common Data Service 中的**帐户**页面创建帐户时，请确保选择**客户**作为关系类型。 如果在初始同步期间遇到**主要联系人**字段的问题，请从映射中删除该字段，然后再次运行初始同步。 成功完成初始同步后，停止映射，然后再次向其添加**主要联系人**字段。 然后开始映射，但跳过初始同步。 **主要联系人**字段的值不会包含在初始同步中，您必须手动迁移这些值。
3. 当您尝试创建**个人**类型的客户时，请确保在 Common Data Service 的**联系人**页面上将**适售**选项设置为**是**。
4. 此映射在两端都有一个筛选器来链接客户联系人。 打开映射详细信息，选择 **Sales.Contact** 实体名称旁边的筛选器按钮（漏斗符号），并确保文件条件包含 **msdyn_contactforvendor eq true and msdyn_sellable eq false**。
5. 此映射在两端都有一个筛选器来链接供应商联系人。 打开映射详细信息，选择 **Sales.Contact** 实体名称旁边的筛选器按钮（漏斗符号），并确保筛选条件包含 **msdyn_contactforvendor eq true and msdyn_sellable eq false**。 

## <a name="dynamics-365-human-resources-entities"></a>Dynamics 365 Human Resources 实体

Dynamics 365 Human Resources 的以下实体将按其应该启用的顺序列出。

| 双写入页面上的映射名称 | Human Resources 中的实体元数据名称 | Common Data Service 中的实体元数据名称 | 说明 |
|---|---|---|---|
| cdm_jobfunction - 工作职能                                |                                   | cdm_jobfunction                  | |
| cdm_jobtypes - 工作类型                                      |                                   | cdm_jobtypes                     | |
| cdm_jobs - 工作                                               |                                   | cdm_jobs                         | |
| cdm_jobs - 工作详细信息                                        |                                   | cdm_jobs                         | |
| cdm_positiontype - 职位类型                               | HcmPositionTypeEntity             | cdm_positiontype                 | |
| cdm_jobpositions - 基本职位                              | HcmPositionBaseEntity             | cdm_jobposition                  | 请参见[注释 1](#hr-notes)。 |
| cdm_jobposition - 职位详细信息                            | HcmPositionDetailEntity           | cdm_jobposition                  | 请参见[注释 1](#hr-notes)。 |
| cdm_jobposition - 职位持续时间                           | HcmPositionDurationEntity         | cdm_jobposition                  | 请参见[注释 1](#hr-notes)。 |
| cdm_jobposition - 职位层次结构                        | HcmPositionHierarchyEntity        | cdm_jobposition                  | 请参见[注释 1](#hr-notes)。 |
| cdm_veteranstatus - 退伍军人身份                            |                                   | cdm_veteranstatus                | |
| cdm_ethnicorigin - 所属种族                              |                                   | cdm_ethnicorigin                 | |
| cdm_languagecode - 语言代码                              |                                   | cdm_languagecode                 | |
| cdm_worker - 工作人员                                           | HcmWorkerEntity                   | cdm_worker                       | |
| cdm_employments - 雇用                                 |                                   | cdm_employments                  | |
| cdm_employments - 雇用详细信息                           |                                   | cdm_employments                  | |
| cdm_positionworkerassignmentmaps - 职位工作人员分配 | HcmPositionWorkerAssignmentEntity | cdm_positionworkerassignmentmaps | 请参见[注释 2](#hr-notes)。|

### <a name="mapping-specific-notes"></a><a id='hr-notes'></a>映射特定注释

1. 一个 Common Data Service 实体将映射到若干 Finance and Operations 应用实体。
2. 此映射具有自引用。

## <a name="asset-management-entities"></a>资产管理实体

Dynamics 365 Supply Chain Management 的资产管理的以下实体将按其应该启用的顺序列出。

| 双写入页面上的映射名称 | 资产管理中的实体元数据名称 | Common Data Service 中的实体元数据名称 | 说明 |
|---|---|---|---|
| FO.AssetManagementAssetLifecycleStates--Common Data Service.msdyn_assetlifecyclestates                           | 资产管理资产生命周期状态               | msdyn_assetlifecyclestates               | |
| FO.AssetManagementAssetLifecycleModels--Common Data Service.msdyn_assetlifecyclemodels                           | 资产管理资产生命周期模型               | msdyn_assetlifecyclemodels               | |
| FO.AssetManagementFunctionalLocationLifecycleModels--Common Data Service.msdyn_functionallocationlifecyclemodels | 资产管理功能位置生命周期模型 | msdyn_functionallocationlifecyclemodels  | |
| FO.AssetManagementFunctionalLocationLifecycleStates--Common Data Service.msdyn_functionallocationlifecyclestates | 资产管理功能位置生命周期状态 | msdyn_functionallocationlifecyclestates  | |
| FO.AssetManagementAssetTypes--Common Data Service.msdyn_customerassetcategories                                  | 资产管理资产类型                          | msdyn_customerassetcategories            | |
| FO.AssetManagementFunctionalLocationTypes--Common Data Service.msdyn_functionallocationtypes                     | 资产管理功能位置类型            | msdyn_functionallocationtypes            | |
| FO.AssetManagementFunctionalLocations--Common Data Service.msdyn_functionallocations                             | 资产管理功能位置                 | msdyn_functionallocations                | 请参见[注释](#am-notes)。 |
| FO.AssetManagementAssets--Common Data Service.msdyn_customerassets                                               | 资产管理资产                               | msdyn_customerassets                     | 请参见[注释](#am-notes)。 |
| FO.AssetManagementManufacturers--Common Data Service.msdyn_manufacturers                                         | 资产管理制造商                        | msdyn_manufacturers                      | |
| FO.AssetManagementModels--Common Data Service.msdyn_models                                                       | 资产管理模型                               | msdyn_models                             | |
| FO.AssetManagementWarranty--Common Data Service.msdyn_warranties                                                 | 资产管理保修                             | msdyn_warranties                         | |

### <a name="mapping-specific-notes"></a><a id='am-notes'></a>映射特定注释

- 由于存在自依赖关系，您可能必须运行多次初始同步。
