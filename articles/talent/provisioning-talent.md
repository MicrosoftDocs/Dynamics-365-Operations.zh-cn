---
title: "配置 Microsoft Dynamics 365 for Talent"
description: "此主题将指导您如何为 Microsoft Dynamics 365 for Talent 配置新环境。"
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: Talent
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6ffb97b53f522cfe8ccd8e89df854cbc557e4f1f
ms.openlocfilehash: fadc373b2c1c06987f22d4d9c20a9ab07b0c85d5
ms.contentlocale: zh-cn
ms.lasthandoff: 11/20/2017

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>配置 Microsoft Dynamics 365 for Talent
此主题将指导您如何为 Microsoft Dynamics 365 for Talent 配置新环境。 此主题假设您已通过云解决方案提供商 (CSP) 或企业体系结构 (EA) 协议购买了 Talent。 如果您有已包括 Talent 服务计划的现有 Microsoft Dynamics 365 许可证，但无法完成本主题中的步骤，请联系支持人员。

若要开始，全局管理员应登录到 [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) 并创建新的 Talent 项目。 除非许可问题妨碍了您配置 Talent，否则不需要从支持人员或 Dynamics Service 工程 (DSE) 代表处获得帮助。

## <a name="create-an-lcs-project"></a>创建 LCS 项目
若要使用 LCS 来管理您的 Talent 环境，您必须先创建 LCS 项目。

1. 使用您用于订阅 Talent 的帐户登录到 [LCS](https://lcs.dynamics.com/Logon/Index)。
2. 选择加号 (**+**) 创建项目。
3. 选择 **Microsoft Dynamics 365 for Talent** 作为产品名称和产品版本。
4. 选择 **Dynamics 365 for Talent** 方法。
5. 选择**创建**。

有关如何开始 Talent 的信息，请参阅在新项目中创建的 **Talent** 方法。 在您完成创建项目后，请完成以下过程来设置您的 Talent 环境。

## <a name="provision-a-talent-project"></a>配置 Talent 项目
在创建 LCS 项目之后，您可以将 Talent 配置到环境中。

1. 在您的 LCS 项目中，选择 **Talent 应用管理**磁贴。
2. Talent 始终配置到 Microsoft PowerApps 环境，以支持 PowerApps 集成和可扩展性。 如果您还没有 PowerApps 环境，在继续前请先执行本主题“创建新的 PowerApps 环境（如果需要）”部分中的步骤。

    > [!NOTE]
    > 若要查看现有的环境或创建新环境，必须为配置 Talent 的租户管理员分配 PowerApps P2 许可证。 如果您的组织没有 PowerApps P2 许可证，则可以从 CSP 或从 [PowerApps 定价页面](https://powerapps.microsoft.com/en-us/pricing/)获取一个。

3. 选择**添加**，然后选择要为 Talent 配置的环境。
4. 选择**是**同意条款并开始部署。

    您的新环境将出现在左侧导航窗格的环境列表中。 不过，在部署状态更新为**已部署**前，您无法开始使用此环境。 此过程通常需要几分钟。 如果配置失败，您必须与支持人员联系。

6. 选择**登录 Talent** 来使用您的新环境。

> [!NOTE]
> 如果您尚未验证最终要求，您可以在项目中部署 Talent 的测试实例。 您可以随后使用此实例来测试您的解决方案，直到验证完成。 如果您使用新环境进行测试，那么您必须重复此过程来创建一个生产环境。

## <a name="create-a-new-powerapps-environment-if-required"></a>创建新的 PowerApps 环境（如果需要）
1. 在 LCS 中选择**管理环境**。 您会被带到 [PowerApps 管理员中心](https://preview.admin.powerapps.com/environments)，从中您可以查看现有的环境并创建新环境。
2. 选择 (**+**) **新建环境**按钮。
3. 为环境输入唯一名称，然后选择要部署的位置。

    > [!NOTE]
    > Talent 不是在所有地区都可用。 因此，在您为环境选择位置之前，请务必检查可用性。

4. 在询问您是否要创建数据库时，请选择**创建数据库**来创建必须承载Talent 数据的一部分的 Common Data Service (CDS) 数据库。 通过创建数据库，您还可以将 PowerApps 应用程序与 Talent 集成。
5. 您将被询问要用于数据库的访问级别。 我们建议您选择**限制访问**，因为此选项通过使用 PowerApps 应用程序阻止 Talent 用户直接访问敏感数据。
6. 创建的 CDS 数据库包含演示数据。 此演示数据很有用，因为您可以使用演示数据公司进行测试，或创建任务录制或任务指南。 但是，演示数据会将其他信息中的非活动员工和虚构地址添加到您的生产环境中。 若要删除演示数据，在您完成创建 CDS 数据库后执行以下步骤：

    > [!IMPORTANT]
    > 如果您以前已创建了 CDS 数据库并在其中输入了您公司的任何生产数据，请注意，以下步骤将删除所选数据库中的**所有**数据，甚至您公司的生产数据。

    1. 登录到 [PowerApps](https://preview.web.powerapps.com/home)，并转至您在步骤 2 中创建的环境。
    2. 选择**实体**。 在页面的右侧，请选择椭圆形 (**…**) 按钮，然后选择**清除所有数据**。
    3. 选择**删除数据**以确认您要删除该数据。 此操作默认情况下将删除 CDS 中包括的所有演示数据。 它还会删除在所选数据库中输入的任何其他数据。

您现在可以使用您的新环境了。

