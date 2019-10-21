---
title: 为电子采购发包设置外部目录
description: 此主题描述使用外部目录或发包目录从供应商收集报价信息并将其添加到申请。
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9b6c3cb5b6bbc83604bee11a2472b2ad1136269
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249372"
---
# <a name="set-up-an-external-catalog-for-punchout-eprocurement"></a>为电子采购发包设置外部目录

[!include [banner](../includes/banner.md)]

通过使用外部目录，您可以确保您在 Dynamics 365 for Finance and Operations 2017 年 7 月版中后续处理的产品和价格信息准确和最新。 之后可以批准申请和转换为采购订单，并且可以向供应商下单。

设置好外部目录并且员工准备申请时，将有一个选项重定向到外部站点，即外部目录，并返回在外部站点创建的购物篮。 此通信基于 cXML 协议且必须在购买和销售组织的系统间建立。

要建立通信，您的供应商必须为您提供在外部目录配置中使用的信息，例如身份、采购员公司的域（如“DUNS”和“DUNS 编号”）、凭据以及要到达供应商目录的 URL。

## <a name="setting-up-an-external-catalog"></a>设置外部目录

外部目录应支持输入采购申请的员工被重定向到外部站点以选择产品。 员工从外部目录选择的产品连同最新价格信息被返回，并且可以添加到采购申请。 其目的是不允许员工在外部站点下单。 设置外部目录时，您需确保外部目录可访问的站点的目的是收集报价信息，不是实际下单。

### <a name="to-set-up-an-external-vendor-catalog-complete-the-following-tasks"></a>若要设置外部供应商目录，请完成以下任务：

