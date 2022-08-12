---
title: 卸载双重写入应用程序业务流程解决方案
description: 本文介绍如何卸载双重写入应用程序业务流程解决方案。
author: RamaKrishnamoorthy
ms.date: 03/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2022-01-21
ms.openlocfilehash: 676802ddabac69db4947cf806e9103f67cece3de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870365"
---
# <a name="uninstall-dual-write-application-orchestration-solutions"></a>卸载双重写入应用程序业务流程解决方案

[!include [banner](../../includes/banner.md)]

本文介绍如何卸载双重写入应用程序业务流程解决方案。

一些客户无意中安装了双重写入应用程序业务流程程序包，该程序包在其 Microsoft Dataverse 环境中安装了多个解决方案。 安装程序包中的无关解决方案可能会导致意外和不良问题。

要解决与安装双重写入应用程序业务流程程序包相关的问题，请按以下顺序卸载不需要的双重写入解决方案：

1. Dynamics365FinanceAndOperationsAnchor_managed
1. msdyn_OneFSSCM_managed（如果存在）
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps_managed
1. Dynamics365Notes_managed（若要卸载此解决方案，您必须打开 Microsoft 支持票证。）
1. DualWriteCore_managed
1. Dynamics365AssetManagementApp_managed
1. Dynamics365AssetManagement_managed
1. Dynamics365SupplyChainExtended_managed
1. Dynamics365FinanceExtended_managed
1. HCMCommon_managed
1. Dynamics365FinanceAndOperationsCommon_managed
1. Dynamics365Company_managed
1. CurrencyExchangeRates_managed
1. msdyn_AssetCommon_managed
1. FieldServiceCommon_managed

如果安装了当事方和全球通讯簿解决方案，请按以下顺序卸载这些解决方案：

1. Dynamics365FinanceAndOperationsAnchor
1. Dynamics365FinanceAndOperationsDualWriteEntityMaps
1. msdyn_DualWriteCore
1. Dynamics365AssetManagementApp
1. Dynamics365AssetManagement
1. Dynamics365SupplyChainExtended
1. Dynamics365FinanceExtended
1. HCMCommon
1. Dynamics365FinanceAndOperationsCommon
1. 当事方
1. Dynamics365Company_managed
1. CurrencyExchangeRates
1. msdyn_AssetCommon
1. FieldServiceCommon