---
ms.openlocfilehash: f6bf4b6c946ebc63d3d84140f762cd4b789deb03
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458516"
---
在环境之间复制数据库时，您需要先运行环境重新配置工具才能使复制的数据库完全正常运行，从而确保所有 Commerce 组件都保持最新。

> [!IMPORTANT]
> 无论您是否使用 Commerce 组件，我们都建议您运行此过程，因为所有环境都包含 Commerce 功能。 

在继续之前，必须确保满足以下先决条件：
1. 如果要升级到 2017 年 7 月版本（也称为 7.2 版）7.2.11792.56024，请先在目标环境中应用以下应用程序 X++ 修补程序，然后再在该环境中运行数据升级。 这些操作可以预防在数据升级期间出现各种错误：

    - KB 4036156 - Retail 次要版本升级 -“未设置变型编号规则。” 此修复程序包还包括 KB 4035399 和 KB 4035751。 请注意，您必须至少拥有 Platform Update 9 才能使用此程序包。 如果您不确定，请安装最新的二进制文件。
    
2. 如果要从 Microsoft Dynamics AX 2012 升级，请先在目标环境中安装以下应用程序 X++ 修补程序，然后再运行数据升级：
    - KB 4033183 - Dynamics AX 2012 R2 或 Dynamics AX 2012 R3 Pre-CU8 非零售升级失败，dbo.RETAILTILLLAYOUTZONE 未找到对象。
    - KB 4040692 - Dynamics AX 2012 R3 至 Microsoft Dynamics 365 for Operations 7.2 升级因 SalesLineIdx 上的 RetailSalesLine 重复索引失败。
    - KB 4035490 - GeneralJournalAccountEntry MainAccount 字段升级脚本出现性能问题。


请按照以下步骤运行环境重新配置工具。

1. 在共用资产库中，选择 **软件可部署包**。
2. 下载环境重新配置工具。
3. 在项目的资产库中，选择 **软件可部署包**。
4. 选择 **新建** 以创建新程序包。
5. 为程序包输入名称和描述。 您可以使用 **环境重新配置工具** 作为程序包名称。
6. 上载之前下载的程序包。
7. 在目标环境的 **环境详情** 页面，选择 **维护** > **应用更新**。
8. 选择您之前上载的环境重新配置工具，然后选择 **应用** 以应用程序包。
9. 监控程序包部署的进度。 

有关如何应用可部署包的更多信息，请参阅[应用可部署包](../deployment/create-apply-deployable-package.md)。 有关如何手动应用可部署包的更多信息，请参阅[安装可部署包](../deployment/install-deployable-package.md)。
