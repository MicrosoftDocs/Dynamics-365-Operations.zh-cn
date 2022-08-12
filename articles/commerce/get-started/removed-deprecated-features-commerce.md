---
title: Dynamics 365 Commerce 中已删除或弃用的功能
description: 本文介绍 Dynamics 365 Commerce 中已经删除或计划删除的功能。
author: josaw
ms.date: 07/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: a59d62ad846eed659fa4e70390ebafc40127df0f
ms.sourcegitcommit: ef56b5d0ed26e373add5dec63168e08ade40573e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2022
ms.locfileid: "9138578"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Dynamics 365 Commerce 中已删除或弃用的功能

[!include [banner](../includes/banner.md)]

本文介绍 Dynamics 365 Commerce 中已经删除或计划删除的功能。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

此列表旨在帮助您在您自己的计划中考虑这些功能的移除和弃用。 

> [!NOTE]
> [技术参考报告](/dynamics/s-e/)中提供了有关财务和运营应用中的对象的详细信息。 可比较这些报告的不同版本，以了解财务和运营应用各版本中已更改或已删除的对象。

## <a name="feature-deprecation-effective-july-2022"></a>功能弃用从 2022 年 7 月开始生效

### <a name="commerce-analytics-preview"></a>Commerce 分析（预览版）

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 该 Dynamics 365 Commerce 团队已分析 Commernce 分析（预览版）功能的使用情况和利用情况，并决定不再继续将该功能引入正式发布。   |
| **被另一个功能取代？**   | 此时，Commerce 分析（预览版）将不会替换为其他功能或解决方案。 可以继续将原始交易和主数据从财务和运营应用导出到 Azure Data Lake，如[在财务和运营应用中导出到 Data Lake](../../fin-ops-core/dev-itpro/data-entities/finance-data-azure-data-lake.md) 中所述。 合作伙伴和客户可以利用该数据流为其业务需求创作任何预期分析报告。
| **影响的产品区域**         | Commerce 分析（预览版） |
| **部署选项**              | 所有 |
| **Status**                         | 我们将考虑在 2022 年 8 月 30 日之前禁用此功能。  从此日期开始，Commerce 分析（预览版）提供的当前 Power BI 报表中将不会进行刷新。     |


## <a name="features-removed-or-deprecated-in-the-commerce-10025-release"></a>Commerce 10.0.25 版本中已经删除或弃用的功能

### <a name="modern-point-of-sale-mpos"></a>现代销售点 (MPOS)

现代销售点 (MPOS) 应用程序将在 Commerce 版本 10.0.25 中被弃用，取而代之的是 Store Commerce 应用。

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 店内应用是 Dynamics 365 Commerce 全渠道产品/服务的基石。 我们不断创新以提供现代和智能的商店体验，并且为了进一步实现解决方案现代化，我们将推出一系列新的变化，这些变化将显著改善 Windows 上现有店内应用程序的 IT 运营和用户体验。 新的 Store Commerce 应用程序是现有 MPOS 的技术升级。 它在 Windows 平台上提供了改进的性能、可靠性和长期支持，并且无需在每次更新时都重新打包应用。 |
| **被另一个功能取代？**   |  [Store Commerce](../dev-itpro/store-commerce.md) |
| **影响的产品区域**         | 现代销售点 |
| **部署选项**              | 所有 |
| **Status**                         | 已弃用：从 Commerce 版本 10.0.25 开始，通过 LCS 虚拟机 (VM) 提供的 MPOS 安装程序将于 2023 年 10 月被删除。 |

## <a name="features-removed-or-deprecated-in-the-commerce-10021-release"></a>Commerce 10.0.21 版本中已经删除或弃用的功能

[!include [banner](../includes/preview-banner.md)]

### <a name="overlapping-discounts-handling-setting-in-commerce-parameters"></a>叠加 Commerce 参数中的折扣处理设置

