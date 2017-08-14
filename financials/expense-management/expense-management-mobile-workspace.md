---
title: "费用管理移动工作区"
description: "本主题提供有关费用报销管理移动工作区的信息。 此工作区让用户能够捕获和上载收据，以便以后可以将其附加到支出报表。 用户还可以使用附加的收据快速创建支出行，并创建和管理其支出报表。"
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.translationtype: HT
ms.sourcegitcommit: 2dd3db95eb741c37dd8a50c397cb4c9494599250
ms.openlocfilehash: 993586b1fb46c21d2b68a6060ab897c8ccc76a6c
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---

# <a name="expense-management-mobile-workspace"></a>费用报销管理移动工作区

[!include[banner](../includes/banner.md)]

本主题提供有关**费用报销管理**移动工作区的信息。 此工作区让用户能够捕获和上载收据，以便以后可以将其附加到支出报表。 用户还可以使用附加的收据快速创建支出行，并创建和管理其支出报表。 此外，审核人可以使用**费用报销管理**移动工作区查看分配给他们的支出报表，并且审核或拒绝这些支出报表。


将此工作区用于与 Microsoft Dynamics 365 for Unified Operations 移动应用一起使用。


## <a name="overview"></a>概览

很多组织要求收据副本附加到员工为获得补偿提交的差旅相关或业务相关的支出报表。 **费用管理**移动工作区让用户可以通过使用附加的收据照片在所选择的移动设备上快速创建新的支出行。 或者，用户可以捕获收据照片，然后以后再将其附加到支出报表。 员工也可以使用其移动设备创建和管理其支出报表，然后将它们提交以供审核和补偿。


具体来说，**费用报销管理**移动工作区让用户能够执行以下任务：

- 拍摄收据照片，并上载到 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本。 你以后可以将该照片附加到支出报表。
- 作为捕获的收据上载文件。 你以后可以将该文件附加到支出报表。
- 通过使用附加的收据创建新支出行。 你以后可以将该行项添加到支出报表，并提交以供审核和补偿。

如果你正在使用 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本2017 年 7 月更新，你还可以使用以下功能：

- 创建新支出报表。
- 将信用卡交易记录和其他以前创建的支出附加到支出报表。
- 为支出报表创建新的支出。
- 通过拍摄收据照片或将文件作为捕获的收据上传的方式将收据添加到支出报表的任何支出。
- 根据公司的支出政策，请将来宾列表添加到支出。
- 根据公司的支出政策，请列出支出明细。
- 提交支出报表以供审核和补偿。
- 审核或拒绝你作为对其分配的审核人的支出报表。

## <a name="prerequisites"></a>必备项
先决条件根据为你的组织部署的 Microsoft Dynamics 365 版本不同。

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a>使用 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本2017 年 7 月更新时的先决条件 
如果已经为你的组织部署 Microsoft Dynamics 365 for Finance and Operations Enterprise 版本2017 年 7 月更新，系统管理员必须发布**费用报销管理**移动工作区。 有关说明，请查阅 [发布移动工作区](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace)。

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>使用带平台更新 3 或更高版本的 Microsoft Dynamics 365 for Operations 版本 1611 时的先决条件
如果已经为您的组织部署带平台更新 3 或更高版本的 Microsoft Dynamics 365 for Operations 版本 1611，系统管理员必须完成以下先决条件。 

<table>
<thead>
<tr class="header">
<th>必备项</th>
<th>角色</th>
<th>说明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>实现 KB 4019015。</td>
<td>系统管理员</td>
<td>KB 4019015 是包含<strong>费用报销管理</strong>移动工作区的 X++ 更新或元数据修补程序。 若要实施 KB 4019015，系统管理员必须遵循这些步骤。
<ol>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">从 Microsoft Dynamics Lifecycle Services (LCS) 下载元数据修补程序</a>。</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">安装元数据修补程序</a>。</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">创建</a>包含 <strong>ApplicationSuite</strong> 和 <strong>ExpenseMobile</strong> 模型的可部署包，然后将可部署包上载到 LCS。</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">应用可部署包</a>。</li>
</ol></td>
</tr>
<tr class="even">
<td>发布<strong>费用报销管理</strong>移动工作区。</td>
<td>系统管理员</td>
<td>请查阅<a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">发布移动工作区</a>。</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>下载并安装 Dynamics 365 for Operations 移动应用
下载并安装 Dynamics 365 for Unified Operations 移动应用：

