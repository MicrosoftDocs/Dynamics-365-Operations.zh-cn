---
title: 从全局存储库导入功能
description: 本文说明如何从全局存储库导入全球化功能。
author: gionoder
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 5a72673e17c5653d43b60d3348d5518e09c40a15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278302"
---
# <a name="import-features-from-the-global-repository"></a>从全局存储库导入功能

[!include [banner](../includes/banner.md)]

全局存储库包含与您的配置提供程序共享的电子开票功能。 Microsoft 提供的所有电子开票功能都将与所有公司共享。 您自动有权访问 Microsoft 发布到全局存储库的所有电子开票功能。

要开始使用与您的配置提供程序共享的电子开票功能，请将它们从全局存储库导入到您的 Regulatory Configuration Service (RCS) 实例中。 然后查看功能详细信息，如电子报告 (ER) 配置和处理管道。

## <a name="import-a-feature-from-the-global-repository"></a>从全局存储库导入功能

1. 登录您的 RCS 帐户。
2. 在 **全球化功能** 工作区的 **功能** 部分中，选择 **电子开票** 磁贴。
3. 选择 **导入** 打开 **从全局知识库导入功能** 查找。
4. 要浏览全局存储库中可供特定配置提供程序使用的电子开票功能，请选择 **同步** 同步您组织的 RCS 实例。 同步完成后，可用电子开票功能的列表会在全局存储库中更新。 此更新可能需要几分钟时间。
5. 选择要导入的功能，然后选择 **导入**。

要查看导入的电子开票功能，请确保选择了正确的配置提供程序。 默认情况下，活动的配置提供程序创建的功能会被自动筛掉。您可以调整筛选器以查看其他提供程序（例如 Microsoft 配置提供程序）创建的功能。

您现在可以使用导入的功能了。 您可以查看功能的详细信息，并可以使用导入的功能作为模板创建新功能。

> [!NOTE]
> 仅当功能由当前活动的配置提供程序创建时，您才能修改它。 您可以使用原始功能作为基础来创建新功能。 然后可以进行所需的更改或设置参数。

当 Microsoft 或与您的公司共享全球化功能的其他公司更新您已导入的功能时，您可以在 **全球化功能** 工作区的 **相关设置** 部分选择 **检查功能更新** 来检查是否有更新版本。

如果您看到用作模板的功能有更新，您可以在同步全局存储库中的已发布功能列表后导入新版本。
