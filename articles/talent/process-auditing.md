---
title: 跟踪招聘数据的变化
description: 流程审核功能允许您跟踪应聘者、职位空缺或工作申请何时因为报告或合规性原因改变。
author: tracykeya
manager: AnnBe
ms.date: 04/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 448fceccb507bec5b60b686043a303c1997a9ac0
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742658"
---
# <a name="track-changes-in-recruiting-data"></a>跟踪招聘数据的变化

可使用审核流程跟踪对应聘者、职位空缺或工作申请进行的更改。 这对报告或合规性原因非常有用。

可使用 OData 连接器查看 Power BI 中跟踪的数据。 有关详细信息，请参阅[在 Power BI Desktop 中连接到 OData 源](https://docs.microsoft.com/power-bi/desktop-connect-odata)。

## <a name="track-changes"></a>跟踪更改
若要设置招聘数据的跟踪更改，请执行以下步骤：

1. 在 [PowerApps](https://web.powerapps.com) 中，选择相应环境。

2. 选择**设置**（齿轮图标），选择**高级自定义**，然后选择**开发人员资源**下的**资源**。 

3. 在**开发人员资源**页中，复制**实例 Web API 值**字段中的值。 例如，该值可能如下所示：https://yourorgname.api.crm.dynamics.com/api/data/v9.1/。

4. 然后可以从下列实体之一查询数据：
  - 职位空缺历史记录 (msdyn_jobopeninghistories)
  - 工作申请历史记录 (msdyn_jobapplicationhistories) 
  - 应聘者历史记录 (msdyn_candidatehistories)

## <a name="data-reported"></a>报告的数据

以下数据可用于流程审核。

| 报告的数据 | 说明 |
| --- | --- |
| 更改者 (msdyn_ChangedbyId) | 用户引用 |
| 创建日期 (createdon) |  进行更改时的 UTC 日期和时间 |
| 更改类型 (msdyn_changetype) | 发生的更改 |
| 应聘者、职位空缺， <br></br>以及工作申请的通用值 | 创建<br></br>更新日期 |
| 工作申请历史记录 | 添加项目 <br></br>删除项目 |
| 职位空缺历史记录 | 任务：添加文章 <br></br>任务：删除文章 <br></br>任务：更新文章 <br></br>任务：添加参与者 <br></br>任务：删除参与者 |
| 应聘者历史记录 | 添加项目 <br></br>删除项目 <br></br>添加工作经验 <br></br>删除工作经验 <br></br>添加教育 <br></br>删除教育 <br></br>添加技能 <br></br>删除技能 <br></br>添加标签 <br></br>删除标签 <br></br>添加社交网络 <br></br>删除社交网络 <br></br>添加个人详细信息 <br></br>更新个人详细信息<br></br> |
| 更改的字段 (msdyn_changedfields) | JSON 对象列举更改的字段，可能不会存储所有字段的值。<br></br><br></br>对于“创建”和“更新”更改，将列出创建或修改记录的字段。<br></br><br></br>对于“添加”更改类型，将列出子记录的字段。<br></br><br></br>**示例：**<br></br><br></br>{<br></br>  “msdyn_applyurl”：{ "newValue": "" }，<br></br>  “msdyn_description”：{ "valueOmitted": true } <br></br>} |
|工作申请历史记录 | 工作申请 (msdyn_JobapplicatonId)<br></br>状态 (msdyn_status) <br></br>状态描述 (msdyn_statusreason) <br></br>拒绝原因 (msdyn_rejectionreason) |
| 职位空缺历史记录 | 职位空缺 (msdyn_JobopeningId) <br></br>状态 (msdyn_jobopeningstatus) <br></br>状态描述 (msdyn_jobopeningstatusreason) |
| 应聘者历史记录 | 应聘者 (msdyn_CandidateId) |
