--- 
title: "设定客户付款期限"
description: "此程序定义了一个现金折扣和到期日期设置。"
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c871421254be6b0e9443fdf596932776d64428ae
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="establish-customer-payment-terms"></a>设定客户付款期限

[!include[task guide banner](../../includes/task-guide-banner.md)]

此程序定义了一个现金折扣和到期日期设置。 此任务指南使用 USMF 公司演示。

1. 转到“应收帐款”>“付款设置”>“付款日”。
    * “付款期限”的设置为“应收帐款”和“应付帐款”共享。 如果您在模块中进行定义，其它模板也可以使用这些定义。 对于此任务向导，我在应收帐款下设置了所有付款期限。  
2. 单击“新建”。
    * 如果您的付款期限要求一周中特定的一天（星期一，星期二等）或一个月中特定的一天（5 日，10 日等），请创建付款日。  
3. 在“付款日期”字段中，为付款日输入一个 ID。
4. 在“描述”字段中，输入付款日的描述。
5. 在“周/月”字段中，选择“周”或“月”。
    * 如果您要输入一周中的一天，如星期一，请选择“周”。 如果要输入一个月中的一天，如 10 日，选择“月”。 此示例中，选择“月”。  
6. 在“日期”字段中，输入一个日期。
    * 日期应作为数字输入，如“10”而不是“第 10”。  
7. 单击“保存”。
8. 关闭该页面。
9. 转到“应收帐款”>“付款设置”>“付款期限”。
10. 单击“新建”。
    * 付款期用于定义如何计算到期日。 现金打折日期设置在另一个页面进行定义。  
11. 在“付款期限”字段中，输入一个 ID。
12. 在“描述”字段中，输入描述。
13. 选择一种付款方式，如货到付款、净额、当前月份等。
    * 款方法用于定义如何开始计算到期日期。  例如，如果到期日总是发票日期后的固定月数或天数，将使用净额。 如果使用货到付款，当收到发票时需要付款，所以将不计算到期日。 在此任务向导中，选择“当前月份”。  
14. 如果计算中包括了一周中的特定一天或特定一日，请选择一个付款日。
    * 根据您的付款期限，您可以以月或天数为单位输入一个数量。 或者您可以使用付款计划或付款日来“添加”到付款方式的结束日期。 如果到期日期始终是下个月的 10 号，选择日期为 10 号的付款日。  
15. 单击“保存”。
16. 关闭该页面。
17. 转到“应收帐款”>“付款设置”>“现金折扣”。
18. 单击“新建”。
    * 此页面用于定义如何计算现金折旧日期。  
19. 在“现金折扣”字段中，输入一个 ID。
20. 在“描述”字段中，输入描述。
21. 如果分层的现金折旧可用，则选择与这个新的现金折旧相关的“下一个折旧代码”。
22. 输入一个天数，用于计算现金折旧日期。
    * 如果选择了“净额原则”，天数将被添加到发票日期来计算现金折旧日期。  
23. 输入现金折旧的百分比。
24. 输入客户发票的主要帐户，现金折旧将过帐到该主要帐户。
25. 选择“折旧抵销帐户”字段中，选择一个选项。
    * 如果您选择“发票行上的帐户”，现金折旧将被过帐到供应商发票行的同一资产/费用主要帐户。 如果您选择“使用供应商发票的主要帐户”，现金折旧将被过帐到您在“供应商的主要帐户”中定义的主要帐户。 对于本示例，选择“使用供应商发票的主要帐户”。  
26. 输入一个供应商发票主要帐户，现金折旧将过帐到该主要帐户。
27. 单击“保存”。

