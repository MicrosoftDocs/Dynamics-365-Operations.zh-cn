---
title: 批量创建月日记帐条目
description: 本文说明如何在记录月租赁费用时批量创建日记帐条目来帮助提高效率。
author: moaamer
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fb5c65b0a2c982171fa0ae88141d92c2f1ead6ac
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894984"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a>批量创建月日记帐条目

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


本文说明如何在记录月租赁费用时批量创建日记帐条目来帮助提高效率。 批处理可用于从多个计划创建日记帐条目。 这些日记帐条目可以包括租赁付款、负债摊销、使用权 (ROU) 资产摊销以及执行成本费用。 您还可以使用批处理来同时对多个租赁进行初始识别，或者同时为多个租赁创建转换调整。

要设置批处理作业，或处理多个租赁的付款发票、折旧或利息，请转到 **资产租赁 \> 定期 \> 批量创建日记帐**。 在出现的对话框中，您可以选择用于创建日记帐条目的计划。 您还可以指定是否应针对特定实体、租赁组或租赁帐簿运行批处理流程。

> [!NOTE]
> 后续交易（如负债摊销计划、付款、折旧和费用）将仅在相应租赁的初始确认过帐后才过帐。
>
> 将创建日记帐条目，但是在您选择 **运行** 命令之前，不会过帐这些条目。

若要在租赁开始日期之外的其他日期过帐初始确认日记帐，请选择 **分配初始确认过帐日期**。 将显示 **日期** 字段，以便您可以指定正确的过帐日期。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
