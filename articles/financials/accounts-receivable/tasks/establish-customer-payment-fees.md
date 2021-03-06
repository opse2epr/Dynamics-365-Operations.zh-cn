---
title: 设定客户付款费用
description: 为客户付款创建付款费用。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5acb202d46ef39376a01ca592f60926786d11186
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572966"
---
# <a name="establish-customer-payment-fees"></a>设定客户付款费用

[!include [task guide banner](../../includes/task-guide-banner.md)]

为客户付款创建付款费用。

本任务使用 USMF 公司进行演示。

1. 转到“应收账款”>“付款设置”>“付款费用”。
2. 单击“新建”。
3. 在“费用 ID”字段中，输入一个“费用 ID”。
    * “费用 ID”将显示在付款日记帐中，以便您足够清晰地了解所评估的费用。  
4. 在“名称”字段中，输入一个“费用名称”。
5. 在“费用描述”字段，输入一个费用描述。
6. 选择费用是向“客户”或“会计”帐户收取。
    * 如果评估费用的是客户，则选择“客户”。 如果费用作为您组织的一项开支进行评估，请选择“分类帐”。 对于此任务，选择“客户”。  
7. 选择用于此费用的日记帐类型。
    * 如果这些费用用于客户付款，则日记帐类型将是“客户付款”。  
8. 单击“保存”。
9. 单击“付款费用”设置。
    * “付款费用设置”用于定义付款费用评估时间的条件。  例如，若银行帐户是 USMF 工序且付款方式为支票时，您可以定义将会计算费用。  
10. 选择“表单”、“组”或“所有物料”以定义评估此费用的银行帐户。
    * 若您选择“全部”，则所有的银行帐户都将评估此项费用。  若您选择“表单”，将只有您所选的银行帐户可以评估此项费用。 如果选择了“组”，则只有所选银行组中的银行帐户才可评估此费用。  
11. 选择某一银行组或某一银行帐户。
    * 如果您选择了“表单”，则查找操作将显示银行帐户。 如果您选择了“组”，则查找操作将显示银行组。  
12. 在列表中，单击所选行中的链接。
13. 选择评估该费用的“付款方式”。
    * 例如，如果客户使用支票付款，而不是电子付款，您需要向您的客户评估费用。  
14. 在列表中，找到并选择所需记录。
15. 如果相关，输入付款币种。
    * 付款币种用于是否评估费用的附加条件。  例如，通常情况下采用欧元交易，所以当贵银行收取以 USD 为单位的币种付款时，便会收取附加费用。  
16. 选择费用是否为百分比、金额或间隔。
17. 输入该费用的百分比或金额。
    * 如果“百分比/金额”字段为“百分比”，则在该处输入的值将是一个百分比。 如果“百分比/金额”字段为“金额”，则在该处输入的值应为金额。 如果“百分比/金额”字段为“间隔”，则使用“间隔选项卡”定义等级。  
18. 在“费用币种”字段中，选择费用的币种。
    * 此为费用支付币种。  
19. 单击“保存”。

