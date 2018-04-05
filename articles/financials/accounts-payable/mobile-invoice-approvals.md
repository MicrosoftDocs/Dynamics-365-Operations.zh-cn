---
title: "移动发票审核"
description: "本主题旨在通过以供应商发票的移动审核为使用案例，提供在 Dynamics 365 for Finance and Operations 中设计移动方案的方法实践。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 98e32298d1c8285437adf3df9820a71e7a0d7f6c
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="mobile-invoice-approvals"></a>移动发票审核

[!include[banner](../includes/banner.md)]


商业用户可通过 Microsoft Dynamics 365 for Finance and Operations 中的移动功能设计移动体验。 对于高级方案，开发人员还可通过此平台根据需要扩展功能。 若要了解有关移动的一些新概念，最有效的方法是设计一些新方案。 本主题旨在通过以供应商发票的移动审核为使用案例，提供移动方案的设计方法实践。 本主题应该可以帮助您设计这些方案的变型，还可以适用于与供应商发票无关的其他方案。

<a name="prerequisites"></a>必备项
-------------

| 必备项                                                                                            | 说明                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 移动手册预习                                                                                |[移动平台](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| Dynamics 365 for Finance and Operations                                                                             | 已安装了 Microsoft Dynamics 365 for Operations 版本 1611 和 Microsoft Dynamics for Operations 平台更新 3（2016 年 11 月）的环境                   |
| 安装修补程序 KB 3204341。                                                                              | 任务录制器可能错误地为 Dynamics 365 for Operation 平台更新 3（2016 年 11 月更新）中的下拉对话框录制两个关闭命令。 |
| 安装修补程序 KB 3207800。                                                                              | 此修补程序允许在 Dynamics 365 for Operation 平台更新 3（2016 年 11 月更新）中的移动客户端上查看附件。           |
| 安装修补程序 KB 3208224。                                                                              | Microsoft Dynamics AX 应用程序 7.0.1（2016 年 5 月）中的移动供应商发票审核应用程序的应用程序代码。                          |
| 为 Finance and Operations 安装了此移动应用程序的 Android、iOS 或 Windows 设备 | 在相应的应用程序商城中搜索该应用程序。                                                                                                                     |

## <a name="introduction"></a>简介
供应商发票的移动审核需要“必备条件”部分中提到的三个修补程序。 这些修补程序不为发票审核提供工作区。 若要了解移动上下文中的工作区是什么，请阅读“必备条件”部分中提到的移动手册。 必须设计发票审核工作区。 

每个组织都以不同方式为供应商发票编排和定义自己的业务流程。 为供应商发票审核设计移动体验时，应考虑以下业务流程因素。 观点是尽量使用这些数据点优化设备上的用户体验。

-   用户希望在移动体验中看到发票抬头中的哪些字段？其顺序如何？
-   用户希望在移动体验中看到发票行中的哪些字段？其顺序如何？
-   一个发票中有多少个发票行？ 在此处应用 80-20 规则，并针对 80% 进行优化。
-   用户是否希望检查期间在移动设备上显示会计分配（发票编码）？ 如果此问题的答案为是，请注意以下问题：
    -   一个发票行有多少个会计分配（延伸价格、销售税、费用、拆分等）？ 再次应用 80-20 规则。
    -   发票的发票抬头中是否也有会计分配？ 如果有，这些会计分配在设备上是否可用？

> [!NOTE]
> 此主题不介绍如何编辑会计分配，因为此功能现在不支持移动方案。

-   用户是否要在设备上查看发票的附件？

发票审核的移动体验设计将有所不同，具体取决于这些问题的答案。 目标是优化组织中移动业务流程的用户体验。 本文的其他部分中，我们将查看两个方案变型，这两个变型基于前面问题的不同答案。 

在使用移动设计器时，通常需要确保“发布”更改，以防丢失更新。

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>为 Contoso 设计简单发票审核方案
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>方案属性</th>
<th>答卷</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>用户希望在移动体验中看到发票抬头中的哪些字段？其顺序如何？</td>
<td><ol>
<li>供应商名称</li>
<li>发票合计</li>
<li>发票帐户</li>
<li>发票编号</li>
<li>发票日期</li>
<li>发票描述</li>
<li>到期日期</li>
<li>发票币种</li>
</ol></td>
</tr>
<tr class="even">
<td>用户希望在移动体验中看到发票行中的哪些字段？其顺序如何？</td>
<td><ol>
<li>采购类别</li>
<li>数量</li>
<li>单价</li>
<li>行净额</li>
<li>1099 金额</li>
</ol></td>
</tr>
<tr class="odd">
<td>一个发票中有多少个发票行？ 在此处应用 80-20 规则，并针对 80% 进行优化。</td>
<td>1</td>
</tr>
<tr class="even">
<td>用户是否希望检查期间在移动设备上显示会计分配（发票编码）？</td>
<td>是</td>
</tr>
<tr class="odd">
<td>一个发票行有多少个会计分配（延伸价格、销售税、费用等）？ 再次应用 80-20 规则。</td>
<td>延伸价格：2，销售税：0，费用：0</td>
</tr>
<tr class="even">
<td>发票的发票抬头中是否也有会计分配？ 如果有，这些会计分配在设备上是否可用？</td>
<td>未使用</td>
</tr>
<tr class="odd">
<td>用户是否要在设备上查看发票的附件？</td>
<td>是</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>创建工作区

1.  在浏览器中，打开 Finance and Operations 并登录。
2.  登录之后，按照以下示例所示将 **&mode=mobile** 追加到 URL，然后刷新页面：https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**
3.  单击页面右上角的**设置**（齿轮）按钮，然后单击**移动应用程序**。 任务录制器显示时，移动应用程序设计器也必须显示。
4.  单击**添加**以创建新工作区。 对于此示例，请将该工作区命名为**我的审核**。
5.  输入描述。
6.  选择工作区颜色。 此工作区颜色将用于此工作区的移动体验的整体样式。
7.  为该工作区选择图标。
8.  单击**完成**。
9.  单击**发布工作区**以保存更改。

### <a name="vendor-invoices-assigned-to-me"></a>分配给我的供应商发票

应设计的第一个移动页面是为用户分配以待检查的发票列表。 若要设计此移动页面，请使用 Finance and Operations 中的 **VendMobileInvoiceAssignedToMeListPage** 页面。 完成此过程，请确保为您分配至少一个供应商发票进行检查，并且发票行有两个分配。 此设置满足该方案的要求。

1.  在 Finance and Operations URL 中，将菜单项的名称替换为 **VendMobileInvoiceAssignedToMeListPage**，以便在**应付账款**模块中打开**分配给我的待定供应商发票**列表页面的移动版本。 此页面根据系统中为您分配的发票数量显示这些发票。 若要查找特定发票，必须使用左侧的筛选器。 但是，此示例不需要特定发票。 只需要为您分配某张发票，这将允许您设计移动页面。 已专门为供应商发票的移动方案设计可用新页面。 因此，您必须使用这些页面。 此 URL 应类似以下 URL，并且输入该 URL 之后，必须显示下图中显示的页面：https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![“分配给我的待定供应商发票”页面](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  单击页面右上角的**设置**（齿轮）按钮，然后单击**移动应用程序**
3.  选择您的工作区，然后单击**编辑**
4.  单击**添加页面**创建第一个移动页面。
5.  输入名称（如**我的供应商发票**）和描述（如**分配给我检查的供应商发票**）。
6.  单击**完成**。
7.  在移动设计器中的**字段**选项卡上，单击**选择字段**。 列表页面上的列必须类似下图。 [![“分配给我的待定供应商发票”页面上的列](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  从列表页面添加必须在移动页面中向用户显示的所需列。 添加顺序为字段向最终用户显示的顺序。 只能通过重新选择所有字段才能更改字段的顺序。 根据此方案的要求，需要下面的八个字段： 但是，某些用户可能会认为八个字段在移动设备上提供的信息太多。 因此，我们将在移动列表视图中仅显示最重要的字段。 其余字段将在我们以后将设计的详细信息视图中显示。 现在我们将仅添加以下字段。 单击这些列中的加号 (**+**) 添加到移动页面。
    - 供应商名称
    - 发票合计
    - 发票帐户
    - 发票编号
    - 发票日期

    添加字段之后，移动页面必须类似下图。 
    [![添加字段后的页面](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  还必须立即添加以下列，以便在以后启用工作流操作。
    - 显示已完成任务
    - 显示委托任务
    - 显示撤消任务
    - 显示拒绝任务
    - 显示请求完成任务
    - 显示重新提交任务

10. 单击**完成**退出编辑模式。
11. 单击**后退**，然后单击**完成**退出工作区
12. 单击**发布工作区**以保存工作。
13. 在“应付账款参数”窗体中的**发票**下，启用**在待定供应商发票列表中显示发票总计**。 请注意，只有通过启用此参数，才能计算发票总计并在待定供应商发票列表页面中显示。 这是必备修补程序 3208224 中的一项新功能。

### <a name="vendor-invoice-details"></a>供应商发票明细

若要为移动设计发票明细页面，请使用 Finance and Operations 中的 **VendMobileInvoiceHeaderDetails** 页面。 请注意，此页面根据您在系统中的发票数量，显示时间最久的发票（即最先创建的发票）。 若要查找特定发票，必须使用左侧的筛选器。 但是，此示例不需要特定发票。 我们仅需要一些发票数据，以便设计移动页面。 [![工作流页面](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1.  在 Finance and Operations URL 中，将菜单项的名称替换为 **VendMobileInvoiceHeaderDetails** 以打开窗体
2.  通过**设置**（齿轮）按钮打开移动设计器。
3.  单击**编辑**按钮在工作区中启动编辑模式。
4.  选择前面创建的 **我的供应商发票** 页面，然后单击**编辑**。
5.  在**字段**选项卡上，单击**窗格**列标题。
6.  单击**属性** &gt; **添加页面**。 **注释：**单击**窗格**标题并添加页面时，将自动建立与明细页面之间的关系。
7.  输入页面标题（如**发票明细**）和描述（如**查看发票抬头和行明细**）。
8.  单击**选择字段**。 请注意，添加顺序为字段向最终用户显示的顺序。 只能通过重新选择所有字段才能更改字段的顺序。 
9.  根据此方案的要求，从抬头添加以下字段：
    - 供应商名称
    - 发票合计
    - 发票帐户
    - 发票编号
    - 发票日期
    - 发票描述
    - 到期日期
    - 发票币种

10. 从页面中的行窗格添加以下字段：
    - 采购类别
    - 数量
    - 单价
    - 行净额
    - 1099 金额

11. 添加了前面两步骤中的所有字段之后，单击**完成**。 此页面必须类似下图。
[![添加字段后的页面](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. 单击**完成**退出编辑模式。
13. 单击**后退**，然后单击**完成**退出工作区
14. 单击**发布工作区**以保存工作

### <a name="workflow-actions"></a>工作流操作

若要添加工作流操作，请使用 Finance and Operations 中的 **VendMobileInvoiceHeaderDetails** 页面。 若要打开此页面，请替换 URL 中的菜单项名称，如前面执行的操作。 然后通过**设置**（齿轮）按钮打开移动设计器。 执行以下步骤在明细页面上添加工作流操作。 您必须将状态为可提供您要设计的工作流操作的发票分配给您。

#### <a name="record-workflow-actions"></a>记录工作流操作
1.  单击**编辑**按钮在工作区中启动编辑模式。
2.  选择前面创建的**发票明细**页面，然后单击**编辑**。
3.  在**操作**选项卡上，单击**添加操作**。
4.  输入操作标题（如**审核**）和描述（如**审核发票**）。 请注意，此处输入的操作标题将成为移动应用程序中对用户显示的操作名称。
5.  单击**完成**。
6.  单击**选择字段**。
7.  完成 **VendMobileInvoiceHeaderDetails** 页面中的工作流流程，然后完成要录制的操作。 确保此流程中输入工作流注释，这样移动体验中也会包括注释字段。
8.  运行工作流操作后，单击**完成**完成“选择字段”任务。
9.  单击**完成**退出编辑模式。
10. 单击**后退**，然后单击**完成**退出工作区
11. 单击**发布工作区**以保存工作
12. 重复前面的步骤，记录需要的所有工作流操作。 

#### <a name="create-a-js-file"></a>创建 .js 文件
1. 打开“记事本”或 Microsoft Visual Studio，然后粘贴以下代码。 将文件保存为 .js 文件。 此代码执行以下操作：
    - 隐藏我们前面在移动列表页面中添加且与工作流有关的额外列。 我们添加这些列是为了让应用程序在上下文中有这些信息，并且可以执行下一步。
    - 它根据处于活动状态的工作流步骤应用逻辑，以便仅显示这些操作。

> [!NOTE]
> 这些页面和代码中的其他控件的名称必须与工作区中的名称相同。

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  通过选择**逻辑**选项卡，将该代码文件上传到工作区。
3.  单击**完成**退出编辑模式。
4.  单击**后退**，然后单击**完成**退出工作区
5.  单击**发布工作区**以保存工作

### <a name="vendor-invoice-attachments"></a>供应商发票附件

1.  单击页面右上角的**设置**（齿轮）按钮，然后单击**移动应用程序**
2.  单击**编辑**按钮在工作区中启动编辑模式。
3.  选择前面创建的 **发票明细** 页面，然后单击**编辑**。
4.  将**文档管理**选项设置为**是**，如下所示。 **注释：**如果需要在移动设备上显示附件，可以让此选项保留为**否**（这是默认设置）。
![文档管理](./media/docmanagement-216x300.png)
6.  单击**完成**退出编辑模式。
7.  单击**后退**，然后单击**完成**退出工作区
8.  单击**发布工作区**以保存工作

### <a name="vendor-invoice-line-distributions"></a>供应商发票行配送

此方案的要求确认将仅有行级别的分配，并且一张发票始终只有一行。 由于此方案非常简单，所以移动设备上的用户体验还必须足够简单，这样用户才不必向下滚动多次即可查看分配。 Finance and Operations 中的供应商发票包含用于显示发票抬头中的所有分配的选项。 此体验正是移动方案需要的。 因此，我们将使用 **VendMobileInvoiceAllDistributionTree** 页面设计移动方案的此部分。 

> [!NOTE] 
> 了解要求可以帮助我们在设计方案时确定要使用哪个特定页面和到底如何为用户优化移动体验。 在第二个方案中，我们将使用其他页面显示分配，因为该方案的要求不同。

1.  在 URL 中，替换 URL 中的菜单项名称，如前面执行的操作。 显示的页面应类似下图。
[![“全部分配”页面](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  通过**设置**（齿轮）按钮打开移动设计器。
3.  单击**编辑**按钮在工作区中启动编辑模式。 **注释：**您将发现自动创建了两个新页面。 系统之所以创建这些页面，是因为您在上一部分中开启了文档管理。 您可以忽略这些新页面。
4.  单击**添加页面**。
5.  输入页面标题（如**查看会计**）和描述（如**查看发票的会计**）。
6.  单击**完成**。
7.  在**字段**选项卡上，单击**选择字段**，从分配页面选择以下字段，然后单击**完成**。
    1.  本币金额
    2.  币种
    3.  会计科目

    > [!NOTE] 
    > 我们未从分配网格选择**描述**列，因为此方案的要求确认只有延伸价格才是有分配的金额。 因此，我们不需要再一个字段来确定分配针对的金额类型。 但是在下一个方案中，**将**使用此信息，因为该方案的要求指定，其他金额类型有分配（如销售税）。
8.  单击**完成**退出编辑模式。
9.  单击**后退**，然后单击**完成**退出工作区
10. 单击**发布工作区**以保存工作

> [!NOTE] 
> **查看会计**移动页面现在未链接到我们迄今为止设计的任何移动页面。 因为用户应该可以从移动设备上的**发票明细**页面导航到**查看会计**页面，所以我们必须提供从**发票明细**页面到**查看会计**页面的导航。 我们使用通过 JavaScript 的更多逻辑建立此导航。

1.  打开您在前面创建的 .js 文件，然后添加以下代码中突出显示的行。 此代码执行两项操作：
    1.  这将帮助确保用户不能直接从工作区导航到**查看会计**页面。
    2.  它建立从**发票明细**页面到**查看会计**页面的导航控件。

> [!NOTE] 
> 这些页面和代码中的其他控件的名称必须与工作区中的名称相同。

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  通过选择**逻辑**选项卡，将该代码文件上传到工作区以覆盖以前的代码
3.  单击**完成**退出编辑模式。
4.  单击**后退**，然后单击**完成**退出工作区
5.  单击**发布工作区**以保存工作

### <a name="validation"></a>验证

从您的移动设备打开应用程序，然后连接到您的 Finance and Operations 实例。 确保在供应商发票分配给您检查的位置登录公司。 您应该可以执行以下操作：

-   查看**我的审核**工作区。
-   钻取到**我的审核**工作区中，并查看**我的供应商发票**页面。
-   钻取到**我的供应商发票**页面中，并查看分配给您的发票的列表。
-   钻取到一张发票中，并查看发票抬头明细和行明细。
-   在明细页面中，查看附件的链接，并使用该链接导航到附件列表和查看附件。
-   在明细页面中，查看**查看会计**页面的链接，并使用该链接导航到分配页面和查看分配。
-   在明细页面中，单击底部的**操作**菜单，并执行适用于工作流步骤的工作流操作。

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>为 Fabrikam 设计复杂发票审核方案
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>方案属性</th>
<th>答卷</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>用户希望在移动体验中看到发票抬头中的哪些字段？其顺序如何？</td>
<td><ol>
<li>供应商名称</li>
<li>发票金额</li>
<li>发票帐户</li>
<li>发票编号</li>
<li>发票日期</li>
<li>发票描述</li>
<li>到期日期</li>
<li>发票币种</li>
</ol></td>
</tr>
<tr class="even">
<td>用户希望在移动体验中看到发票行中的哪些字段？其顺序如何？</td>
<td><ol>
<li>采购类别</li>
<li>数量</li>
<li>单价</li>
<li>行净额</li>
<li>1099 金额</li>
</ol></td>
</tr>
<tr class="odd">
<td>一个发票中有多少个发票行？ 在此处应用 80-20 规则，并针对 80% 进行优化。</td>
<td>5</td>
</tr>
<tr class="even">
<td>用户是否希望检查期间在移动设备上显示会计分配（发票编码）？</td>
<td>是</td>
</tr>
<tr class="odd">
<td>一个发票行有多少个会计分配（延伸价格、销售税、费用等）？ 再次应用 80-20 规则。</td>
<td>延伸价格：2，销售税：2，费用：2</td>
</tr>
<tr class="even">
<td>发票的发票抬头中是否也有会计分配？ 如果有，这些会计分配在设备上是否可用？</td>
<td>未使用</td>
</tr>
<tr class="odd">
<td>用户是否要在设备上查看发票的附件？</td>
<td>是</td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a>后续步骤

可根据方案 2 的要求为方案 1 完成以下变型。 您可以使用此部分提高您的移动应用体验。

1.  因为方案 2 中应该有更多行，所以对设计的以下更改将帮助优化移动设备上的用户体验：
    1.  用户可以选择查看单独移动页面上的行，而不是查看明细页面上的发票行（如方案 1 中）。
    2.  因为此方案中应该有多张发票，所以如果使用 **VendMobileInvoiceAllDistributionTree** 页面为移动设计分配页面（如方案 1 中），用户可能很难将行与分配关联。 因此，请使用 **VendMobileInvoiceLineDistributionTree** 页面设计分配页面。
    3.  理想情况下，应该在此方案中的发票行上下文内显示分配。 因此，请确保用户可以钻取到行中以查看分配页面。 请使用页面链接功能建立钻取，就如在方案 1 中对抬头和明细页面执行的操作。

2.  因为方案 2 中分配上应该有多个金额类型（销售税、费用等），所以显示金额类型的描述非常有用。 （我们在方案 1 中忽略了此信息。）





