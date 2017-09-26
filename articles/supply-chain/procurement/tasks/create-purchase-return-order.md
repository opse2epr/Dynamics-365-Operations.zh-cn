--- 
title: "创建采购退货单"
description: "此过程演示如何通过使用“贷方通知单”操作将供应商发票单据中的行复制到新采购订单中来创建采购退货单。"
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 45d5eb62abd916316ffc323727035b77760cd30d
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-return-order"></a>创建采购退货单

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程演示如何通过使用“贷方通知单”操作将供应商发票单据中的行复制到新采购订单中来创建采购退货单。 还演示如何确认订单和处理要退给供应商的货物的装运。 可以在 USMF 演示数据公司中使用本过程中的示例。 此任务通常由采购代理完成。


## <a name="create-a-new-purchase-return-order"></a>新建采购退货单
1. 转到“采购”>“采购订单”>“所有采购订单”。
    * 第一步是新建要用作采购退货单的采购订单。  
2. 单击“新建”。
3. 在“供应商帐户”字段中输入 US-102。
4. 单击“确定”。
5. 在操作窗格上，单击“采购”。
6. 单击“贷方通知单”。
    * 这是可在其中将现有供应商发票中的内容复制到退货单的页面。 这是用于其他复制操作的相同页面。 因为此页面是通过贷方通知单操作打开的，所以此页面配置为支持创建用于抵消供应商发票的退货单。  
7. 展开“参数”部分。
    * “符号反转”选项自动选中，并且不能更改。 这保证为数量更改此符号，并且添加的订单行抵消供应商发票。  
    * “复制费用”选项自动选中，并且不能更改。 这意味着将把供应商发票中的费用添加到采购退货单以抵消原始费用。 可以在以后修改订单头和行中的更改。  
    * “准确复制”选项自动选中，并且不能更改。 这确保准确复制供应商发票头和行中所有字段内的值。 这意味着使用与通过供应商发票单据创建的所有物料匹配的值创建采购退货单。  
    * “删除采购行”选项删除添加新行之前采购订单中已有的所有采购订单行。 在本示例中，尚未向采购退货单添加任何行，所以不会有任何效果。 请谨慎使用此选项，因为它在不进一步警告的情况下删除所有现有行。  
    * “复制订单头”选项自动选中，并且不能更改。 这确保从供应商发票复制信息并应用于采购退货单头。 这非常有用，因为有助于确保采购退货单通过使用类似物料抵消发票。  
8. 折叠“参数”部分。
9. 展开“发票”部分。
    * 此页面是通过贷方通知单操作打开的，所以唯一可用选项是从供应商发票复制信息。 此选项卡显示您在前面创建的采购退货单中指定的供应商帐户的可用发票。   发票通过发票凭证或采购订单 ID 标识。  
10. 找到发票编号 AP-0006 标识的供应商发票，然后通过单击该行中的任意字段突出显示该行。
11. 通过在行的复选框中单击选中行。 
    * 请注意，供应商发票中的可用行随订单一起自动选中。 这张特殊供应商发票有 2 个订单行。 对于此示例，我们将退回第二行中的部分数量。  
12. 通过单击第二行（即具有物料 M0006 的行）中的任意字段突出显示该行。
13. 在“数量”字段中，将数量更改为 10。 这是将退给供应商的数量。 
14. 通过单击第一行（即具有物料 M0005 的行）中的任意字段突出显示该行。
15. 清除该行的复选框。
    * 将仅把您已选中的行复制到订单。  
16. 折叠“发票”部分。
17. 展开“要复制的选定行或标题”部分。
    * 此视图显示您已选择要复制到订单的所有单据和行。  
18. 折叠“要复制的选定行或标题”部分。
19. 单击“确定”。
    * 您选择的行现在已复制到了您的采购退货单。 “数量”字段显示 -10。   
20. 单击“库存”。
21. 单击“标记”。
    * 创建的订单行根据供应商发票中的库存交易记录来标记。 这保证了退给供应商的库存与之前从供应商处收到的库存相同。 有些情况下不进行标记，例如，如果库存已标记为“已消耗”，或者如果该产品不使用标记功能。  
22. 单击“确定”。

## <a name="confirm-and-record-the-shipment-of-goods"></a>确认和记录货物的装运
1. 单击“确认”。
2. 在操作窗格上，单击“接收”。
3. 单击“产品收据”。
    * 此页用于记录采购订单的产品收货，以及处理向供应商的退货。 包含负数量的订单行表示要退货给供应商，并且可将可从该页生成的单据用作此用途的装箱单。   
    * 在“数量”字段中，为此示例选择“订购数量”。   这确保处理随订单行创建的整个订购数量的装运。   
4. 在“产品收据”字段中，输入一个值。
    * 此字段用于输入将用作产品收货日记帐的凭证的参考。  
5. 单击“确定”。
    * 此货物现已在采购退货单中记录为已装运，并已创建了产品收货日记帐。 可使用“产品收货”操作审查随采购订单创建的日记帐，以了解产品的收货或退货内容和收货或退货时间。  

