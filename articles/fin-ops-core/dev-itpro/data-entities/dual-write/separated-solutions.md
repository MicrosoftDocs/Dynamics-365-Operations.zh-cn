---
title: 分隔的双重写入应用程序业务流程包
description: 双重写入应用程序业务流程包不再是单个包，而是分成了更小的包。 本主题介绍了每个包所包含的解决方案和映射及其与其他包的依赖关系。
author: RamaKrishnamoorthy
ms.date: 04/25/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: f6950ec3e6ded49a71f119c21be67f538c8e1c69
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716543"
---
# <a name="separated-dual-write-application-orchestration-package"></a>分隔的双重写入应用程序业务流程包

[!include [banner](../../includes/banner.md)]



以前，双重写入应用程序流程包是包含以下解决方案的单个包：

- Dynamics 365 说明
- Dynamics 365 Finance and Operations 公用定位点
- Dynamics 365 Finance and Operations 双写入实体映射
- Dynamics 365 资产管理应用
- Dynamics 365 资产管理
- HCM 常用
- Dynamics 365 Supply Chain Extended
- Dynamics 365 Finance Extended
- Dynamics 365 Finance and Operations 公用
- Dynamics 365 公司
- 币种汇率
- Field Service Common

由于是单个包，因此，此包为客户创建了一个“全有或全无”情况。 但是，Microsoft 现在已将其分成了更小的包。 因此，客户只能为所需解决方案选择包。 例如，如果您是 Microsoft Dynamics 365 Supply Chain Management 客户，并且不需要与 Dynamics 365 Human Resources、附注和资产管理集成，则可以从已安装的解决方案中排除这些解决方案。 由于基础解决方案名称、发布者和映射版本保持不变，因此，此更改是非破坏性的。 将升级现有安装。

![已分隔包。](media/separated-package-1.png)

本主题介绍了每个包所包含的解决方案和映射及其与其他包的依赖关系。

## <a name="dual-write-application-core"></a>双重写入应用程序核心

双重写入应用程序核心包允许用户在没有任何 Customer Engagement 应用的情况下安装和配置双重写入。 它包含以下五个解决方案。

| 唯一名称                           | 显示的名称                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Dynamics 365 公司                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finance and Operations 公用 |
| CurrencyExchangeRates                 | 币种汇率                    |
| msdyn_DualWriteAppCoreMaps            | 双重写入应用程序核心实体映射   |
| msdyn_DualWriteAppCoreAnchor          | 双重写入应用程序核心定位点        |

此包中提供以下映射。

| Finance and Operations 应用     | 客户互动应用                    |
|---------------------------------|---------------------------------------------|
| 运营单位                  | msdyn_internalorganizations                 |
| 组织层次结构          | msdyn_internalorganizationhierarchies       |
| 法人                  | msdyn_internalorganizations                 |
| 法人                  | cdm_companies                               |
| 组织层次结构目的 | msdyn_internalorganizationhierarchypurposes |
| 汇率币种对     | msdyn_currencyexchangeratepairs             |
| 名称词缀                    | msdyn_nameaffixes                           |
| 汇率类型              | msdyn_exchangeratetypes                     |
| CDS 汇率              | msdyn_currencyexchangerates                 |
| 组织层次结构类型     | msdyn_internalorganizationhierarchytypes    |
| 币种                      | transactioncurrencies                       |
| 混合现实指南实体     | msmrw_guides                                |

**依赖项信息**

双重写入应用程序核心包不依赖于其他包。

## <a name="dual-write-human-resources"></a>双重写入 Human Resources

双重写入 Human Resources 包包含同步 Human Resources 数据所需的解决方案和映射。 它包含以下三个解决方案。

| 唯一名称                | 显示的名称                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | HCM 常用                               |
| msdyn_Dynamics365HCMMaps   | Dynamics 365 Human Resources 实体映射 |
| msdyn_Dynamics365HCMAnchor | Dynamics 365 Human Resources 定位点      |

此包中提供以下映射。

| Finance and Operations 应用 | 客户互动应用         |
|-----------------------------|----------------------------------|
| 所属种族              | cdm_ethnicorigins                |
| 薪酬工作职能   | cdm_jobfunctions                 |
| 职位 V2                | cdm_jobpositions                 |
| 工作                        | cdm_jobs                         |
| 薪酬工作类型       | cdm_jobtypes                     |
| 语言代码              | cdm_languages                    |
| 职位类型               | cdm_positiontypes                |
| 职位工作人员分配 | cdm_positionworkerassignmentmaps |
| 退伍军人状态              | cdm_veteranstatuses              |
| 工作线程                      | cdm_workers                      |
| 每个公司的雇用      | cdm_employments                  |

