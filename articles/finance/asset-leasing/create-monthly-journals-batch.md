---
title: 批量创建月日记帐条目
description: 本主题说明如何在记录月租赁费用时批量创建日记帐条目来帮助提高效率。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cb03ebe316b1655b1d0ad1d2b9108c4ead7fc61f7a25b4f554b574186efa03b7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737717"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a>批量创建月日记帐条目

[!include [banner](../includes/banner.md)]

本主题说明如何在记录月租赁费用时批量创建日记帐条目来帮助提高效率。 批处理可用于从多个计划创建日记帐条目。 这些日记帐条目可以包括租赁付款、负债摊销、使用权 (ROU) 资产摊销以及执行成本费用。 您还可以使用批处理来同时对多个租赁进行初始识别，或者同时为多个租赁创建转换调整。

要设置批处理作业，或处理多个租赁的付款发票、折旧或利息，请转到 **资产租赁 \> 定期 \> 批量创建日记帐**。 在出现的对话框中，您可以选择用于创建日记帐条目的计划。 您还可以指定是否应针对特定实体、租赁组或租赁帐簿运行批处理流程。

> [!NOTE]
> 后续交易（如负债摊销计划、付款、折旧和费用）将仅在相应租赁的初始确认过帐后才过帐。
>
> 将创建日记帐条目，但是在您选择 **运行** 命令之前，不会过帐这些条目。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
