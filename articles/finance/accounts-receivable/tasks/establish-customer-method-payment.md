---
title: 设定客户付款方式
description: 本主题说明如何为客户付款创建付款方式。
author: ShivamPandey-msft
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8c2095bba274ca5b19007b4abef743c908ba2b8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822339"
---
# <a name="establish-customer-method-of-payment"></a>设定客户付款方式

[!include [banner](../../includes/banner.md)]

本主题说明如何为客户付款创建付款方式。 此任务使用 USMF 公司演示。

1. 在导航窗格中，转到 **模块 > 应收帐款 > 付款设置 > 付款方式**。
2. 选择 **新建**。
3. 在 **付款方式** 字段中，为付款方式输入一个 ID。 付款方式 ID 将显示在发票和付款上，以便您足够清晰地了解正在记录的付款类型以及所使用的银行帐户。  
4. 在 **描述** 字段中，输入描述。
5. 选择需要哪种付款状态才能过帐付款。 在创建客户付款时，只有当付款状态与您在此处定义的付款状态匹配时才可以过帐。  
6. 选择如何为发票创建客户付款。 仅当运行付款提议时才使用该选项。 在进行直接借记和从客户的银行帐户收集资金时可以在客户付款中使用付款提议。  
7. 选择付款类型。 付款类型将有助于确定付款时是否会出现验证。  
8. 选择要过帐的付款的帐户类型。 通常为此选项选择“银行”。  
9. 选择该项付款将记录的银行帐户。
10. 输入“银行交易记录类型”以标识您的银行所使用的付款类型。 银行交易记录类型用于银行对帐过程，并且可以使对帐更容易。  
11. 选择此项旨在确定付款是否暂时过帐到过渡帐户。 如果您想要尝试付款的浮动时间，以此来清除银行帐户，请使用“桥接”功能。 付款将暂时过帐到一个分类帐，直到其清除了银行帐户，此时，付款将会移到您在此处定义的银行帐户。  
12. 输入过渡过帐的主要帐户。 这是使用桥接时付款将会被暂时过帐到其中的主要帐户。  
13. 使用 **文件格式** 选项卡是为电子付款设置进行定义。
14. 使用 **付款控制** 选项卡以定义必填字段。 例如，如果您要求存入所有带该付款方式的付款，您可以在此选项卡上选择该选项。  
15. 使用 **付款属性** 选项卡以定义您想针对此付款方式使用哪种付款属性。
16. 选择 **保存**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]