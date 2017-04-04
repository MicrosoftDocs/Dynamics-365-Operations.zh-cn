---
title: "将发票审核"
description: "移动&quot;工序 365 的 Microsoft Dynamics 中允许用户业务设计移动体验。 对于高级方案，当它们平台，希望还允许开发人员扩展功能。 有效了解某些方式在移动电话的新设计理念要评议某些方案流程。 通过执行此主题供应商发票审核用于提供对设计移动方案中的实用的方法要移动电话为用例。 此主题帮助您设计方案的应其他差异，还可以应用到与其他供应商的发票方案。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 30229c0d24aed0bd927993b9af76b32d9bb073ee
ms.lasthandoff: 03/31/2017


---

# <a name="mobile-invoice-approvals"></a>将发票审核

移动"工序 365 的 Microsoft Dynamics 中允许用户业务设计移动体验。 对于高级方案，当它们平台，希望还允许开发人员扩展功能。 有效了解某些方式在移动电话的新设计理念要评议某些方案流程。 通过执行此主题供应商发票审核用于提供对设计移动方案中的实用的方法要移动电话为用例。 此主题帮助您设计方案的应其他差异，还可以应用到与其他供应商的发票方案。

<a name="prerequisites"></a>先决条件
-------------

| 必备项                                                                                            | 说明                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 先将读取的指南                                                                                |(/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform.md)                                                                                                  |
| 工序的 Dynamics 365                                                                             | 具有操作平台的更新版本的工序 3 的环境 (2016 年 11 月 Microsoft Dynamics 365 和 Microsoft Dynamics 1611)                   |
| 修补 3204341 KB 安装程序。                                                                              | 工序在该平台更新的 3 的任务录制器将不正确记录下拉对话框的结转的订单 (两年 11 月 2016) 更新 365 包括 Dynamics " |
| 修补 3207800 KB 安装程序。                                                                              | -在工序 3 的此平台更新的新的移动。启用客户将显示的关联 (年 11 月 2016) 更新 Dynamics 365 包括。           |
| 修补 3208224 KB 安装程序。                                                                              | 将供应商发票审核应用程序的应用程序代码-在 Microsoft Dynamics AX 应用程序 7.0.1 (5 月 2016 中)。                          |
| 机器人或 iOS 或具有移动应用的 Windows 设备为工序的 Dynamics 365 安装 | 应用的搜索将应用相应的商店。                                                                                                                     |

## <a name="introduction"></a>简介
供应商发票在“要求审核的移动先决条件”部分中提及的三修补程序。 修补程序为这些发票审核未提供一工作区。 若要了解哪些工作区是在将电话中，请阅读“先决条件”部分中提及的移动指南》。 必须设计发票审核工作区。 

每个组织用于协调不同方式并定义其供应商发票的业务流程。 在您设计供应商审核的发票前一移动体验，您应该考虑以下特性的业务流程。 使用思路在于尽量使用这些数据点优化设备上的用户体验。

-   用户要查看从发票抬头的哪些字段在移动体验，并且，什么顺序？
-   从发票行的哪些字段要用户可以在移动体验，并且，什么顺序？
-   关于发票行是否在发票？ 将该行 80-20 规则在此处，并且 80% 为优化。
-   用户是否要查看分类帐分配 (发票编码) 在查看期间，在移动设备？ 如果对此问题的回答是，请考虑以下问题：
    -   分类帐分配的总价 (、增值税、费用，拆分，依此类推) 是否为发票行？ 而且，则将该行 80-20 规则。
    -   发票是否还在发票抬头的分类帐分配？ 如果是这样，则这些分类帐分配应能够针对设备？

> [!NOTE]
> 因为此功能。要移动情况，支持当前没有为此主题说明如何编辑分类帐分配。

-   用户是否要为设备的发票可以查看附件？

移动体验的设计为发票审核根据回答将不同，有了这些问题。 优化目标将业务流程的用户体验在移动电话在组织。 在其余此主题，我们将查看基于到之前的问题的回答的这两种方案差异。 

