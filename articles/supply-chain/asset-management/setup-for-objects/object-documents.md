---
title: 资产文档
description: 本主题介绍资产管理中的资产文档。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8e93ae3a1170b2f8441d29090af7a5a91db94e8e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245387"
---
# <a name="asset-documents"></a>资产文档

[!include [banner](../../includes/banner.md)]

 

本主题介绍资产管理中的资产文档。

在资产管理中，可设置文档，以便将其与作业类型、资产制造商、资产类型或资产之类自动关联。 此功能在发布了更新后的文档版本时非常有用。 在此情况下，只需将更新后的文档放到您的 Supply Chain Management 文档所用标准位置，然后将该文档附加到您已创建的资产文档记录。 然后可以从 **所有资产**、**有效资产**、**我的有效资产**、**所有工作订单** 和 **有效工作订单作业** 菜单项访问更新后的文档。 将文档附加到资产文档记录的过程使用标准文档处理系统。

**示例 1：** 与作业类型关联的文档可能介绍该作业类型的过程。

**示例 2：** 与资产类型、制造商和模型关联的文档可以是所选资产制造商模型的标准手册。

## <a name="create-asset-document-relation"></a>创建资产文档关联

1. 选择 **资产管理** \> **设置** \> **资产文档**。
2. 选择 **新建** 创建资产文档记录。
3. 根据所需文档关联的具体程度，在下面的一个或多个字段中进行相关选择：**资产类型**、**制造商**、**模型**、**资产**、**作业类型类别**、**作业类型**、**作业类型变体** 和 **作业要求**。 **作业类型变体** 和 **作业要求** 字段中的可用选项取决于在 **作业类型** 字段中进行的选择。

    > [!NOTE]
    > 系统搜索应该与资产或工作订单关联的文档时，资产管理检查所有资产文档记录以查找是否有可能的匹配项。 始终先检查最具体的组合。 换句话说，资产管理首先会检查 **作业要求** 字段的匹配项。 如果未找到匹配项，将检查 **作业类型变体** 字段的匹配项。 如果未找到匹配项，将检查 **作业类型** 字段的匹配项，以此类推。 如 **资产文档** 页面布局中显示，此行为表示为了找到最具体的组合，资产管理从右到左检查每个记录以查找匹配项。 可以将多个文档与一个资产或工作订单关联。 可按照需要编辑维护请求或工作订单中的服务级别。

4. 选择 **附件**。 将显示标准 **文档处理** 页。
5. 设置应该附加到资产文档记录的文档或注释。 附加文档之后，**附件** 字段显示与记录关联的文档数量。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]