- [适用于 Android 手机](https://go.microsoft.com/fwlink/?linkid=850662)
- [适用于 iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>登录到移动应用
1. 在移动设备上启动应用程序。
2. 输入您的 Dynamics 365 URL。
4. 首次登录时，将提示您输入您的用户名和密码。 输入凭据。
5. 登录后，将显示您的公司的可用工作区。 请注意，如果您的系统管理员以后发布新工作区，您必须刷新移动工作区列表。


[![下拉以刷新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>通过使用费用管理移动工作区捕获收据

1. 在移动设备上，打开**费用报销管理**工作区。
2. 选择**捕获收据**。
3. 选择**拍照**或**选择图像**。
4. 按以下步骤之一：

    - 如果您选择了**拍照**，请执行以下步骤：

        1. 已将您带到移动设备的照相机，以便您可以拍摄收据照片。 在你完成拍照时，选择**确定**以接受照片。
        2. 可选：为照片输入一个名称，并且输入任何注释。

    - 如果你选择了**选择图像**，请执行以下步骤：

        1. 在列表中选择一个图像。
        2. 可选：为图像输入一个名称，并且输入任何注释。

5. 选择**完成**。

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>通过使用费用报销管理移动工作区快速输入费用
1. 在移动设备上，打开**费用报销管理**工作区。
2. 选择**快速输入费用**。
3. 选择支出类别。 将看到加载到您的应用程序中供脱机使用的支出类别的列表。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，开发人员应参阅 [移动平台](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform)。 如果你的类别不在该列表中，请选择**搜索**以执行在线搜索。 按支出类别搜索，或切换到按支出类型搜索。
4. 输入支出的交易记录日期。
5. 可选：输入支出商家。
6. 输入支出金额。
7. 选择支出币种。 将看到加载到您的应用程序中供脱机使用的币种代码的列表。 默认情况下加载 400 个币种，但是开发人员可以更改此数字。 有关详细信息，开发人员应参阅 [移动平台](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform)。 如果你的币种不在该列表中，请选择**搜索**以执行在线搜索。 按币种搜索，或切换到按名称搜索。
8. 选择**拍照**或**选择图像**。
9. 按以下步骤之一：

    - 如果选择了**拍照**，会将您带到移动设备的照相机，以便您可以拍摄收据照片。 在你完成拍照时，选择**确定**以接受照片。
    - 如果你选择了**选择图像**，则在列表中选择一个图像。

10. 选择**完成**。

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>使用费用报销管理工作区移动（如果使用 2017 年 7 月更新）审核支出报表
1. 在移动设备上，打开**费用报销管理**工作区。
2. **支出审核**显示分配给你进行审核的支出报表的数量。 数量约每 30 分钟更新一次。 选择**支出审核**。

    显示分配给你进行审核的支出报表的列表。
    
3. 选择支出报表以查看其支出详细信息。
4. 选择支出以查看其详细信息。 为支出显示的信息包括任何收据、来宾和明细详细信息。
5. 返回到**支出报表**页，选择审核或拒绝支出报表。
6. 为审核操作输入任何注释。
7. 选择**完成**。

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>使用费用报销管理移动工作区（如果使用 2017 年 7 月更新）创建新的支出报表并提交审核。
1. 在移动设备上，打开**费用报销管理**工作区。
2. 选择**支出条目**。
3. 选择**新报表**或选择列表中的一个现有支出报表。
4. 对于新的支出报表，输入用途和可用的任何附加信息。 此信息根据为你的公司配置费用报销管理的方式而有所不同。
5. 选择**完成**。
6. 若要将现有支出（例如信用卡交易记录）添加到支出报表，请选择**附加**。
7. 选择列表中的一个或多个支出。
8. 选择**完成**。
9. 若要将新的支出添加到支出报表，请选择**新支出**。
10. 选择支出类别。 将看到加载到您的应用程序中供脱机使用的支出类别的列表。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，开发人员应参阅 [移动平台](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform)。 如果你的类别不在该列表中，请选择**搜索**以执行在线搜索。 按支出类别搜索，或切换到按支出类型搜索。
11. 可选：输入支出商家。
12. 输入支出的交易记录日期。
13. 输入支出金额。
14. 选择支出币种。 将看到加载到您的应用程序中供脱机使用的币种代码的列表。 默认情况下加载 400 个币种，但是开发人员可以更改此数字。 有关详细信息，开发人员应参阅 [移动平台](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform)。 如果你的币种不在该列表中，请选择**搜索**以执行在线搜索。 按币种搜索，或切换到按名称搜索。
15. 选择**完成**。
16. 若要向支出添加更多详细信息，请选择**添加更多详细信息**。 可用的字段取决于为你的公司配置费用报销管理的方式。
17. 如果公司政策要求提供支出收据，请选择**收据**，然后执行以下步骤：

    1. 选择**捕获收据**或**附加收据**。
    2. 按以下步骤之一：

        - 如果你选择了**捕获收据**，请执行以下步骤：

            1. 选择**拍照**或**选择图像**。
            2. 按以下步骤之一：

                - 如果您选择了**拍照**，请执行以下步骤：

                    1. 已将您带到移动设备的照相机，以便您可以拍摄收据照片。 在你完成拍照时，选择**确定**以接受照片。
                    2. 可选：为照片输入一个名称，并且输入任何注释。

                - 如果你选择了**选择图像**，请执行以下步骤：

                    1. 在列表中选择一个图像。
                    2. 可选：为图像输入一个名称，并且输入任何注释。

            3.  选择**完成**。

        - 如果你选择了**附加收据**，请执行以下步骤：

            1.  选择列表中的一个或多个图像。
            2.  选择**完成**。

    3. 选择**返回**按钮以返回到支出详细信息。

18. 如果公司政策要求为支出提供来宾，请选择**来宾**，然后执行以下步骤：

    1. 选择**来宾**、**以前的来宾**或**同事**。
    2. 按以下步骤之一：

        - 如果你选择了**来宾**，请执行以下步骤：

            1. 输入来宾的姓名。
            2. 可选：输入来宾的组织和/或国家/地区。
            3. 可选：输入来宾的职务。
            4. 选择**完成**。

        - 如果你选择了**以前的来宾**，请执行以下步骤：

            1. 选择列表中的一个或多个以前的来宾。 你会看到你已添加到支出报表并加载到你的应用程序中供脱机使用的以前的来宾的列表。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，开发人员应参阅 [移动平台](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform)。 如果以前的来宾不在该列表中，请选择**搜索**以执行在线搜索。 按姓名搜索，或切换到按组织、国家/地区或职务搜索。
            2. 选择**完成**。

        - 如果你选择了**同事**，请执行以下步骤：

            1. 选择列表中的一个或多个同事。 你将看到加载到你的应用程序中供脱机使用的同事的列表。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，开发人员应参阅 [移动平台](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform)。 如果你的同事不在该列表中，请选择**搜索**以执行在线搜索。 按姓名搜索，或切换到按公司或职务搜索。
            2. 选择**完成**。

    3. 选择**返回**按钮以返回到支出详细信息。

19. 如果公司政策要求列出支出明细，请选择**列出明细**，然后执行以下步骤：

    1. 选择要列出明细的第一个日期。
    2. 选择**添加明细**。
    3. 选择支出明细的子类别。 你将看到加载到你的应用程序中供脱机使用的支出子类别的列表。 默认情况下，加载 50 项，但是开发人员可以更改此数字。 有关详细信息，开发人员应参阅 [移动平台](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform)。 如果你的子类别不在该列表中，请选择**搜索**以执行在线搜索。 按支出子类别名称搜索。
    4. 输入用于明细的交易记录金额。
    5. 根据需要编辑交易记录日期。
    6. 选择**完成**。
    7. 重复上面的步骤，直到你完成添加所选日期的所有明细。
    8. 对于更多天数，你可以选择**复制到下一天**以将明细复制到下一天。 或者，可以选择要列出明细的日期，然后像你为第一个日期所做的那样添加明细。
    9. 在你列出支出的明细结束后，选择**返回**按钮以返回到支出详细信息。

20. 选择**返回**按钮以返回到**支出报表**页。
21. 重复上面的步骤，直到你添加所有支出结束。
22. 选择**提交**。
23. 为审核人输入任何注释。
24. 选择**完成**。

