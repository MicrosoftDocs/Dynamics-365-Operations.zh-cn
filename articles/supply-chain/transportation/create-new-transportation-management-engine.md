---
title: 创建新的运输管理引擎
description: 本主题介绍如何在 Dynamics 365 Supply Chain Management 中创建新的运输管理引擎。
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSGenericEngine, TMSRateEngine, TMSMileageEngine, TMSEngineParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88661b6a974e2bd60f78e38d49a08d3290008b8b
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/19/2021
ms.locfileid: "7651941"
---
# <a name="create-a-new-transportation-management-engine"></a>创建新的运输管理引擎

[!include [banner](../includes/banner.md)]

本主题介绍如何在 Dynamics 365 Supply Chain Management 中创建新的运输管理引擎。 

运输管理 (TMS) 引擎定义用于生成和处理运输管理中的运输费率的逻辑。 Supply Chain Management 提供多种不同的引擎类型，用于计算不同的参数，如费率、运输时间和运输期间将跨越的区域数。 本文介绍如何使用 Microsoft Visual Studio 开发环境以及 Supply Chain Management 开发工具创建和部署新的 TMS 引擎，以及如何在 Operations 中设置引擎。 有关引擎的详细信息，请参阅[运输管理引擎](transportation-management-engines.md)。

## <a name="create-a-new-tms-engine"></a>创建新 TMS 引擎

本节介绍如何创建具有 TMS 引擎实现的类库，以及如何从 Supply Chain Management 模型中引用它。

1. 要部署新引擎，您必须有包含引擎的模型。 在 **Dynamics 365** &gt; **模型管理** 菜单上，单击 **创建模型** 创建新模型。 在 **创建模型** 向导的第一页上，将模型命名为 **TMSEngines**。 

   [![创建模型。](./media/012.png)](./media/012.png)

2. 在下一页上，选择 **创建新包**。 

   [![创建新包。](./media/021.png)](./media/021.png)

3. 在下一页上，选择要引用的 **ApplicationSuite** 模型。 （已预选 **ApplicationPlatform** 模型。） 

   [![选择要引用的模型。](./media/032.png)](./media/032.png)

4. 在下一页上，单击 **完成** 确认新模型的创建。 

   [![完成模型创建。](./media/042.png)](./media/042.png)

5. 在新的解决方案中，创建新的 Supply Chain Management 项目，将其命名为 **TMSThirdParty**。 在项目属性中，将项目的模型设置为 **TMSEngines**。
6. 将新的 C\# 类库添加到您的解决方案中，将其命名为 **ThirdPartyTMSEngines**。
7. 在 ThirdPartyTMSEngines 项目中，添加对 Supply Chain Management 特定程序集的引用：
   -   支持引用 X++ 类型的应用程序程序集。 可在以下位置找到这些程序集。 \[Packages root\] 是放置所有已部署程序集的位置的路径，如 C:\\Packages。

        ```xpp
        [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
        [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
        [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll
        ```
        
   -   支持访问数据、LINQ 和辅助功能的框架程序集。 可在 \[Packages root\]\\bin 中找到所有这些程序集。

        ```xpp 
        Microsoft.Dynamics.ApplicationPlatform.Environment.dll
        Microsoft.Dynamics.AX.Data.Core.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
        Microsoft.Dynamics.AX.Server.Core.dll
        Microsoft.Dynamics.AX.Xpp.AxShared.dll
        Microsoft.Dynamics.AX.Xpp.Support.dll
        ```

   -   核心 TMS 程序集（包含引擎）和 TMS 基础程序集（包含帮助程序、常量、数据传输类定义等）。 可在以下位置找到这些程序集。

        ```xpp
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll
        ```
8. 将 ThirdPartyTMSEngines 项目中自动生成的 C\# 类重命名为 **SampleRatingEngine**。
9. 实现引擎。 由于我们在此示例中创建的是费率引擎，因此我们从费率引擎的基础类继承。 基础类实现大多数费率引擎接口 (**TMSFwkIRateEngine**)。 我们只需要实现费率方法。 为了让此示例保持简单，我们将使此方法注册硬编码费率 100。 您可以创建实现任何引擎接口的引擎，如 **TMSFwkIAccessorialEngine**。 所有引擎接口均在 X++ 中定义。

    ```xpp
    namespace ThirdPartyTMSEngines
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.Ax.Tms.Base.Data;
        using Microsoft.Dynamics.Ax.Tms.Base.Utility;
        using Microsoft.Dynamics.Ax.Tms.Bll;
        using System.Xml.Linq;
        public class SampleRatingEngine : BaseRateEngine
        {
            public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
            {
               XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
               re.AddRate(TmsRateType.Rate, 100);
               return this.RatingDto;
            }
        }
    }
    ```

