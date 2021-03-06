---
title: 定义原始凭证的审计策略
description: 此过程显示如何设置和运行审计政策规则。
author: ryansandness
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a82c3e8e8787beb309b75b73cda36f4ca8031d6f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558875"
---
# <a name="define-audit-policies-for-source-documents"></a>定义原始凭证的审计策略

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何设置和运行审计政策规则。 本例使用含酒店费用类型的费用报表。 该程序适用于 USMF 演示公司。 审计角色包含执行这些任务的正确权限。

1. 转至“审计工作台”>“设置”>“政策规则类型”。
2. 单击“新建”。
3. 在“规则名称”字段中，输入一个值。
4. 在“描述”字段中，键入一个值。
5. 在“查询名称”字段中，选择“费用报表”行
6. 在“查询类型”字段中，选择“汇总”
7. 在“法人实体”字段中，选择“法人实体”
8. 在“文档日期引用”字段中，选择“已修改的日期和时间”
9. 单击“保存”。
10. 转至“审计工作台”>“设置”>“审计政策”。
11. 单击“新建”。
12. 在“名称”字段中，键入一个值。
13. 展开“政策组织”部分。
14. 在树结构中，选择“美国 Contoso 娱乐系统”。
15. 单击“添加”。
16. 在树结构中，选择“美国 Contoso 咨询”。
17. 单击“添加”。
18. 在树结构中，选择“美国 Contoso 零售”。
19. 单击“添加”。
20. 展开“政策组织”部分。
21. 展开“政策规则”部分。
22. 在列表中，查找并选择以前创建的政策规则。
23. 单击“创建政策规则”。
24. 在“有效日期”字段中输入日期和时间。
25. 单击“筛选器”。
26. 在列表中，选择“费用类别”行，然后设置酒店详细信息
27. 在“标准”字段中，输入或选择一个值。
28. 单击“汇总”选项卡。
29. 单击“添加”。
30. 在列表中，选择“交易金额”上的字段值
31. 在名为“字段”的字段中，输入或选择一个值。
32. 在“汇总功能”字段中，选择“合计”。
33. 单击选项卡上的“组别”。
34. 单击“添加”。
35. 在列表中，选择员工值 
36. 单击“添加”。
37. 在列表中，选择“费用类别”的值
38. 在名为“字段”的字段中，输入或选择一个值。
39. 单击“持有”选项卡。
40. 单击“添加”。
41. 选择“交易金额”
42. 在名为“字段”的字段中，输入或选择一个值。
43. 在“汇总功能”字段中，选择“合计”。
44. 在“条件”字段中，键入“>2000”。
45. 单击“确定”。
46. 单击“测试”。
47. 在“文档选择开始日期”字段，输入日期和时间。
48. 在“文档选择结束日期”字段，输入日期和时间。
49. 单击“运行测试”。
50. 在操作窗格上，单击“审计政策”。
51. 单击“附加选项”。
52. 在“开始日期”字段中，输入日期和时间。
53. 在“结束日期”字段中，输入日期和时间。
54. 单击“批处理”。
55. 展开“后台运行”部分。
56. 在“批处理”字段中选择“是”。
57. 单击“确定”。
58. 转至“审计工作台”>“审计案例”。
59. 在列表中，找到并选择所需记录。
60. 在列表中，单击所选行中的链接。
61. 展开“关联”部分。
62. 在列表中，找到并选择所需记录。
63. 在列表中，单击所选行中的链接。

