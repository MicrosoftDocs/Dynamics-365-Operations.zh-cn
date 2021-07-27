---
title: 配置共享参数
description: 您必须为在公司间共享的记录设置共享参数，例如职位记录。 本文说明如何设置跨法人的人力资源参数。
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7aff01bee8cadcf852ae32fd60447c68e2174a2a
ms.sourcegitcommit: 43962e6fedaf55aab2f28f53bc38a69d2ff58403
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/01/2021
ms.locfileid: "6332987"
---
# <a name="configure-shared-parameters"></a>配置共享参数

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

您必须为在公司间共享的记录设置共享参数，例如职位记录。 本文说明如何设置跨法人的人力资源参数。

某些类型的记录（如位置记录）将在公司间共享。 对于这些记录，您必须设置共享的参数。 例如，您使用 **人力资源共享参数** 页设置法人之间的人力资源参数。 

在 **人力资源共享参数** 页上，将根据区域的功能将参数分组到相应区域中。 

### <a name="settings"></a>设置
在 **标识** 选项卡上，您必须选择表示页面上列出的标识号的标识类型。 在您可以输入工作的人员的标识信息之前，必须设置标识类型。 有关社会保险号、国家/地区 ID 号、侨民 ID 号和个人 ID 代码的信息保留在 **标识类型** 页上。 要定义新的标识类型或检查现有类型的列表，请单击 **人事管理** &gt; **链接选项卡** &gt; **设置** &gt; **标识类型**。 您可以输入简单的代码和描述。 

在 **编号规则** 选项卡上，您可以选择用于以下记录的编号规则：人员编号、职位、用户请求 ID、I-9 文档、申请人、讨论、福利 ID 和人事操作（如果此记录类型已启用）。 要维护编号规则引用和代码，请使用 **编号规则** 列表页。 要查找此页，请使用页搜索功能。 

在 **职位** 选项卡上，指示新的职位在默认情况下是否可分配：

- **始终** – 创建新的职位时，可将工作人员分配到这些职位。 在创建职位时，**职位** 页的 **常规** 选项卡上的 **可进行分配的日期和时间** 将自动设置为创建日期和时间。
- **从不** – 创建新的职位时，您无法将工作人员分配到这些职位。 如果选择此选项，必须为每个新职位（当它变为可用时）打开 **职位** 页面。 然后，在 **常规** 选项卡上，输入 **可用于分配** 日期以启用工作人员分配。

在 **高级访问** 选项卡上，您可以限制对某些信息或链接的访问：

- **限制对工作人员信息的访问** – 如果用户应该可以查看仅他们有权访问的法人以及在这些法人中受雇的员工的员工信息，打开此功能。

    打开此功能后，您必须按照以下步骤为必须限制查看的每个用户设置适当的权限：

    1. 在 **用户** 页面上，选择用户。
    1. 选择用户的角色。 **分配组织** 选项变得可用。
    1. 选择 **分配组织**。
    1. 在新页面上，选择 **单独授予对特定组织的访问权限**，然后选择用户应有权访问的组织。
    1. 对于用户拥有的每个其他角色（包括系统用户角色）重复步骤 2 到 4。

    > [!NOTE]
    > 用户有权访问的公司必须跨所有用户的角色匹配。

- **启用跨公司薪酬视图** – 按雇用的每个法人分配员工的薪酬。 有时，一名员工可以同时受雇于多个法人。 打开此功能后，每个法人的薪酬将显示在员工自助服务和经理自助服务中，而无需您更改法人。 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