**依赖项信息**

双重写入 Human Resources 包依赖于双重写入应用程序核心包。 因此，您应先安装双重写入应用程序核心包，然后再安装双重写入 Human Resources 包。

## <a name="dual-write-supply-chain"></a>双重写入供应链

双重写入供应链包包含同步 Supply Chain Management 数据所需的解决方案和映射。 它包含以下三个解决方案。

| 唯一名称                                | 显示的名称                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | Dynamics 365 Supply Chain Extended                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Dynamics 365 Supply Chain Management 扩展实体映射 |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Dynamics 365 Supply Chain Management 扩展定位点      |

此包中提供以下映射。

| Finance and Operations 应用                 | 客户互动应用                      |
|---------------------------------------------|-----------------------------------------------|
| 单位                                       | uoms                                          |
| CDS 销售订单标题                     | salesorders                                   |
| CDS 销售订单行                       | salesorderdetails                             |
| CDS 销售报价标题                  | 询价                                        |
| CDS 销售报价行                   | quotedetails                                  |
| CDS 发布的独特产品              | 产品                                      |
| 仓库区域                             | msdyn_warehousezones                          |
| 仓库区域组                       | msdyn_warehousezonegroups                     |
| 仓库工作行                        | msdyn_warehouseworklines                      |
| 仓库工作标题                      | msdyn_warehouseworkheaders                    |
| 仓库                                  | msdyn_warehouses                              |
| 库存通道                             | msdyn_warehouseaisles                         |
| 单位换算                            | msdyn_unitofmeasureconversions                |
| 交货条款                           | msdyn_termsofdeliveries                       |
| 交货模式                           | msdyn_shipvias                                |
| 基础产品样式                       | msdyn_sharedproductstyles                     |
| 销售发票行 V2                      | invoicedetails                                |
| 销售发票抬头 V2                    | 发票                                      |
| 基础产品大小                        | msdyn_sharedproductsizes                      |
| 已发布产品 V2                        | msdyn_sharedproductdetails                    |
| 基础产品配置               | msdyn_sharedproductconfigurations             |
| 基础产品颜色                       | msdyn_sharedproductcolors                     |
| 销售订单来源代码                    | msdyn_salesorderorigins                       |
| 物料收货标题                      | msdyn_purchaseorderreceipts                   |
| 物料收货行                        | msdyn_purchaseorderreceiptproducts            |
| 采购订单标头 V2                   | msdyn_purchaseorders                          |
| CDS 采购订单行软删除实体 | msdyn_purchaseorderproducts                   |
| CDS 采购订单行实体              | msdyn_purchaseorderproducts                   |
| 跟踪维度组                   | msdyn_producttrackingdimensiongroups          |
| 样式                                      | msdyn_productstyles                           |
| 存储维度组                    | msdyn_productstoragedimensiongroups           |
| 产品特定单位转换           | msdyn_productspecificunitofmeasureconversions |
| 产品默认订单设置 V2           | msdyn_productspecificdefaultordersettings     |
| 尺寸                                       | msdyn_productsizes                            |
| 产品维度组                    | msdyn_productdimensiongroups                  |
| 默认订单设置                      | msdyn_productdefaultordersettings             |
| 配置                              | msdyn_productconfigurations                   |
| 所有产品                                | msdyn_globalproducts                          |
| 颜色                                      | msdyn_productcolors                           |
| 产品类别层次结构角色            | msdyn_productcategoryhierarchyroles           |
| 产品类别层次结构                | msdyn_productcategoryhierarchies              |
| 产品类别分配                | msdyn_productcategoryassignments              |
| 产品类别                          | msdyn_productcategories                       |
| 仓库库位                          | msdyn_inventorylocations                      |
| CDS 库存开启                            | msdyn_inventoryonhandentries                  |
| 产品类别                          | msdyn_productcategories                       |
| CDS 库存开启                            | msdyn_inventoryonhandrequests                 |
| 产品编号标识条形码           | msdyn_productbarcodes                         |
| 会员卡                                | msdyn_loyaltycards                            |
| 会员奖励分                       | msdyn_loyaltyrewardpoints                     |
| 价格客户组                       | msdyn_pricecustomergroups                     |
| 站点                                       | msdyn_operationalsites                        |
| CDS 销售报价行                   | quotedetails                                  |
| CDS 销售订单行                       | salesorderdetails                             |

