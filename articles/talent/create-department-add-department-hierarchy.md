---
title: 创建部门并将其添加到部门层次结构中
description: 部门是一个运营单位，表示组织的类别或功能区域。 部门负责组织的特定区域，例如，销售、会计或人力资源。 您可以在功能区中使用要上报的部门。 部门可能具有损益职责。
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 207b8c78c203cef4524eb2047e7680e57f2a109c
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898425"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a>创建部门并将其添加到部门层次结构中

部门是一个运营单位，表示组织的类别或功能区域。 部门负责组织的特定区域，例如，销售、会计或人力资源。 您可以在功能区中使用要上报的部门。 部门可能具有损益职责。

部门还可能包括成本中心组。 可以向部门分配位置。 要创建部门，请单击**人力资源** &gt; **部门** &gt; **部门**。 下表说明可用的字段。

| 字段               | 描述                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 姓名                | 输入部门名称。                                                                                                                                                                                  |
| 部门编号   | 如果向**编号规则**页上的**组织编号**引用分配编号规则代码，则可能会自动生成默认值。                                                 |
| 搜索名称         | 输入可用于搜索部门的名称或缩写。                                                                                                                                            |
| 备忘录                | 在此处输入任何附加信息。                                                                                                                                                                            |
| 在层次结构中        | 选中的复选框表示部门已包含在部门层次结构中。 有关如何将部门添加到部门层次结构的信息，请参阅本文中后面的信息。 |
| DUNS 编号         | DUNS 代表数据统一编码系统。 这是由 Dun & Bradstreet 发布的 9 位数编号。                                                                                                     |
| 经理             | 输入管理部门的人员。                                                                                                                                                                    |
| 地址           | 添加部门的地址信息。 例如，添加部门所在的建筑物邮寄地址。                                                                          |
| 联系人信息 | 添加部门的联系人信息。 例如，添加部门服务台的电话号码。                                                                                           |

要将部门添加到部门层次结构，请执行以下步骤。

1.  单击**人力资源** &gt; **部门** &gt; **部门层次结构**。
2.  单击**编辑**，然后选择部门应在其下方的组织。
3.  单击**插入**，然后在列表中选择**部门**。
4.  在显示的部门列表中，选择要添加到层次结构的部门。
5.  保存所做的更改。 您会收到一条消息，表示已创建层次结构的草稿版本。
6.  准备好后，单击层次结构设计器中的**发布**。 您可以输入一个指示何时应发布层次结构的生效日期。 例如，要在下一个日历年的年初添加新部门，请将生效日期设置为新日历年的 1 月 1 日。 对层次结构进行的更改将在该日期生效。

## <a name="steps-for-creating-a-department"></a>部门创建步骤
请参阅[定义新部门](../fin-and-ops/hr/tasks/define-new-departments.md)主题了解创建新部门的分步过程。 
