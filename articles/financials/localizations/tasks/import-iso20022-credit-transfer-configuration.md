--- 
title: "导入 ISO20022 贷方转帐配置"
description: "此过程显示如何导入供应商付款电子申报配置。"
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 52d502a53deb6defa619af4ca8cdc3158e086bae
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="import-iso20022-credit-transfer-configuration"></a>导入 ISO20022 贷方转帐配置

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何导入供应商付款电子申报配置。 以德国 ISO 20022 贷方转帐格式为例。 此过程可用于其他可用电子申报格式。 

此任务是使用演示数据公司 DEMF 创建的，但是您可以使用任何演示数据公司完成此任务。

这是五个共同用于演示使用电子申报配置的供应商付款流程的任务中的第一个。 此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。

1. 转到“组织管理”>“工作区”>“电子申报”。
2. 在可用配置提供商列表中，选择“Microsoft”。
3. 单击“设置有效”。
4. 单击“存储库”。
5. 单击“打开”。
6. 单击“显示筛选器”。
7. 应用以下筛选器：使用“开头为”筛选器运算符在“配置名称”字段中输入筛选器值“ISO20022 贷方转帐（德国）”。
    * 也可以在列表中查找配置，选择该配置，然后将其移至“导入任务”。  
8. 单击“导入”。
    * 如果导入按钮没出现，表示该配置文件已经被导入了。  
9. 单击“是”。