**依赖项信息**

双重写入供应链包依赖于以下三个包。 因此，您应先安装这些包，然后再安装双重写入供应链包。

- 双重写入应用程序核心包
- 双重写入 Finance 包
- 双重写入 Human Resources 包

## <a name="dual-write-finance"></a>双重写入 Finance

双重写入 Finance 包包含同步 Dynamics 365 Finance 数据所需的解决方案和映射。 它包含以下四个解决方案。

| 唯一名称                            | 显示的名称                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | Dynamics 365 Finance Extended 实体映射 |
| FieldServiceCommon                     | Field Service Common                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Dynamics 365 Finance Extended 定位点      |

此包中提供以下映射。

| Finance and Operations 应用             | 客户互动应用        |
|-----------------------------------------|---------------------------------|
| 预缴税金组                  | msdyn_withholdingtaxgroups      |
| CDS 联系人 V2（客户）              | 联系人                        |
| CDS 联系人 V2（供应商）                | 联系人                        |
| 客户 V3                            | 联系人                        |
| 预缴税金代码                   | msdyn_withholdingtaxcodes       |
| 供应商 V2                              | msdyn_vendors                   |
| 供应商付款方式                   | msdyn_vendorpaymentmethods      |
| 供应商组                           | msdyn_vendorgroups              |
| 会计帐户表                       | msdyn_chartofaccountses         |
| 销售税分类帐过帐组 V2      | msdyn_taxpostinggroups          |
| 物料销售税组                    | msdyn_taxitemgroups             |
| 销售税组                        | msdyn_taxgroups                 |
| 免税(销售税)代码实体 CDS        | msdyn_taxexemptcodes            |
| 客户组                         | msdyn_customergroups            |
| 客户付款方式                 | msdyn_customerpaymentmethods    |
| 财务维度                    | msdyn_dimensionattributes       |
| 销售税主管机构                   | msdyn_taxauthorities            |
| 财务维度格式              | msdyn_financialdimensionformats |
| 会计日历期间                  | msdyn_fiscalcalendarperiods     |
| 会计日历集成实体      | msdyn_fiscalcalendars           |
| 会计日历年度集成实体 | msdyn_fiscalcalendaryears       |
| 付款期限                        | msdyn_paymentterms              |
| 付款计划                        | msdyn_paymentschedules          |
| 付款计划行                  | msdyn_paymentschedulelines      |
| 付款日 CDS                        | msdyn_paymentdays               |
| 付款日行 CDS V2                | msdyn_paymentdaylines           |
| 主帐户                            | msdyn_mainaccounts              |
| 主帐户类别                 | msdyn_mainaccountcategories     |
| 总帐                                  | msdyn_ledgers                   |
| 客户 V3                            | 帐户                        |

**依赖项信息**

双重写入 Finance 包依赖于双重写入应用程序核心包。 因此，您应先安装双重写入应用程序核心包，然后再安装双重写入 Finance 包。

## <a name="dual-write-notes"></a>双重写入说明

双重写入注释包包含同步说明或注释数据所需的解决方案和映射。 它包含以下四个解决方案。

| 唯一名称                  | 显示的名称                   |
|------------------------------|--------------------------------|
| Dynamics365Notes             | Dynamics 365 说明             |
| Dynamics365NotesExtended     | 已扩展 Dynamics 365 说明    |
| msdyn_Dynamics365NotesMaps   | Dynamics 365 说明实体映射 |
| msdyn_Dynamics365NotesAnchor | Dynamics 365 说明定位点      |

此包中提供以下映射。

| Finance and Operations                     | Customer Engagement |
|--------------------------------------------|---------------------|
| 销售订单头文档附件    | 注释         |
| 客户附件                       | 注释         |
| 供应商单据附件                | 注释         |
| 采购订单头文档附件 | 注释         |

**依赖项信息**

双重写入说明包依赖于以下两个包。 因此，您应先安装这些包，然后再安装双重写入说明包。

- 双重写入应用程序核心包
- 双重写入 Finance 包

