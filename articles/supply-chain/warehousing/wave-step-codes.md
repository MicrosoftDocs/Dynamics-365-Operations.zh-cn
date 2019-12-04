---
title: 波次步骤代码
description: 此主题提供波次步骤代码及其用法的概述。
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992349"
---
# <a name="wave-step-codes"></a>波次步骤代码

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a>关于波次步骤代码

波次步骤代码是用户可设置并用于将特定波次方法实例链接到相应模板的代码。 模板包括用于补货、集装化、标签打印、装载计划和排序的模板。

如果不使用波次步骤代码，用户必须输入普通文本才能引用来自波次方法实例的特定模板。 普通文本容易出错，因为用户必须确保其为波次模板中的特定波次步骤方法添加的波次步骤文本与目标模板中的波次步骤文本完全匹配。

特定波次步骤类型的波次步骤类型在单独页面中设置。 必须在下拉列表中为波次模板中每个需要波次步骤代码的波次步骤方法实例选择波次步骤代码。 在下拉列表中进行的选择将替换普通文本，因此有助于降低人为错误的风险和影响。 设置代码用于将波次模板中的波次步骤方法链接到该方法的目标模板。

> [!NOTE]
> 是否使用波次步骤代码功能为可选，并且按法人使用。 因此，如果特定法人使用此功能，则将把该法人中的所有现有波次步骤代码升级为新结构。

## <a name="setup-demo"></a>设置演示 

必须为此演示安装演示数据，并且必须使用 **USMF** 演示数据公司。

### <a name="enable-wave-step-codes"></a>启用波次步骤代码

请执行以下步骤开启波次步骤代码功能。

1. 转到**仓库管理 \> 设置 \> 仓库管理参数**。
2. 在**常规**选项卡的**波次处理**快速选项卡上，将**启用波次步骤代码**选项设置为**是**。

将把所有现有波次步骤普通文本升级为新结构。 为法人完成此升级之后，**波次管理参数**页上的**启用波次步骤代码**选项不再可用。

升级期间将进行验证，而如果升级失败，您将收到错误消息。 以下冲突可能导致升级失败：

- 存在重复波次步骤普通文本。
- 存在自定义项。
- 与波次步骤方法实例关联的波次步骤普通文本与预期模板类型不匹配。

解决验证期间确定的所有冲突之后，可以重新运行升级流程。

升级成功之后，**波次步骤代码**页（**仓库管理 \> 设置 \> 波次 \> 波次步骤代码**）变为可用。 此页中列出开启波次步骤代码功能时升级的波次步骤代码。

### <a name="create-new-wave-step-codes"></a>创建新波次步骤代码

可使用**波次步骤代码**页创建和删除波次步骤代码。

每个新波次步骤代码及其关联的 ID 必须在所有波次步骤类型中唯一，并且必须是为特定波次步骤类型定义的。

### <a name="apply-wave-step-codes"></a>应用波次步骤代码

定义正确的波次步骤代码之后，可以将其应用于波次处理方法。

若要应用波次步骤代码，请转到相应的目标模板。 下面是波次步骤代码应该针对的目标模板：

- **补货模板：** 仓库管理 \> 设置 \> 补货 \> 补货模板
- **装载计划模板：** 仓库管理 \> 设置 \> 装载 \> 装载计划模板
- **排序模板：** 仓库管理 \> 设置 \> 装箱 \> 出站排序模板
- **集装化模板：** 仓库管理 \> 设置 \> 集装箱 \> 集装箱生成模板
- **标签打印模板：** 仓库管理 \> 设置 \> 文档路线选择 \> 波次标签模板

从波次模板中选择的波次处理方法引用此列表中的模板时，将应用这些模板。 如果波次模板中的波次处理方法的波次步骤代码与一个模板类型中的波次步骤代码匹配，将应用该模板。

### <a name="sample-scenario"></a>示例场景

以下过程可帮助确保为波次模板应用您创建的补货模板。

1. 转到**仓库管理 \> 设置 \> 波次 \> 波次步骤代码**，然后为**补货**类型创建波次步骤代码。
2. 转到**仓库管理 \> 设置 \> 补货 \> 补货模板**，然后创建补货模板。
3. 在补货模板中，选择为**补货**类型创建的波次步骤代码。
4. 转到**仓库管理 \> 设置 \> 波次 \> 波次模板**，然后选择要使用的波次模板。
5. 在该模板中的**方法**快速选项卡上，选择**捕获**方法。
6. 在**波次步骤代码**字段中，选择在补货模板中选择的波次步骤代码。