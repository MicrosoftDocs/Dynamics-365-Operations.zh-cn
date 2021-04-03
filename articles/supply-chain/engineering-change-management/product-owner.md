---
title: 产品所有者
description: 此主题提供有关产品所有者的信息。 产品所有者是负责特定产品的一组用户。 只有该组成员可以发布这些产品。 产品所有者也可以在审核工作流中使用。
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: a1c3bc6f77fed83cfbbd502cdd469baa491fd81f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5266119"
---
# <a name="product-owners"></a>产品所有者

[!include [banner](../includes/banner.md)]

产品所有者是负责特定产品的一组用户。 将产品所有者组分配给产品后，只有该组的成员可以发布该产品。 产品所有者也可以在工程更改管理中的审核工作流中使用。

产品所有者是全局设置。 因此，可用于所有法人。

## <a name="create-a-product-owner-group"></a>创建产品所有者组

若要创建产品所有者组并向其中添加成员，请按照下列步骤操作。

1. 转到 **工程更改管理 \> 设置 \> 产品所有者**。
2. 在操作窗格上，选择 **新建**。
3. 在 **产品所有者** 字段中，为组输入名称。
4. 在 **名称** 字段中，输入组的描述。
5. 在 **成员** 快速选项卡上，添加应成为组成员的工作人员。

## <a name="assign-a-product-owner-to-a-product"></a>向产品分配产品所有者

要向产品分配产品所有者，请执行以下步骤。

1. 打开相关产品或基础产品的 **产品详细信息** 页。
1. 在 **常规** 快速选项卡上，将 **产品所有者** 字段设置为相关产品所有者组的名称。

将产品所有者分配给产品后，只有产品所有者组的成员可以编辑 **产品所有者** 设置。

产品所有者也在 **已发布产品** 页上可见。

## <a name="product-owners-and-product-releases"></a>产品所有者和产品发布

只有产品的产品所有者组中的用户可以发布该产品。 但是，如果产品是子物料并且其父物料由父物料的所有者发布，这时会有例外。 换言之，如果该产品是另一个产品的物料清单的一部分，系统不会检查物料清单中每个物料的产品所有者。 只会检查父物料的产品所有者。

例如，产品 X 被分配到 *设计柜* 产品所有者组。 产品 X 也是产品 Y 的物料清单的一部分，后者被分配到 *设计扬声器* 产品所有者组。 如果来自 *设计扬声器* 产品所有者组的用户发布产品 Y 及其物料清单，产品 X 将与产品 Y 一起发布。

## <a name="product-owners-and-approvals"></a>产品所有者和审核

因为产品所有者知道特定的工程更改是否会对他们的产品有所帮助，所以在工程更改管理中将它们作为审核流程的一部分包括在内通常是有意义的。 您可以通过在用于工程更改管理的工作流中将产品所有者设置为参与者提供方来实现此方法。 然后，系统将基于工程更改请求和工程更改订单中的产品在工作流中分配审核任务。 有关详细信息，请参阅[管理工程产品的更改](engineering-change-management.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]