## <a name="dual-write-asset-management"></a>双重写入资产管理

双重写入资产管理包包含同步 Supply Chain Management 或 Dynamics 365 Field Service 中的资产数据所需的解决方案和映射。 它包含以下四个解决方案。

| 唯一名称                          | 显示的名称                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | Dynamics 365 资产管理             |
| Dynamics365AssetManagementApp        | Dynamics365 资产管理应用          |
| msdyn_DualWriteAssetManagementMaps   | Dynamics 365 资产管理实体映射 |
| msdyn_DualWriteAssetManagementAnchor | Dynamics 365 资产管理定位点      |

此包中提供以下映射。

| Finance and Operations 应用                           | 客户互动应用                |
|-------------------------------------------------------|-----------------------------------------|
| 资产管理保修                             | msdyn_warranties                        |
| 资产管理模型                               | msdyn_models                            |
| 资产管理制造商                        | msdyn_manufacturers                     |
| 资产管理功能位置类型            | msdyn_functionallocationtypes           |
| 资产管理功能位置                 | msdyn_functionallocations               |
| 资产管理功能位置生命周期状态 | msdyn_functionallocationlifecyclestates |
| 资产管理功能位置生命周期模型 | msdyn_functionallocationlifecyclemodels |
| 资产管理资产                               | msdyn_customerassets                    |
| 资产管理资产类型                          | msdyn_customerassetcategories           |
| 资产管理资产生命周期状态               | msdyn_assetlifecyclestates              |
| 资产管理资产生命周期模型               | msdyn_assetlifecyclemodels              |

**依赖项信息**

双重写入资产管理包依赖于双重写入应用程序核心包。 因此，您应先安装双重写入应用程序核心包，然后再安装双重写入资产管理包。

## <a name="packages-required-for-project-operations"></a>Project Operations 所需的包
Project Operations 依赖于以下包。 因此，您应先安装这些包，然后再安装 Project Operations。

- 双重写入应用程序核心包
- 双重写入 Finance 包
- 双重写入供应链包
- 双重写入资产管理包
- 双重写入 Human Resources 包

## <a name="dual-write-party-and-global-address-book-solutions"></a>双重写入当事方和全球通讯簿解决方案

双重写入当事方和全球通讯簿包包含同步当事方和全球通讯簿数据所需的以下解决方案和映射。 

| 唯一名称                       | 显示的名称                            |
|-----------------------------------|-----------------------------------------|
| 当事方                             | 当事方                                   |
| Dynamics365GABExtended            | Dynamics 365 GAB Extended               |
| Dynamics365GABDualWriteEntityMaps | Dynamics 365 GAB 双重写入实体映射 |
| Dynamics365GABParty_Anchor        | Dynamics 365 GAB 和当事方              |

此包中提供以下映射。

| Finance and Operations 应用 | 客户互动应用 | 
|-----------------------------|--------------------------|
| CDS 当事方 | msdyn_parties | 
| CDS 邮政地址位置 | msdyn_postaladdresscollections | 
| CDS 邮寄地址历史记录 V2 | msdyn_postaladdresses | 
| CDS 当事方邮政地址位置 | msdyn_partypostaladdresses | 
| 当事方联系人 V3 | msdyn_partyelectronicaddresses | 
| 客户 V3 | 帐户 | 
| 客户 V3 | 联系人 | 
| 供应商 V2 | msdyn_vendors | 
| 联系人职务 | msdyn_salescontactpersontitles | 
| 结束语 | msdyn_complimentaryclosings | 
| 称呼 | msdyn_salutations | 
| 决策角色 | msdyn_decisionmakingroles | 
| 雇用工作职能 | msdyn_employmentjobfunctions | 
| 忠诚度级别 | msdyn_loyaltylevels | 
| 人员特点类型 | msdyn_personalcharactertypes | 
| 联系人 V2 | msdyn_contactforparties | 
| CDS 销售报价标题 | 询价 | 
| CDS 销售订单标题 | salesorders | 
| 销售发票抬头 V2 | 发票 | 
| CDS 地址角色 | msdyn_addressroles |

**依赖项信息**

双重写入当事方和全局通讯簿解决方案依赖于以下三个包。 因此，您应先安装这些包，然后再安装双重写入当事方和全球通讯簿解决方案包。

- 双重写入应用程序核心包
- 双重写入 Finance 包
- 双重写入供应链包