10. 构建解决方案。
11. 添加对 TMSThirdParty 项目的新引用。 引用应指向 ThirdPartyTMSEngines 项目。 完成后，您的解决方案应看起来像这样。 

    [![解决方案，包括对 TMSThirdParty 项目的引用。](./media/052.png)](./media/052.png)

12. 构建解决方案。 验证新库是否出现在应用程序资源管理器中的 **引用** 节点中。 

    [![应用程序资源管理器的引用节点中的新库。](./media/061.png)](./media/061.png)

## <a name="deploy-the-tms-engine-as-a-package"></a>将 TMS 引擎部署为包

部署第三方 TMS 引擎的一种方法是通过部署包。 建议在生产环境中使用此方法。 在开发环境中，您可以手动复制程序集，如下一节“在 Supply Chain Management 中设置 TMS 引擎”中所述。 要将引擎部署为包，请执行以下步骤。

1. 在 **Dynamics 365** &gt; **部署** 菜单上，单击<strong>创建部署包</strong>。
2. 在 **创建部署包** 对话框中，选择 TMSEngines 模型，然后输入要存储包文件的路径。 

   [![选择 TMSEngines 模型。](./media/071.png)](./media/071.png)

3. 您现在可以将包部署到目标环境。 要查看教程，请参阅[安装可部署包](../../fin-ops-core/dev-itpro/deployment/install-deployable-package.md)。

## <a name="set-up-the-tms-engine-in-supply-chain-management"></a>在 Supply Chain Management 中设置 TMS 引擎

本节介绍如何设置 Supply Chain Management 以使用 TMS 引擎，并演示如何在费率查询中使用我们创建的新引擎。 本节中的示例使用 USMF 演示数据公司。

1. 创建新引擎，如“创建新 TMS 引擎”一节所述。
2. 构建您的解决方案。
3. 将生成的程序集复制到 Supply Chain Management 服务器的二进制位置 \[AOSWebRoot\]bin。 **注意：** 此步骤仅在开发环境中使用。 在生产环境中，您应通过部署包进行部署。 要查看说明，请参阅上一节“将 TMS 引擎部署为包”。
4. 在 Supply Chain Management 中，在 **费率引擎** 页面上，创建新的费率引擎。 此引擎应指向通过构建引擎类库和实现的引擎类生成的引擎程序集。 

   [![在“费率引擎”页面创建新的费率引擎。](./media/081.png)](./media/081.png)

5. 创建使用示例费率引擎的装运承运人。 由于我们的引擎不使用任何数据，因此您不必分配费率主数据。 

   [![创建新装运承运人。](./media/092.png)](./media/092.png)

6. 在 **费率路线工作台** 页面上，单击 **费率工场**。 您应会看到 SampleCarrier 的费率为 100.00，如下面的屏幕截图所示。 在此示例中，我们对从仓库 24 到客户 US-004 的路线进行费率查询。 但是，由于费率是硬编码的，您始终会看到费率为 100.00。

   [![费率运输路线工作台。](./media/101.png)](./media/101.png)

## <a name="tips-and-tricks"></a>提示和窍门

- 如果您正在使用 Supply Chain Management 的开发工具，向解决方案中添加新项目很有用。 如果您将此项目设置为启动项目并开始调试会话，您可以在同一调试会话中同时调试 X++ 和 C\# 代码。
- 每次更改并重新编译 ThirdPartyTMSEngines 项目时，您都必须将生成的程序集手动复制到二进制位置或通过部署包进行部署。 否则，您可能会使用过时的程序集运行。
- 在 Supply Chain Management 中执行 TMS 特定的操作后，Internet 信息服务 (IIS) 工作进程可能会锁定 ThirdPartyTMSEngines 程序集，以使程序集无法更新。 在这种情况下，应重新启动 w3svc 进程。

### <a name="whitepaper"></a>白皮书

有关详细信息，请下载以下白皮书（为支持 AX2012 编写，同样适用于 Dynamics 365 Supply Chain Management）

- [实现和部署运输管理引擎](https://download.microsoft.com/download/b/5/f/b5ff8fef-3918-4c1d-92d5-b67eb0971684/ImplementingAndDeployingTransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]