1. 设置一个采购类别层次结构。 有关详细信息，请参阅 [设置采购类别层次结构的策略](tasks/set-up-policies-procurement-category-hierarchies.md)。
2. 在 Supply Chain Management 中登记供应商。 在您可以设置访问外部供应商目录的配置时，您必须先在 Microsoft Dynamics 365 中设置供应商和供应商联系人。 外部目录供应商也必须添加到所选采购类别。 有关登记供应商的详细信息，请参阅[管理供应商协作用户](manage-vendor-collaboration-users.md)。 有关如何分配供应商到采购类别的信息，请参阅 [核准特定采购类别的供应商](tasks/approve-vendors-specific-procurement-categories.md)。
3. 确保设置供应商使用的度量单位和币种。 有关如何创建度量单位的信息，请参阅[管理度量单位](../pim/tasks/manage-unit-measure.md)。
4. 使用对您的供应商的外部目录站点的要求配置外部供应商目录。 有关此任务的更多详细信息，请参阅[配置外部供应商目录](#configure-the-external-vendor-catalog)。
5. 测试供应商外部目录配置以验证设置是有效的而且您可以访问供应商外部目录。 使用**验证设置**操作验证您定义的请求设置消息。 此消息可以导致供应商外部目录站点在浏览器窗口中打开。 在验证期间，无法从供应商订购物料和服务。 要订购物料和服务，则必须从采购申请访问供应商的目录。
6. 通过使用**外部目录**页上的**激活目录**按钮激活外部目录。 外部目录必须在员工可以使用之前激活。 您可以在任何时间停用外部目录。


## <a name="configure-the-external-vendor-catalog"></a>配置外部供应商目录

本节提供关于上一节中的任务 4 的更多详细信息。

1. 输入供应商外部目录的名称和描述。 您输入的名称将出现在代表外部目录的购物车中，显示给创建申请的员工。 员工可以单击购物车以打开供应商外部目录站点上的目录。
2. 通过使用 **外部目录图像**操作添加图像。 此图像将出现在代表外部目录的购物车中，显示给创建申请的员工。 请注意，图像的宽度和高度必须相等。 否则图像不会正确显示。
3. 选择供应商的外部目录网站是否应显示在员工创建申请时的相同浏览器窗口中，或者是否应在新窗口中打开。
4. 选择目录的供应商。 在**法人**列表中，每个法人都有一行用于设置供应商。 要允许用户直接从某人法人（而不从其他法人）的供应商目录中申请产品，您可以对您希望提供或不提供目录的各个法人使用**禁止访问**或**允许访问**按钮。
5. 在**默认到期（天数）** 字段中，输入从外部目录收到的报价单有效，且可以用来从外部供应商进行采购的天数。 从供应商外部目录站点创建和检索报价单时，报价单截至当前系统日期有效，且在您在此字段输入的天数内一直有效。
6. 单击**添加**按钮以开始将采购目录映射到外部目录。然后，在目录名称列表中，选择一个类别。 类别列表是为供应商设置的所有法人中的供应商已经映射到的采购类别的超集。

    > [!NOTE]
    > 采购策略用于允许或限制对采购法人或接收运营单位的类别的访问权限。发包到外部目录要求允许访问至少一个映射到目录的采购类别。

7. 设置将发送到供应商的 cXML 设置请求消息。 自动生成的消息格式是为了启动会话所需的最小模板。 填写标记的值。

在任何时候，您都可以通过单击**还原消息格式**重载系统生成的消息模板。 
请注意，如果还原消息格式，当前消息将自动替换成自动生成的具有空标记的消息格式。

### <a name="cxml-setup-message"></a>cXML 设置消息
您可以在下方找到模板中包含的标记的描述：

| 字段 | 说明 | 
|---------|---------|
|< Header >< From >< Credential domain=”” >|采购员公司的域。|
|< Header >< From >< Credential>< Identity >< /Identity > | 采购员公司的标识。|
|< Header >< To >< Credential domain=”” > | 供应商公司的域。|
|< Header >< To >< Credential>< Identity >< /Identity> | 供应商公司的标识。|
|< Header >< Sender >< Credential domain=”” > | 采购员公司的域。|
|< Header >< Sender >< Credential >< Identity >< /Identity> | 采购员公司的标识。|
|< Header >< Sender >< Credential >< SharedSecret >< /SharedSecret >|采购员公司的共享密钥。|
|< 请求 deploymentMode=”” >|测试或生产部署。|
|< Request >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|供应商发包终结点的 URL。|

### <a name="extrinsic-elements"></a>外在元素

外在元素的附加信息，例如基于发包的用户的用户名称。外在元素在发生发包且可以在请求设置消息中发送时进行设置。
您的供应商可能提出在设置请求中收到外在元素的要求。 在这种情况下，您应将外在元素添加到**外部目录**页的**消息格式**部分中的外在元素列表。 指定供应商可以识别并将其映射到值的外在元素的名称。 值的选项为：用户名、用户电子邮件或随机值。
有关 cXML 协议的详细信息，请访问 [cXML.org 网站](http://cxml.org/)。

## <a name="post-back-message"></a>回发消息
回发消息是当用户从外部站点签出并返回到 Supply Chain Management 时从供应商收到的消息。 回发消息不能进行配置。 此消息基于 cXML 协议定义。以下信息可以是在申请行中收到的回发信息的一部分。

| 从供应商接收的消息 | 已复制到申请行|
|------------------------------|----------------------------------------------------------|
|< ItemIn quantity=”” > |数量|
|< ItemIn>< ItemID >< SupplierPartID >< /SupplierPartID >|外部物料 ID|
|< ItemDetail>< UnitPrice >< Money currency=”” >| 币种|
|< ItemDetail >< UnitPrice >< Money >< /Money >| 单价|
|< ItemDetail >< Description ShortName=”” >|产品名称|
|< ItemDetail >< Description >< /Description >|包含在物料描述中；产品名称，如果未指定 ShortName。|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|单位|
|< ItemDetail >< Classification >< /Classification >|包含在物料描述中|
|< ItemDetail >< Classification domain=”” >|包含在物料描述中|

## <a name="delete-an-external-catalog"></a>删除外部目录
删除页面上具有删除操作的外部目录。

如果从外部供应商的目录请求产品，不能删除外部供应商目录。 相反，外部供应商目录的状态被设置为无效。 如果您要取消对外部供应商的目录站点的访问，但是不删除它，请将外部目录的状态更改为无效。

