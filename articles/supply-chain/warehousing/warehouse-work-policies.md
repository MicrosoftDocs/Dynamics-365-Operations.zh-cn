---
title: 仓库工作策略
description: 仓库工作策略控制是否通过仓库流程在制造中基于工作订单类型、库存库位和产品创建仓库工作。
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 0710eac8daba7f51f6b5d1522476b812a130960d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567024"
---
# <a name="warehouse-work-policies"></a>仓库工作策略

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations 中的仓库工作策略控制是否通过仓库流程在制造中基于工作订单类型、库存库位和产品创建仓库工作。

此工作策略控制是否为生产中的仓库流程创建仓库工作。 您可以使用**工作订单类型**、**库存库位**和**产品**组合设置工作策略。 例如，产品 L0101 报告为完工入库到输出库位 001。 成品稍后将在输出库位 001 的另一个生产订单中使用。 在这种情况下，您可以设置工作策略，阻止在您将产品 L0101 报告为完工入库到输出库位 001 时创建产品储存的工作。 工作策略是可以通过以下信息描述的单个实体：

-   **工作策略名称**（工作策略的唯一标识符）
-   **工作订单类型**和**工作创建方法**
-   **库存库位**
-   **产品**

## <a name="work-order-types"></a>工作订单类型
您可以选择以下工作订单类型：

-   成品储存
-   联产品和副产品储存
-   原材料领取

**工作创建方法**字段的值为**从不**。 该值表示工作策略将阻止为选定的工作订单类型创建仓库工作。

## <a name="inventory-locations"></a>库存库位
您可以选择应用工作策略的位置。 如果工作策略没有关联任何位置，则工作策略不会应用到任何流程。 在**位置**页面，您还可以选择或取消选择特定位置的工作策略。

## <a name="products"></a>产品
您可以选择应用工作策略的产品。 您可以将工作策略应用到所有产品或所选的产品。

## <a name="example"></a>示例
在以下示例中，有两个生产订单，PRD-001 和 PRD-00*2*。 生产订单 PRD-001 具有名为**装配**的工序，此时产品 SC1 正在报告为完工入库到库位 O1。 生产订单 PRD-002 具有名为**喷涂**的工序，使用来自库位 O1 的产品 SC1。 生产订单 PRD-002 还使用来自库位 O1 的原材料 RM1。 RM1 存储在仓库库位 BULK-001，将通过原材料领料的仓库工作领取到库位 O1。 生产 PRD-002 放行时生成领料工作。 

[![仓库工作策略](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png) 

当您计划为此场景配置仓库工作策略时，您应该考虑以下信息：

-   当您报告产品 SC1 从生产订单 PRD-001 完工到库位 O1 时，不要求创建成品储存的仓库工作。 这是因为生产订单 PRD-002 的**喷涂**工序使用同一位置的 SC1。
-   为了将原材料 RM1 从仓库库位 BULK-001 移到库位 O1，要求创建原材料领料的仓库工作。

这是您基于这些注意事项可以设置的工作策略示例。


|                                       |                                       |
|---------------------------------------|---------------------------------------|
| <strong>工作策略名称</strong><br> | <strong>工作订单类型</strong><br> |
|         无储存 01     `          |     - 成品储存<br>      |
|                                       |    <strong>位置</strong><br>     |
|                                       |                 - O1                  |
|                                       |    <strong>产品</strong> <br>     |
|                                       |                 - SC1                 |

以下步骤提供了关于如何为此场景设置仓库工作策略的详细说明。 还介绍了一个示例设置，显示如何报告生产订单完工入库到非牌照控制的库位。

## <a name="set-up-a-warehouse-work-policy"></a>设置仓库工作策略
仓库流程不是始终包括仓库工作。 通过定义工作策略，您可以防止为原材料领料创建工作，并将一组产品的成品储存在特定位置。 创建此过程时使用的是 USMF 演示数据格式。 

步骤 (21)

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| 1  | 转到“仓库管理”&gt;“设置”&gt;“工作”&gt;“工作策略”。        |
| 2  | 单击“新建”。                                                                 |
| 3  | 在“工作策略名称”字段中，键入“无储存工作”。                    |
| 4  | 单击“保存”。                                                                |
| 5  | 单击“添加”。                                                                 |
| 6  | 在列表中，标记所选的行。                                        |
| 7  | 在“工作订单类型”字段中，选择“成品储存”。            |
| 8  | 单击“添加”。                                                                 |
| 9  | 在列表中，标记所选的行。                                        |
| 10. | 在“工作订单类型”字段中，选择“联产品和副产品储存”。 |
| 11. | 展开“库存库位”部分。                                    |
| 12. | 单击“添加”。                                                                 |
| 13 | 在列表中，标记所选的行。                                        |
| 14. | 在仓库列表中，输入 '51'。                                         |
| 15. | 在“位置”字段中，输入或选择 '001'。                              |
| 16. | 展开“产品”部分。                                               |
| 17. | 在“产品选择”字段中，选择“已选择”。                         |
| 18. | 单击“添加”。                                                                 |
| 19. | 在列表中，标记所选的行。                                        |
| 20. | 在“物料编号”字段中，输入或选择 'L0101'。                         |
| 21. | 单击“保存”。                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>报告生产订单完工入库到非牌照控制的库位
此过程显示报告为完工入库到非牌照控制的位置的示例。 一个适用的工作策略是此任务的先决条件。 上一个过程显示工作策略的设置。 

步骤 (25)

<table>
<tbody>
<tr>
<td colspan="3"><strong>子任务：设置输出库位。</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>转到“组织管理”&gt;“资源”&gt;“资源组”。</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>在列表中选择资源组 &#39;5102&#39;。</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>单击“编辑”。</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>在“输出仓库”字段中，输入 &#39;51&#39;。</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>在“输出库位”字段中，输入 &#39;001&#39;。</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>库位 001 不是牌照控制的位置。 只有当库位存在适用的工作策略时，您才可以设置非牌照控制的输出位置。</td>
</tr>
<tr>
<td colspan="3"><strong>子任务：创建生产订单并报告为已完工入库。</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>关闭该页面。</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>转到“生产控制”&gt;“生产订单”&gt;“全部生产订单”。</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>单击“新建生产订单”。</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>在“物料编号”字段中输入 &#39;L0101&#39;。</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>单击“创建”。</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>在操作窗格上单击“生产订单”。</td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td>单击“估计”。</td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td>单击“确定”。</td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td>单击“开始”。</td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td>单击“常规”选项卡。</td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td>在“自动物料清单消耗量”字段中，选择&#39;从不&#39;。</td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td>单击“确定”。</td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td>单击“完工入库”。</td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td>单击“常规”选项卡。</td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td>在“接受错误”字段中选择“是”。</td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td>单击“确定”。</td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td>在“操作窗格”中，单击“仓库”。</td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td>单击“工作详细信息”。</td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td>在生产订单报告为完工入库时，尚未为储存生成工作。 发生这种情况是因为将工作策略定义为在产品 L0101 报告为已完工入库到库位 001 时阻止生成工作。</td>
</tr>
</tbody>
</table>