作为一般准则，则使用移动设计器时，确保“过帐”防止丢失更改更新。

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>设计 Contoso 的简单发票审核方案
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
<td>用户要查看从发票抬头的哪些字段在移动体验，并且，什么顺序？</td>
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
<td>从发票行的哪些字段要用户可以在移动体验，并且，什么顺序？</td>
<td><ol>
<li>采购类别</li>
<li>数量</li>
<li>单价</li>
<li>行净额</li>
<li>1099 金额</li>
</ol></td>
</tr>
<tr class="odd">
<td>关于发票行是否在发票？ 将该行 80-20 规则在此处，并且 80% 为优化。</td>
<td>1</td>
</tr>
<tr class="even">
<td>用户是否要查看分类帐分配 (发票编码) 在查看期间，在移动设备？</td>
<td>是</td>
</tr>
<tr class="odd">
<td>分类帐分配的总价 (、增值税费用，依此类推) 是否为发票行？ 而且，则将该行 80-20 规则。</td>
<td>总价：增值税：2 费用：00</td>
</tr>
<tr class="even">
<td>发票是否还在发票抬头的分类帐分配？ 如果是这样，则这些分类帐分配应能够针对设备？</td>
<td>未使用</td>
</tr>
<tr class="odd">
<td>用户是否要为设备的发票可以查看附件？</td>
<td>是</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>创建工作区

1.  在浏览器，工序 365 的未结和 Dynamics，登录。
2.  在登录后，请&mode=mobile **追加**如以下示例中所示，该 URL，并刷新"页面上：https://yoururl/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**&lt;&gt;
3.  ** **设置 (单击齿轮) 将按在右上方页，然后单击** **移动应用。 正任务录制器出现，移动应用设计器必须显示。
4.  **创建新工作区**单击"添加"。 对于本例，进行命名工作区** **我的审核。
5.  输入描述。
6.  选择工作区颜色。 工作区一种颜色以移动体验的整体样式此工作区将的使用。
7.  选择工作区的图标。
8.  **完成**单击
9.  **请过帐工作区**单击"保存更改

### <a name="vendor-invoices-assigned-to-me"></a>分配给我的供应商发票

您应设计的第一个页面将是分配给用户审核的发票的列表。 若要设计这一移动页面，请使用 VendMobileInvoiceAssignedToMeListPage ** ** "工序中 Dynamics 365。 在您完成此过程之前，务须至少一个供应商分配给发票，查看您的发票，并且行具有两个配送。 此设置与此场景的要求。

