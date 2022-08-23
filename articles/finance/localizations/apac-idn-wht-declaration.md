---
title: 印度尼西亚的预缴税金报表
description: 本文说明如何配置和生成印度尼西亚的预缴税金报表。
author: AdamTrukawka
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-12-02
ms.dyn365.ops.version: 10.0.20
ms.search.scope: ''
ms.openlocfilehash: 732db563532ebc46c7b9fc69c2aaa128640084f5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282426"
---
# <a name="withholding-tax-report-for-indonesia-id-00005"></a>印度尼西亚的预缴税金报表 (ID-00005)

[!include [banner](../includes/banner.md)]

本文说明如何设置和生成 PPH 预缴税金文件，印度尼西亚的法人使用该文件在 e-Bupot 应用程序中报告预缴交易。

印度尼西亚税务主管机构 (DGT) 确定，在 KPP Pratama 注册为所得税 (PPh)“第 23 条”和/或“第 26 条”报表的扣税义务人/收税者的应纳税创业者 (PKP) 必须使用 e-Bupot 应用程序以电子方式报告所得税退税第 23 条和第 26 条报表。 

- **第 23 条** - 此报表包括供应商的所有预缴交易，其中主要地址的国家/地区代码是印度尼西亚的代码。
- **第 26 条** - 此报表包括供应商的所有预缴交易，其中主要地址的国家/地区代码不是印度尼西亚的代码。

## <a name="prerequisites"></a>先决条件

- 法人的主地址必须在印度尼西亚。
- 在 **功能管理** 工作区中，必须启用 **全球预缴税金** 功能。 有关如何启用功能的详细信息，请参阅[功能管理概述。](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

### <a name="download-electronic-reporting-configurations"></a>下载电子报告配置

导入文件的生成基于电子报告 (ER) 配置。 有关可配置报告的功能和概念的更多信息，请参见[电子报告](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)。

对于生产和用户验收测试 (UAT) 环境，请按照[从 Lifecycle Services 下载电子报告配置](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)中的说明进行操作。

要生成导入文件，请从存储库上传以下配置：

- **Tax declaration model.version.93.xml** 或更高版本
- **Tax declaration model mapping.version.93.153.xml** 或更高版本
- **WHT PPh schema import (ID).version.93.14** 或更高版本

## <a name="set-up-general-ledger-parameters"></a>设置总帐参数

1. 转到 **税** \> **设置** \> **总帐参数**。
2. 在 **预扣税** 选项卡上的 **WHT 申报格式映射** 字段中，选择 **WHT PPh 架构导入 (ID)**。 
3. 转到 **税** \> **设置** \> **预缴税金** \> **预缴税金收入类型**，以设置 **Kode Bukti Potong** 预缴税金收入类型，然后将代码分配给相关物料预缴税金组。 使用 e-Bupot 应用程序生成集成文件需要使用代码。 

## <a name="generate-the-withholding-import-file"></a>生成预缴导入文件

针对特定时期准备和生成 e-Bupot 文件的过程基于在结算和过帐纳税作业期间过帐的预缴税金交易。

请执行以下步骤以生成此文件。

1. 转到 **税** \> **申报** \> **预缴税金** \> **PPH 导入文件 e-bupot 23 和 26**。
2. 选择报表的“开始”日期和“结束”日期，然后选择结算期间。
3. 输入交易日期，然后选择 **确定**。
4. 选择语言。 所有报表均翻译为美国英语 (**en-us**) 和印度尼西亚语 (**id**)。
5. 选择业务类型，然后输入支票和单据编号。 
6. 检查经理是否已签署报表。 文件中报告了此信息。 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