Commerce 版本 10.0.21 版中已弃用 **Commerce 参数** 页上的 **叠加折扣处理** 设置。 今后，Commerce 定价引擎将使用单个算法来确定叠加折扣的最佳组合。

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | <p>Commerce 参数中的 **叠加折扣处理** 设置控制 Commerce 定价引擎的搜索方式，并确定叠加折扣的最佳组合。 它当前提供了三个选项：<p><ul><li> **最佳性能** - 此选项使用高级启发算法和[边际值排名](../optimal-combination-overlapping-discounts.md)方法，以便及时确定最佳折扣组合的优先级并评估和确定最佳折扣组合。</li><li>**平衡计算** - 在当前代码库中，此选项就像 **最佳性能** 选项一样。 因此，它基本上是重复的选项。</li><li>**详尽计算** - 此选项使用旧算法，该算法在价格计算期间会遍历所有可能的折扣组合。 对于具有大行和大数量的订单，此选项可能会导致性能问题。</li></ul><p>为了帮助简化配置、改进性能和减少由旧算法导致的事件，我们将完全删除 **叠加折扣处理** 设置，并更新 Commerce 定价引擎的内部逻辑，以便它现在仅使用高级算法（即 **最佳性能** 选项背后的算法）。</p> |
| **被另一个功能取代？**   | 否。 我们建议使用 **平衡计算** 或 **详尽计算** 选项的组织在删除此功能之前切换到 **最佳性能** 选项。 |
| **影响的产品区域**         | 定价和折扣 |
| **部署选项**              | 全部 |
| **状态**                         | 从 10.0.21 版本开始，将在 2022 年 10 月从 Commerce 参数中删除 **叠加扣处理设置**。 |

### <a name="retail-sdk-distributed-by-using-lifecycle-services"></a>使用 Lifecycle Services 分发的 Retail SDK

Lifecycle Services (LCS) 中附带 Retail SDK。 10.0.21 版本中已弃用此分发模式。 今后，将在 GitHub 上的公共存储库中发布 Retail SDK 引用包、库和示例。

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | LCS 附带 Retail SDK。 完成 LCS 流程需要几个小时，并且每次更新都必须重复该流程。 今后，将在 GitHub 上的公共存储库中发布 Retail SDK 引用包、库和示例。 可以轻松使用扩展示例和引用包，更新将在几分钟内完成。 |
| **被另一个功能取代？**   |  [从 GitHub 和 NuGet 下载 Retail SDK 示例和引用包](../dev-itpro/retail-sdk/sdk-github.md) |
| **影响的产品区域**         | Retail SDK |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：从 10.0.21 版本开始，通过 LCS VM 提供的 SDK 将于 2023 年 10 月被删除。 |

### <a name="retail-deployable-package-and-combined-pos-hardware-station-and-cloud-scale-unit-installers"></a>Retail 可部署包和组合 POS、硬件工作站和 Cloud Scale Unit 安装程序

10.0.21 中弃用了使用 Retail SDK MSBuild 生成的 Retail 可部署包。 今后，请使用 Cloud Scale Unit (CSU) 包进行 Cloud Scale Unit 扩展（Commerce Runtime、渠道数据库、无头商业 API、付款和云销售点 (POS)）。 请对自托管的 POS、硬件工作站和 Cloud Scale Unit 使用纯扩展安装程序。

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | Retail 可部署包是包含一组完整的扩展包和安装程序的组合包。 此组合包使部署变得复杂，因为 CSU 扩展将转到 Cloud Scale Unit，而安装程序部署在商店中。 安装程序包括扩展和基础产品，这使更新变得困难。 每次升级后，都需要进行代码合并和包生成。 为了简化此流程，扩展包现在被分隔到组件中，以便轻松部署和管理。 使用新方法，扩展和基础产品安装程序会被分隔，并且可以在不进行代码合并或重新包装的情况下独立维护和升级。|
| **被另一个功能取代？**   | CSU 扩展、POS 扩展安装程序、硬件工作站扩展安装程序 |
| **影响的产品区域**         | Dynamics 365 Commerce 扩展和部署 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：从 10.0.21 版开始，将在 2022 年 10 月移除对在 LCS 中部署 RetailDeployablePackage 的支持。 |