1.  在工序 365，则 URL 的 Dynamics 替换的菜单项的名称。VendMobileInvoiceAssignedToMeListPage ** **打开将版本**供应商发票{{等待：Pending}}分配给我**列出在** **应付帐款模块的页面。 根据您在您的系统分配给您的发票数量，此页面将显示这些发票。 若要查找特定的发票，则可以使用左侧的筛选器。 但是，我们不能为此示例需要特定发票。 我们要求某发票分配给您要允许您设计将页面。 可用的新页用于开发供应商的发票方案将专门设计。 因此，你必须使用这些页面。 URL 应类似于下面的 URL，因此，在输入后，在图显示的页面。必须：https://yourURL/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile&lt;&gt;[![未决供应商发票分配给我的某页] (。/media/mobile 发票 approvals01 1024x281.png)](。/media/mobile 发票 approvals01.png)
2.  ** **设置 (单击齿轮) 将按在右上方页，然后单击**移动应用**
3.  选择您的工作区和编辑** **单击
4.  **创建第一页面添加单击**移动的页面。
5.  输入名称，如**我的供应商发票**和描述，例如**供应商发票分配给我**供审核。
6.  Click **Done**.
7.  在移动设计器，** **字段选项卡上，依次单击** **选择的字段。 在列表页必须列的类似于下面的示意图。 [在未决供应商发票的![列分配给我的某页] (。/media/mobile 发票 approvals02 1024x117.png)](。/media/mobile 发票 approvals02.png)
8.  必须从向用户显示在移动页的列表页添加所需的列。 假定您的订单。字段中显示给最终用户的订单。 唯一的排序方式更改字段为将通过重新选择所有字段。 基于此场景的需求，需要以下八字段。 但是，一些移动设备在用户可以具有许多会计八字段信息。 因此，我们在移动列表视图 (只显示最重要的字段。 其余字段将在其中详细信息之后查看我们将设置。 时间点，我们将添加以下字段。 **单击加号 (+**) 在这些列将添加到页面。
    1.  供应商名称
    2.  发票合计
    3.  发票帐户
    4.  发票编号
    5.  发票日期

    在字段添加后，必须将页面类似于下面的示意图。 [在字段后的![页面添加] (。/media/mobile 发票 approvals03.png)](。/media/mobile 发票 approvals03.png)
9.  您现在还必须添加下列，因此，我们能够后启用工作流操作。
    1.  查看完成任务
    2.  查看任务委托
    3.  撤回查看任务
    4.  查看拒绝任务
    5.  查看请求完成任务
    6.  查看重新提交任务

10. ** **单击"完成"退出编辑模式。
11. **单击后退** **执行**然后退出工作区
12. **请过帐工作区**保存您的工作的。单击
13. **启用未决查看有关供应商发票的发票合计**列出在"应付帐款参数"窗体下** **发票。 请注意，通过启用此参数，发票合计。未决供应商发票将计算只能显示的列表页。 作为先决条件、热修复 3208224 的一部分，此文件夹是中的新功能。

### <a name="vendor-invoice-details"></a>供应商发票详细信息

若要设计移动电话的发票详细信息"页面上，请使用 VendMobileInvoiceHeaderDetails ** ** "工序中 Dynamics 365。 根据您在系统的发票的数量，请注意，此页显示最早的发票 (首先创建) 的发票。 若要查找特定的发票，则可以使用左侧的筛选器。 但是，我们不能为此示例需要特定发票。 我们要求某些发票数据，以便我们可以设计将页面。 [] (![工作流页面。/media/mobile 发票 approvals04 1024x425.png)](。/media/mobile 发票 approvals04.png)

1.  在工序 365，则 URL 的 Dynamics 替换的菜单项的名称。VendMobileInvoiceHeaderDetails ** **打开窗体
2.  从打开的移动设计器** **设置 (齿轮按钮)。
3.  在工作区单击**编辑**按开始编辑模式。
4.  **选择我的供应商发票**您之前创建"，然后单击** **编辑。
5.  **在字段**选项卡，请单击网格** **列标题。
6.  **单击属性** &gt; ** **页面添加。 **注释：**，在单击网格** **标题时并添加页面，其中详细信息页的关系将自动创建。
7.  输入一页，例如标题** **信息和发票的详细描述，如**查看发票抬头和行明细**。
8.  单击** **选择的字段。 您注意，") 是订单字段中显示给最终用户的订单。 唯一的排序方式更改字段为将通过重新选择所有字段。
9.  从以下标题添加字段，按此场景的要求：
    1.  供应商名称
    2.  发票合计
    3.  发票帐户
    4.  发票编号
    5.  发票日期
    6.  发票描述
    7.  到期日期
    8.  发票币种

10. 从在页面行的网格添加以下字段：
    1.  采购类别
    2.  数量
    3.  单价
    4.  行净额
    5.  1099 金额

11. 在从以前两个步骤的所有字段添加后，请单击** **执行。 页面必须类似于下面的示意图。 [![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. ** **单击"完成"退出编辑模式。
13. **单击后退** **执行**然后退出工作区
14. **请过帐工作区**保存您的工作的单击

### <a name="workflow-actions"></a>工作流操作

想要添加工作流操作，请使用 VendMobileInvoiceHeaderDetails ** ** "工序中 Dynamics 365。 若要打开此页，请替换的菜单项的名称，则 URL 中的。 打开要从的移动设计器** **设置 (齿轮按钮)。 执行以下步骤在添加详细信息"页面上的工作流操作。

1.  在工作区单击**编辑**按开始编辑模式。
2.  **选择发票详细信息**您之前创建"，然后单击** **编辑。
3.  **在操作**选项卡上，单击** **添加操作。
4.  输入标题的操作，例如审核** **和描述，例如** **审核发票。 请注意您在此处输入标题成为的操作显示给用户。移动应用操作的名称。
5.  Click **Done**.
6.  单击** **选择的字段。
7.  查看在 VendMobileInvoiceHeaderDetails ** **页面的工作流，以及完成您要录制的操作。 确保您{{在此：during}}过程中输入工作流注释，因此，注解栏在移动体验还包括。
8.  在工作流操作运行后，单击** **执行完成任务选择的字段。
9.  ** **单击"完成"退出编辑模式。
10. **单击后退** **执行**然后退出工作区
11. **请过帐工作区**保存您的工作的单击
12. 重复步骤记录所有必需的工作流操作的 3 到 11。 请注意，在需求，它仍为工作流操作可用状态您的发票分配给您设计。
13. 身份打开记事本或 Microsoft Visual Studio 和粘贴，以下代码。 保存该文件，.js 文件。 此代码对两件事情就：
    1.  我们将它隐藏在列表页添加前的额外的工作流相关的列。 我们增加了这些列，以便应用有信息在环境，可能执行下一步。
    2.  基于处于有效状态的工作流步骤，则应用逻辑只显示这些操作。

注意，页面的名称，在 JS 代码的其他控件必须相同从工作区。

1.  主要功能 (metadataService，dataService，cacheService，$q {0}退货 appInit: {0}) 功能 ({0}) appMetadata //需要存在的隐藏控制，不可见，但 metadataService.configureControl (‘我供应商发票，”“”，ShowAccept {0}隐藏的：true。);metadataService.configureControl (‘我供应商发票，”“”，ShowApprove {0}隐藏的：true。);metadataService.configureControl (‘我供应商发票，”“”，ShowReject {0}隐藏的：true。);metadataService.configureControl (‘我供应商发票，”“”，ShowDelegate {0}隐藏的：true。);metadataService.configureControl (‘我供应商发票，”“”，ShowRequestChange {0}隐藏的：true。);metadataService.configureControl (‘我供应商发票，”“”，ShowRecall {0}隐藏的：true。);metadataService.configureControl (‘我供应商发票，”“”，ShowComplete {0}隐藏的：true。);metadataService.configureControl (‘我供应商发票，”“”，ShowResubmit {0}隐藏的：true。);，赋予 pageInit:功能 (pageMetadata，氰胍{0}) (如果 pageMetadata.Name“==发票详细信息”) {0} //基于工作流步骤的查看/隐藏工作流操作 metadataService.configureAction (‘可见的可接受”，: {0}true。);metadataService.configureAction (‘可见的审核”，: {0}true。);metadataService.configureAction (‘可见的拒绝”，: {0}true。);metadataService.configureAction (‘可见的委托人"，: {0}true。);metadataService.configureAction (‘可见：{0} "，请求更改 true。);metadataService.configureAction (‘可见恢复"，: {0}true。);metadataService.configureAction (‘请完成”，{0}可见：true。);metadataService.configureAction (‘请重新提交”，{0}可见：true。);

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

2.  上载代码文件。工作区通过逻辑** **选择选项卡
3.  ** **单击"完成"退出编辑模式。
4.  **单击后退** **执行**然后退出工作区
5.  **请过帐工作区**保存您的工作的单击

### <a name="vendor-invoice-attachments"></a>附件供应商发票

1.  ** **设置 (单击齿轮) 将按在右上方页，然后单击**移动应用**
2.  在工作区单击**编辑**按开始编辑模式。
3.  **选择发票详细信息**您之前创建"，然后单击** **编辑。
4.  **设置该文档管理**是** **选项如下所示。 **注释：**，如果不需要显示在移动设备的附件，可以将此选项集** **，不为默认设置。
5.  [] (![docmanagement。/media/docmanagement-216x300.png)](。/media/docmanagement.png)
6.  ** **单击"完成"退出编辑模式。
7.  **单击后退** **执行**然后退出工作区
8.  **请过帐工作区**保存您的工作的单击

### <a name="vendor-invoice-line-distributions"></a>供应商发票行。

此方案确认的需求将具有行级别仅分配，并且发票，只将始终具有一行。 由于此方案是简单，在用户不必多个级别深化查看分配的移动设备的用户体验也必须是简单足够的。 Dynamics 中 365 的供应商发票包括工序的查看来自发票抬头中所有配送的选项。 此经验正是我们为移动方案需要。 因此，我们将使用 VendMobileInvoiceAllDistributionTree ** **页面设计移动方案的这一部分。 

> [!NOTE] 
> 实际要求我们帮助确定哪一特定页面正确的使用和优化的用户的移动体验，我们在设计方案时。 在第二个情况，因为该方案的需求不同，我们将使用不同的页面查看分配。

1.  在" URL，请替换的菜单项的名称，以前，执行。 页面的显示应类似于下面的示意图。 [] (![配送所有页。/media/mobile 发票 approvals06.png)](。/media/mobile 发票 approvals06.png)
2.  从打开的移动设计器** **设置 (齿轮按钮)。
3.  在工作区单击**编辑**按开始编辑模式。 **注释：**您查看两个新的页面自动创建。 因为您打开该前面的部分，的文档管理系统创建这些页。 您可以忽略这些新的页面。
4.  **单击添加**页面。
5.  输入一页，例如标题**核算**视图和描述，例如发票核算** **的视图。
6.  Click **Done**.
7.  **在字段**选项卡上，单击** **选择的字段，从分配页面的以下字段，然后单击** **执行：
    1.  本币金额
    2.  币种
    3.  会计科目

> [!NOTE] 
> 我们不选择分发** **网格的描述，因为列，此情况要求确认的总价是唯一的金额将为具有分配。 这样，用户将不会要求其他字段确定分配金额类型。 但是，在下一个方案，则我们** **，将使用此信息，因为该方案的需求金额指定其他类型 (具有分配，例如增值税)。
8.  ** **单击"完成"退出编辑模式。
9.  **单击后退** **执行**然后退出工作区
10. **请过帐工作区**保存您的工作的单击

**注释：** **核算**页面视图移动当前未链接到到目前到目前为止我们设计的移动任何页面。 因为用户应该能够导航到从**发票详细信息**的页面视图核算** **页上移动设备，我们提供**必须从发票详细信息**页面的导航到**核算**查看页面。 我们在此可以使用额外的 JavaScript 通过逻辑。

1.  打开您之前创建的 .js 文件，然后将按以下代码中突出显示的行。 此代码对两件事情就：
    1.  该帮助保障用户不能直接从导航到工作区**核算**查看页面。
    2.  它确定从**发票详细信息**页上的某一控件。**核算**查看页面。

> [!NOTE] 
> 页面和其他控件的名称。JS 必须相同代码从工作区。

1.  主要功能 (metadataService，dataService，cacheService，$q {0}退货 appInit: {0}) 功能 ({0}) appMetadata //需要存在的隐藏控制，不可见，但 metadataService.configureControl (‘我供应商发票，”“”，ShowAccept {0}隐藏的：true。);metadataService.configureControl (‘我供应商发票，”“”，ShowApprove {0}隐藏的：true。);metadataService.configureControl (‘我供应商发票，”“”，ShowReject {0}隐藏的：true。);metadataService.configureControl (‘我供应商发票，”“”，ShowDelegate {0}隐藏的：true。);metadataService.configureControl (‘我供应商发票，”“”，ShowRequestChange {0}隐藏的：true。);metadataService.configureControl (‘我供应商发票，”“”，ShowRecall {0}隐藏的：true。);metadataService.configureControl (‘我供应商发票，”“”，ShowComplete {0}隐藏的：true。);metadataService.configureControl (‘我供应商发票，”“”，ShowResubmit {0}隐藏的：true。);隐藏不适用//页为 metadataService.hideNavigation 根目录所在 (‘视图核算”);查看 metadataService.addLink 入帐的//Link (‘发票详细信息”，“视图核算”，查看“核算 nav 控制”，“视图”核算，为 True);，赋予 pageInit:功能 (pageMetadata，氰胍{0}) (如果 pageMetadata.Name“==发票详细信息”) {0} //基于工作流步骤的查看/隐藏工作流操作 metadataService.configureAction (‘可见的可接受”，: {0}true。);metadataService.configureAction (‘可见的审核”，: {0}true。);metadataService.configureAction (‘可见的拒绝”，: {0}true。);metadataService.configureAction (‘可见的委托人"，: {0}true。);metadataService.configureAction (‘可见：{0} "，请求更改 true。);metadataService.configureAction (‘可见恢复"，: {0}true。);metadataService.configureAction (‘请完成”，{0}可见：true。);metadataService.configureAction (‘请重新提交”，{0}可见：true。);

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

2.  上载代码文件。工作区通过逻辑** **选择选项卡都会覆盖以前的代码
3.  ** **单击"完成"退出编辑模式。
4.  **单击后退** **执行**然后退出工作区
5.  **请过帐工作区**保存您的工作的单击

### <a name="validation"></a>验证

从您的移动设备，请打开应用，并连接到自己的操作实例的 Dynamics 365。 确保您登录到供应商发票查看分配给您的公司。 您应该可以执行以下操作：

-   **参阅我的审核**工作区。
-   我的操练到** **审核工作区和查看**我的供应商发票**页。
-   **到操练我的供应商发票**页和查看分配给您的发票列表。
-   操练到某一发票，并查看发票抬头详细信息和行详细信息。
-   在详细信息，请参阅"请指向附件的链接，并导航指向附件的链接使用此列表查看附件、和。
-   在详细信息，请参阅"请指向**核算**查看页面，并使用此链接导航到配送页面和查看分配。
-   在详细信息"页上，依次单击"操作菜单** **底部，并执行是适当的。工作流步骤的工作流操作。

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>设计 Fabrikam 复杂的发票审核方案
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
<td>用户要查看从发票抬头的哪些字段在移动体验，并且，什么顺序？</td>
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
<td>从发票行的哪些字段要用户可以在移动体验，并且，什么顺序？</td>
<td><ol>
<li>采购类别</li>
<li>数量</li>
<li>单价</li>
<li>行净额</li>
<li>1099 金额</li>
</ol></td>
</tr>
<tr class="odd">
<td>关于发票行是否在发票？ 将该行 80-20 规则在此处，并且 80% 为优化。</td>
<td>5</td>
</tr>
<tr class="even">
<td>用户是否要查看分类帐分配 (发票编码) 在查看期间，在移动设备？</td>
<td>是</td>
</tr>
<tr class="odd">
<td>分类帐分配的总价 (、增值税费用，依此类推) 是否为发票行？ 而且，则将该行 80-20 规则。</td>
<td>总价：增值税：2 费用：22</td>
</tr>
<tr class="even">
<td>发票是否还在发票抬头的分类帐分配？ 如果是这样，则这些分类帐分配应能够针对设备？</td>
<td>未使用</td>
</tr>
<tr class="odd">
<td>用户是否要为设备的发票可以查看附件？</td>
<td>是</td>
</tr>
</tbody>
</table>

### <a name="exercise"></a>执行

以下方案 1 差异可用于完成，基于方案 2. 的需求。 使用此部分您为可以使用完成的学习目的执行。

1.  由于更多发票行与方案 2 中预期，给该设计的以下更改将帮助优化在移动设备的用户体验：
    1.  {{而不是：Instead_of}}查看在详细信息页的发票行。(在方案 1)，用户可以选择显示在单独的页面的移动行。
    2.  由于多个发票行{{在此：in}}方案，预期，如果 VendMobileInvoiceAllDistributionTree ** **页面用于设计移动电话的配送页面 (在方案 1)，它可能是混乱的供用户可以关联到配送行。 因此，请使用 VendMobileInvoiceLineDistributionTree ** **页面设计分配页。
    3.  理想情况下，查看分配应在发票行中{{在此：in}}方案。 因此，请确保用户可以操练到行分配查看页面。 您正为标题和详细信息页执行在方案 1.，使用页面链接"钻取功能确定。

2.  由于多个金额类型在方案 2 的配送，预期 (增值税费用，等等)，显示金额的类型描述将很有用。 我们忽略在方案 (1.) 的以下信息

## <a name="conclusion"></a>结论
移动和平台应用程序功能支持您设计为组织中的用户基地优化的移动方案。 基于{{在此：in}}主题提供的示例，您可以尝试其他差异和创建满足的特定需要不同的体验。


