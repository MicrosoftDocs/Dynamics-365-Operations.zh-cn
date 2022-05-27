---
title: 福利报表
description: 福利报表报告解释了员工当前注册的福利。
author: twheeloc
ms.date: 09/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a12649cd0604fb6acd58420fdafb5b560fcc10cf
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688223"
---
# <a name="benefit-statement"></a>福利报表


[!INCLUDE [PEAP](../includes/peap-2.md)]

**福利报表** 报告提供员工目前参加的福利报表。 该报告可由员工直接访问，也可由福利管理员访问。 **福利报表** 提供员工已登记的福利、保险选项、费用以及任何已登记的家属或受益人的清单。 可以为单个工作人员或多个工作人员打印此报表。

> [!NOTE]
在 **功能管理** 工作区中，必须启用 **福利报表** 功能。 要执行此操作，必须在功能管理中启用 **福利管理** 功能。 


## <a name="importing-the-benefit-statement"></a>导入福利报表 

您必须先使用报告配置导入 **福利报表**，然后才能使用 **福利报表**。 为此，请完成以下步骤：

1.  转到 **系统管理** 工作区。

2.  选择 **电子报告** 磁贴。

3.  转到 **配置提供程序** 并选择 **存储库**。

  ![存储库选择。](https://user-images.githubusercontent.com/26801678/134203290-7faf7245-ed08-44e9-95a1-a7ba278c42c6.png)

4.  从列表中选择 **HR 资源**，然后选择 **打开**。

    ![配置存储库。](https://user-images.githubusercontent.com/26801678/134203619-b3fd087d-1fe9-45ef-a588-1afedfe38dfd.png)

5.  在左窗格中选择 **福利报表模型** 并展开该模型，以便显示 **福利报表格式**。

6.  选择左窗格上的 **福利报表格式**。

7.  在屏幕右侧，将有一个 **版本** 快速选项卡。 选择 **导入**。

    ![“版本”快速选项卡。](https://user-images.githubusercontent.com/26801678/134203763-f12ef549-e326-400d-ac69-b25fc94af47b.png)

## <a name="generate-the-benefit-statement-as-a-pdf-file"></a>以 PDF 文件形式生成福利报表

默认情况下，**福利报表** 将打印为 Microsoft Word 文档。 若要以 PDF 格式打印，您将需要在 **电子报告目标** 中配置 PDF 选项。 

1. 要执行此操作，请转到 **系统管理工作区** > **电子报告** > **相关链接** > **电子报告目标**。

1.  选择 **新建**。

2.  在 **引用** 字段中，选择 **福利报表格式**。

3.  在 **文件目标** 快速选项卡上，选择 **新建**。

4.  在 **名称** 字段中，输入 **福利报表 PDF**。

5.  在 **文件组件名称** 字段中，选择 **福利报表**。

6.  选中 **转换为 PDF** 复选框。

7.  从菜单项中选择 **设置**。 

    ![文件目标。](https://user-images.githubusercontent.com/26801678/134203881-a3f1ebc3-d816-485d-a53b-026cc29cae64.png)

8.  选择 **文件** 快速选项卡，然后选择 **已启用**。

9.  选择 **确定**。
   
> [!NOTE]
> 福利管理功能处于预览状态。 在 **电子报告目标** 报表中使用电子邮件目标设置时出现已知问题。 您可能会收到错误消息，并且电子邮件将无法发送。

可从以下页面生成 **福利报表**：

-   **福利管理工作区** > **链接** > **报告** > **福利报表**

-   **员工（旧窗体）** > **个人信息选项卡** > **福利报表**

-   **简化的员工条目** > **福利报表** > **福利报表**

-   **员工自助服务** > **福利** > **查看福利报表**

> [!NOTE]
>  对 **员工自助服务** 中的 **福利报表** 的访问权限由 **查看福利报表** 特权控制。 这属于 **员工自助服务福利** 责任。 默认情况下，会向员工授予此特权。

## <a name="report-contents"></a>报表内容

**福利报表** 将打印员工确认的计划选择，包括任何放弃的计划。 下图显示此报表的示例。 

![福利报表报告。](https://user-images.githubusercontent.com/26801678/134204058-61baa318-fede-4795-a256-acdf3217f9f9.png)

报表将显示 **计划**、**覆盖范围选项**、**员工成本** 和 **雇主成本**。 此报表还将列出任何投保依赖方。 如果计划具有与其关联的受益人，则将显示受益人及其分配优先级和百分比。

可以使用 **福利报表** 页面上的 **要包括的记录** 快速选项卡同时为多个员工打印 **福利报表** 报告。
