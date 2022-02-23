---
title: 从 Attract 和 Onboard 中导出数据
description: 从 Dynamics 365 Talent Attract 和 Onboard 中导出数据。
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460393"
---
# <a name="export-data-from-attract-and-onboard"></a>从 Attract 和 Onboard 中导出数据

[!include [banner](includes/banner.md)]

正如[停用 Dynamics 365 Talent: Attract 和 Dynamics 365 Talent: Onboard 应用](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)中宣布的那样，我们将在 2022 年 2 月 1 日停用 Dynamics 365 Talent: Attract 和 Dynamics 365 Talent: Onboard。 为了帮助您迁移到另一产品，这两款应用现在都提供了数据导出功能。

## <a name="export-data-from-attract"></a>从 Attract 中导出数据

您可以在环境访问权限不受限制的情况下导出数据。 出于测试目的或者是为了了解我们的数据结构，您可能需要执行此操作。 准备迁移时，请按照此过程之后的说明限制 Attract 环境的访问权限。 确保再次导出数据。 

1. 转到 [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport)。

2. 在 **数据导出** 下面，选择 **请求数据导出**。

   ![[请求从 Attract 中导出数据](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. 当出现 **正在处理您的请求** 消息框时，选择 **确定**。 数据导出最多可能需要 20 分钟，具体取决于导出的大小。

4. 导出完成后，选择旁边的 **下载** 按钮。 

   >[!NOTE]
   >所有数据导出都可以使用 7 天，到时 **下载** 链接会过期。</br>
   
下载内容包含带有 Attract 数据的 .zip 文件，其中包括以下文件夹：

| 文件夹名称 | 说明 |
| --- | --- |
| 管理员设置 | Attract 管理中心配置。 |
| 应聘者 | 已添加到工作或人才库的所有应聘者。 |
| 电子邮件模板 | 为环境配置的所有电子邮件模板。 |
| 职位聘约包模板 | 已创建的所有职位聘约包模板及其关联的配置。 |
| 职位聘约规则集 |  为管理聘约而上载的所有规则集文件。 |
| 职位聘约模板 | 为环境创建的所有职位聘约文档模板。 |
| 空缺职位 | 所有创建的职位 已删除的职位不会导出。 子文件夹包含应聘者申请，以及应聘者申请附件和聘约包的子文件夹（如果适用）。 |
| 空缺职位模板 | 在环境中配置的工作流程模板。 |
| 人才池 | 所有已创建的人才池，其要素列表以及人才池的候选人列表。 |
| 工作人员 | 环境中存在的所有工作人员及其角色的列表。 |
| （根文件夹） | 一个描述数据结构字段的 JSON 架构文件。 |

### <a name="restrict-access-to-attract"></a>限制访问 Attract

当您准备好迁移时，请限制非管理员访问您的 Attract 环境并导出数据。

>[!IMPORTANT]
>限制访问 Attract 是永久性限制，不能撤消。 如果希望非管理员用户继续访问您的环境，请跳过此步骤。

1. 转到 [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport)。

2. 要限制非管理员访问您的 Attract 环境，请在 **限制访问此应用** 下面选择 **立即限制访问**。 限制访问还会取消发布任何已发布的有效职位。

   ![[限制非管理员访问 Attract](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. 当您看到 **这是永久性更改** 警告时，选择 **限制访问** 以永久限制非管理员用户进入此环境。 如果您尚未准备好完成此步骤，请选择 **取消**。

   ![[警告限制访问是永久性更改](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   >在您限制访问 Attract 环境后，管理员可以继续访问数据导出和人员报告页面。

## <a name="export-data-from-onboard"></a>从 Onboard 中导出数据

准备就绪后，您可以从 Onboard 中下载模板、指南和应聘者数据。

1. 转到 [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport)。

2. 在 **数据导出** 下面，选择 **请求数据导出**。 

   ![[请求从 Onboard 中导出数据](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. 当出现 **正在处理您的请求** 消息框时，选择 **确定**。 数据导出最多可能需要 20 分钟，具体取决于导出的大小。

4. 导出完成后，选择旁边的 **下载** 按钮。 

   ![[从 Onboard 中下载导出数据](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   >您的数据导出可以使用 7 天。 七天后，**下载** 链接过期，如果您需要再次下载数据，则必须请求新的导出。 当您开始新的数据导出时，新导出成功后，所有现有下载都将过期。

下载是一个 .zip 文件，其中包含：

- 一个 **Templates** 文件夹，其中包含 Word 文档格式的 Onboard 模板。

- 一个 **Guides** 文件夹，其中包含 Word 文档格式的 Onboard 指南。

## <a name="see-also"></a>请参阅

[停用 Dynamics 365 Talent: Attract 和 Dynamics 365 Talent: Onboard 应用](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)