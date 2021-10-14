---
title: 针对电子采购发包使用外部目录
description: 本主题说明如何使用外部目录创建和提交申请。
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests, CatExternalCatalogBasketWizard, CatExternalCatalogPunchoutDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b236a17a7f93bfeb60d64fa25745bd1b4cb1b34b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578024"
---
# <a name="use-external-catalogs-for-punchout-e-procurement"></a>针对电子采购发包使用外部目录

[!include [banner](../includes/banner.md)]

通过针对电子采购发包使用外部目录，您不必再在自己的主数据中维护与您的供应商的产品有关的信息。 相反，供应商网站上的购物车将转换为具有正确产品信息的申请行。 

您应该避免在您自己的产品主数据中维护供应商产品的描述和价格。 相反，应针对电子采购发包使用外部目录。 之后当员工创建申请时，他们可以“发包”到供应商的外部目录站点（换言之，他们离开您的系统，前往供应商站点）。 在供应商的网站上添加到购物车的产品随后可以转换为申请行。 因此，您将获得正确的产品信息：产品 ID、名称、价格等。

若要使用外部目录，员工必须创建在 **我的采购申请** 页创建申请。

创建申请的员工被称为申请准备人。 作为准备人，您可以完成以下任务。

使用 **外部目录** 行操作打开一个页面，该页面包含对指定申请者、购买法人和接收运营单位可用的所有外部目录。

根据您的权限，更改申请者、购买法人和接收运营单位。 更改这些值可能会更改对申请者可用的外部目录的列表。 可用的外部目录取决于购买法人或接收运营单位的当前有效的采购策略。 这些策略可以允许或阻止访问特定采购类别。 因此，映射到这些采购类别的外部目录的列表可能受到影响。

有关策略的详细信息，请参阅[采购策略概述](../procurement/purchase-policies.md)。

- 若要查找特定采购类别的外部目录，请在目录搜索字段输入文本。
- 若要添加来自供应商网站上的供应商外部目录的产品，请单击外部目录。 然后将产品添加到购物车，再签出。购物车行将转移到 Microsoft Dynamics 365。

如果有多个采购类别选项，在您将行添加到申请前，请选择正确的采购类别。
将行添加到申请后，不使用外部目录也可以添加更多行。 或者，您可以继续使用外部目录添加行。

申请准备就绪后，使用 **工作流** > **提交** 操作进行提交以供审核。

### <a name="additional-resources"></a>其他资源

- [为电子采购发包设置外部目录](set-up-external-catalog-for-punchout.md)
- [采购 cXML 增强功能](purchasing-cxml-enhancements.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]