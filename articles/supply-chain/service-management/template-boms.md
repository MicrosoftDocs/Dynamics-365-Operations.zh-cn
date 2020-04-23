---
title: 物料清单模板
description: 使用物料清单模板提供定期提供服务的服务对象组件的标准化列表。
author: ShylaThompson
manager: tfehr
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8842a293a50efb24590784cc52ef0254eca10e3a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206534"
---
# <a name="template-boms"></a>物料清单模板    

[!include [banner](../includes/banner.md)]


使用物料清单模板为您提供定期提供服务的服务对象组件的标准化列表。 物料清单模板中所列的组件表示服务对象的各个子组件。 当您将物料清单模板应用到某服务对象时，您可以记录为该服务对象更换了哪些子组件。

为了将物料清单模板应用到某一服务协议或服务订单，您将它附加到某一服务对象关系。


> [!NOTE]
> <P>每个服务对象只能应用一个物料清单模板。</P>

## <a name="create-a-template-bom"></a>创建物料清单模板

下表包含可用于创建物料清单模板的各种方式的信息。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>方法</p></th>
<th><p> 描述</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>生产</p></td>
<td><p>物料清单模板基于生产订单。 如果仅在生产环境中操作，将适用此选项。 它的好处是提供构成物料的组件的当前详细清单。</p></td>
</tr>
<tr class="even">
<td><p>物料 BOM</p></td>
<td><p>该物料清单模板基于某一物料的物料清单。 该物料的物料清单与生产物料清单不同，为构成物料的组件的一个静态列表。</p></td>
</tr>
<tr class="odd">
<td><p>现有的模板</p></td>
<td><p>该模板基于现有物料清单的模版。</p></td>
</tr>
<tr class="even">
<td><p>手动</p></td>
<td><p>如果了解通常要为服务对象更换哪些备件，您可能创建自己的物料清单模板。 此方法可以帮助您确保模板中包括的组件反映工作场所的实际需求。</p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a>将物料清单模板应用到某一服务协议或服务订单

您可以将物料清单模板应用到服务协议、服务订单或两者同时应用。 服务协议通常涉及与客户的长期关系。 服务物料清单上记录的更换历史信息对服务协议是有用的数据。

您还可以将物料清单模板应用到某服务订单记录为该服务对象执行的服务的历史记录。

## <a name="copy-the-history-of-a-service-bom"></a>复制服务物料清单的历史记录

可以将服务物料清单行的历史记录从一个服务协议复制到另一个服务协议。 通过在服务协议间复制服务历史记录，可以保存物料的更换记录。

**示例**

您为客户的小汽车设置了三年的服务协议。 在该期间，客户已习惯公司提供的优良服务。 因此，在协议到期后，客户想要设置新的协议。 您现在可以寻求通过谈判签订对公司更有利的协议。 因为更换组件的记录在将来可能有用，您将服务物料清单的历史记录复制到新协议。

## <a name="modify-the-template-bom"></a>修改物料清单模板

如果尚未将物料清单模板附加到服务对象，可以修改或删除其中的行。 将物料清单模板附加到某服务对象后，只能修改物料清单的本地版本。 如果要复制物料清单模板本地版本的设置，可以基于本地版本创建新的物料清单模板。 有关服务间隔的详细信息，请参阅[修改物料清单模板](modify-service-bom.md)。

如果更换物料清单中的某个物料，可以在物料清单设计器中的物料清单行上登记更换情况。 或者，您可以为更换对象创建服务订单行。 如果创建服务订单行，您可以为更换物料开发票。 如果不为更换创建服务订单行，将保留更换登记跟踪服务对象的历史记录。

## <a name="change-how-information-on-the-bom-line-is-displayed"></a>更改任何显示物料清单行信息

可以更改所有模板和服务物料清单显示物料清单行信息的方式。 更改应用于所有物料清单模板和服务物料清单。 这包括附加到服务对象的物料。

## <a name="set-up-number-sequences-for-template-boms"></a>设置物料清单模板的编号规则

若要使用物料清单模板，您必须设置两个编号规则。 设置一个编号规则用于物料清单模板，一个用于物料清单历史记录行号。


> [!NOTE]
> <P>编号规则用于分配标识到需要它们的记录。 在您可以将某一编号规则分配给物料清单模板或物料清单历史记录行编号之前，必须设置编号规则代码。</P>


## <a name="set-up-number-sequences"></a>设置编号规则

1.  在**编号规则**列表页，创建物料清单模板和物料清单历史记录行编号的编号规则。 

2.  单击**服务管理** \> **设置**\> **服务管理参数**。

3.  单击**编号规则** ，然后为您在**编号规则**窗体中创建的编号规则引用的编号规则代码。

4.  关闭窗体以保存您所做更改。


> [!NOTE]
> <P>系统使用物料清单历史记录行编号将物料清单历史记录中的交易记录与某一服务协议或服务订单关联。 编号不显示在用户界面上。</P>



## <a name="see-also"></a>请参阅

[创建物料清单模板](create-template-bom.md)

[管理针对对象关系的物料清单模板](manage-template-boms-on-object-relations.md)

[修改服务项清单](modify-service-bom.md)

 


