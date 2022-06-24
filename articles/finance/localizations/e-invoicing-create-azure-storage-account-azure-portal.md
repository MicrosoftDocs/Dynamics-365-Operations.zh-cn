---
title: 在 Azure 门户中创建 Azure 存储帐户
description: 本文说明如何为电子开票创建 Azure 存储帐户。
author: dkalyuzh
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4380261140086bcb278162f8dc70b39eaa7078fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898009"
---
# <a name="create-an-azure-storage-account-in-the-azure-portal"></a>在 Azure 门户中创建 Azure 存储帐户

[!include [banner](../includes/banner.md)]

由电子开票服务生成或在处理过程中转到该服务的所有电子文件都存储在您的 Microsoft Azure 存储帐户容器中。 为确保电子开票可以访问这些容器，您必须向电子开票服务提供存储帐户的共享访问签名 (SAS) 令牌。 此外，为确保安全存储令牌，请勿直接提供 SAS 令牌。 而是将其存储在 Azure 密钥保管库中，并提供 Azure 密钥保管库机密。

1. 打开您计划用于电子开票服务的存储帐户。
2. 转到 **设置** \> **配置**，确保将 **允许 Blob 公共访问** 参数设置为 **启用**。
3. 转到 **数据存储** \> **容器**，创建一个容器。
4. 为容器输入名称，然后将 **公共访问级别** 字段设置为 **专用(无匿名访问)**。
5. 打开新容器，转到 **设置** \> **访问策略**。
6. 选择 **添加策略** 添加存储的访问策略。
7. 根据需要设置 **标识符** 字段。
8. 在 **权限** 字段中，选择所有权限。

    ![在“添加策略”对话框的“权限”字段中选择的所有权限。](media/e-invoicing-azure-1.png)

9. 输入开始日期和结束日期。 结束日期应该在将来。
10. 选择 **确定** 保存策略，然后保存对容器进行的更改。
11. 转到 **设置** \> **共享访问令牌**，然后设置字段值。
12. 输入开始日期和结束日期。 结束日期应该在将来。
13. 在 **权限** 字段中，选择以下权限：

    - 读取
    - 添加
    - 创建
    - 写入
    - 删除
    - 列表

14. 选择 **生成 SAS 令牌和 URL**。
15. 复制并存储 **Blob SAS URL** 字段中的值。 此值稍后将在此过程中使用，将称为 *共享访问签名 URI*。
16. 打开您打算与电子开票一起使用的密钥保管库。
17. 转到 **设置** \> **机密**，选择 **生成/导入** 创建机密。
18. 在 **创建密码** 页上，在 **上载选项** 字段中，选择 **手动**。
19. 输入密码的名称。 此名称将在 Regulatory Configuration Service (RCS) 中的服务设置期间使用，将称为 *密钥保管库机密名称*。 有关如何设置 RCS 的详细信息，请参阅[设置 Regulatory Configuration Service (RCS)](e-invoicing-set-up-rcs.md)。
20. 在 **值** 字段中，输入您之前复制的共享访问签名 URI。
21. 选择 **创建**。