有关详细信息，请参阅：

+ [为 Commerce Cloud Scale Unit (CSU) 生成单独的包](../dev-itpro/retail-sdk/retail-sdk-packaging.md#generate-a-separate-package-for-commerce-cloud-scale-unit-csu)
+ [创建 Modern POS 扩展包](../dev-itpro/pos-extension/mpos-extension-packaging.md)
+ [将 POS 与新的硬件设备集成](../dev-itpro/hardware-device-extension.md)
+ 代码示例
    + [Cloud Scale Unit](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit)
    + [POS、CSU 和硬件工作站](https://github.com/microsoft/Dynamics365Commerce.InStore)

### <a name="modernpossln-and-cloudpossln-in-the-retail-sdk"></a>Retail SDK 中的 ModernPos.Sln 和 CloudPos.sln

10.0.21 版中已弃用了使用 ModernPos.sln、CloudPos.sln、POS.Extension.csproj 和 POS 文件夹开发 POS 扩展的功能。 今后，请使用 POS 独立打包 SDK 进行 POS 扩展。

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 在早期版本的 Retail SDK 中，如果存在 POS 扩展，则需要代码合并和重新打包才能更新到最新版本的 POS。 代码合并是一个耗时的升级过程，您必须维护存储库中的完整 Retail SDK。 您还必须编译核心 POS.App 项目。 您必须使用独立打包模型仅维护您的扩展。 更新到最新版本的 POS 扩展的过程与更新项目使用的 NuGet 包版本一样简单。 可以独立部署扩展，服务会使用扩展安装程序。 可单独部署和维护基础 POS，并且不需要与基础安装程序或代码进行代码合并或重新打包。 |
| **被另一个功能取代？**   | [POS 独立打包 SDK](../dev-itpro/pos-extension/pos-extension-getting-started.md) |
| **影响的产品区域**         | Dynamics 365 Commerce POS 扩展和部署 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：从 10.0.21 版开始，将在 2023 年 10 月移除 Retail SDK 中对使用 ModernPos.Sln、CloudPOs.sln 和 POS.Extensons.csproj 的组合 POS 包和扩展模型的支持。 |

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Commerce 10.0.17 版本中已经删除或弃用的功能

### <a name="full-dataset-generation-interval-is-deprecated"></a>完整数据集生成间隔已弃用

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 从此版本开始，在 Dynamics 365 总部的 **商业调度参数** 窗体中，**完整数据集生成间隔(天)** 字段将弃用。 同样从此版本开始，该字段将从视觉上删除，以使值无法编辑。 值将保留为 **0**。 |
| **被另一个功能取代？**   | 否 |
| **影响的产品区域**         | Dynamics 365 Commerce |
| **部署选项**              | 所有|
| **状态**                         | 已弃用。 不要使用此字段或更改其中的值。|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Commerce 10.0.15 版本中已经删除或弃用的功能

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 的 Internet Explorer 11 支持已弃用

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 从 2020 年 12 月开始，所有 Dynamics 365 产品的 Microsoft Internet Explorer 11 支持已弃用，2021 年 8 月之后，将不再支持 Internet Explorer 11。<br><br>这将影响所用 Dynamics 365 产品设计为通过 Internet Explorer 11 界面使用的客户。 2021 年 8 月之后，此类 Dynamics 365 产品将不支持 Internet Explorer 11。 |
| **被另一个功能取代？**   | 我们建议客户转换到 Microsoft Edge。|
| **影响的产品区域**         | 所有 Dynamics 365 产品 |
| **部署选项**              | 全部|
| **状态**                         | 已弃用。 2021 年 8 月之后将不再支持 Internet Explorer 11。|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Commerce 10.0.11 版本中已经删除或弃用的功能
### <a name="data-action-hooks"></a>数据操作挂接
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 由于性能问题，数据操作挂接功能已弃用。 |
| **被另一个功能取代？**   | 建议使用[数据操作覆盖](../e-commerce-extensibility/data-action-overrides.md)来修改数据操作层中的业务逻辑。|
| **影响的产品区域**         | 电子商务可扩展性数据操作 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：从版本 10.0.11 开始 |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Visual Studio 2015 的 Retail SDK 支持、msbuild 14.0 和 Retail SDK\参考库和工具
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | Visual Studio 2015 的 Retail SDK 支持已弃用并更新为支持 VS 2017，msbuild 15.0 以及 RetailSDK\参考文件夹中的所有参考库和商业代理生成器工具已移至 NuGet 包，以简化扩展模型和 SDK 升级流程。|
| **被另一个功能取代？**   | 我们建议您按照[将 Retail SDK 从 Visual Studio 2015 迁移至 Visual Studio 2017](../dev-itpro/retail-sdk/migrate-sdk.md) 中的信息更新系统。 |
| **影响的产品区域**         | Retail SDK 扩展 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：从版本 10.0.11 开始 |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>使用 IEdmModelExtender 和 CommerceController 的 Retail Server 扩展
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 使用 IEdmModelExtender 和 CommerceController 的 Retail Server 扩展已弃用，以提供简化的扩展模型。 新实现将仅具有控制器类，没有任何其他 IEdmModelExtender 类实现。 这同时避免了对特定 OData 版本的依赖性（如果 OData 版本已更新，可能会中断扩展。） |
| **被另一个功能取代？**   |  我们建议您通过导入 NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) 包来使用 IController 类扩展模型。 |
| **影响的产品区域**         | Retail Server 扩展 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：从版本 10.0.11 开始 |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>使用 IHardwareStationController 的 Hardware Station 扩展
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 使用 IHardwareStationController 的 Hardware Station 扩展已弃用，以提供简化的扩展模型。 新实现将仅具有 IController 类，没有任何其他类实现，以避免对核心硬件工作站库的依赖，以前的扩展需要引用多个库。） |
| **被另一个功能取代？**   | 建议通过导入 NuGet (Microsoft.Dynamics.Commerce.Hosting.Contracts) 包来使用 IController 类扩展模型。 |
| **影响的产品区域**         | Hardware Station 扩展 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：从版本 10.0.11 开始 |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Commerce 10.0.10 版本中已经删除或弃用的功能
### <a name="pos-operation-803---picking-and-receiving"></a>POS 操作 803 - 领料和接收
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 由于重新设计了新的操作，因此不建议执行领料和接收操作。 |
| **被另一个功能取代？**   | 是。 它被以下两个新的 POS 操作取代：入站操作 (804) 和出站操作 (805)。|
| **影响的产品区域**         | 销售点 (POS) 应用程序 |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：从版本 10.0.10 开始，领料和接收操作将不再接收任何新功能更新。 在将来的版本中，将仅对此操作进行重要的 bug 修复。 鼓励所有客户迁移到新的[入站操作](../pos-inbound-inventory-operation.md)和[出站操作](../pos-outbound-inventory-operation.md)，它们将继续成为我们长期产品路线图的一部分。 |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Commerce 10.0.7 版本中已经删除或弃用的功能
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce GetProductAvailabilities 和 GetAvailableInventoryNearby API
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **弃用/移除的原因** | 已创建优化的新 API，以取代 GetProductAvailabilities 和 GetAvailableInventoryNearby API。 |
| **被另一个功能取代？**   | 是：它已被 GetEstimatedAvailabilty 和 GetEstimatedProductWarehouseAvailability API 所取代。 |
| **影响的产品区域**         | 电子商务应用程序 SDK |
| **部署选项**              | 所有 |
| **状态**                         | 已弃用：从版本 10.0.7 开始，将不再对 GetProductAvailabilities 和 GetAvailableInventoryNearby 进行工程投资。 在电子商务部署中使用这些 API 的组织应转换为新的 GetEstimatedAvailabilty 和 GetEstimatedProductWarehouseAvailability API，并启用[优化的产品可用性计算功能](../calculated-inventory-retail-channels.md)。  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>之前有关已删除或已弃用功能的声明
若要了解有关早期版本中已删除或已弃用功能的详细信息，请参阅[早期版本中已删除或已弃用的功能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

