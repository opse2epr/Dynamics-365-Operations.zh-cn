---
title: "设置条码"
description: "本文介绍了如何在 Microsoft Dynamics 365 for Operations - Retail 中使用条码。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 7734a08756f5b737744f9c8ce1d358be020b859f
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bar-codes"></a>设置条码

[!include[banner](includes/banner.md)]


本文介绍了如何在 Microsoft Dynamics 365 for Operations - Retail 中使用条码。

您可以使用条码采购和销售产品、跟踪产品变型和设置客户和员工。 您还可以使用条码发货和批准优惠券、礼品卡和贷方通知单。 您可以设置零售产品，以便具有标准条码或自定义公司内部条码。 产品可以有多个条码。 例如，如果来自不同的制造商，则产品可能具有多个条码，或者，如果基于大小、样式或颜色的变量它具有款式。 条码可以包含产品的重量或价格。 条码掩码是用于创建条码的模板。 **注意：**如果您为每个变型组合分配唯一条码，您可以在收银机上扫描条码，让程序确定出售的是哪种产品款式。 可以按款式收集和查看有关销售的统计。 可以为每个大小、颜色和样式组都分配一个可在条码中标识该组的唯一编号。 Dynamics 365 for Operations 使用条码掩码来自动为每种款式组合生成条码。 如果存在多种大小、颜色和样式的情况下功能很有用，因为不断添加款式代码将显著增加组合的数量。 如果不使用此功能，必须手动将条码分配给表示产品变型的每个组合。 可以通过手动方式或自动方式来创建条码。 若要创建条码，请按照其列出的顺序完成以下任务。

1.  [设置条码掩码字符](set-up-bar-code-masks.md)。
2.  [设置条码掩码](set-up-bar-code-masks.md)。
3.  配置条码设置。
4.  为产品创建条码。


<a name="see-also"></a>请参阅
--------

[设置条码掩码](set-up-bar-code-masks.md)



