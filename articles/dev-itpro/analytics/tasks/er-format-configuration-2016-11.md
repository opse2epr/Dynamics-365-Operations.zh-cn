--- 
title: "针对电子申报 (ER) 创建格式配置"
description: "以下步骤说明属于系统管理员或电子报表开发人员的用户如何创建电子报表 (ER) 的格式配置。"
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c46b222cb12d0432609c47f89afc522e02c41ab6
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a>针对电子申报 (ER) 创建格式配置

[!include[task guide banner](../../includes/task-guide-banner.md)]

以下步骤说明属于系统管理员或电子报表开发人员的用户如何创建电子报表 (ER) 的格式配置。 此格式配置定义用于处理付款的电子单据的格式。 为了完成这些步骤，您首先必须完成“映射模型到所选数据源”这一过程中的步骤。


## <a name="create-a-new-format-configuration"></a>创建新的格式配置
1. 转到“组织管理”>“工作区”>“电子申报”。
2. 单击“申报配置”。
3. 在树结构中，选择“付款（简化模型）”。
4. 单击“创建配置”，以打开下拉对话框。
5. 在“新建”字段中，输入“基于数据模型付款模型的格式”。
6. 在“名称”字段中，键入“银行自动对帐系统（英国虚构）”。
    * 银行自动对帐系统（英国虚构）  
7. 在“描述”字段中，键入“银行自动对帐系统供应商付款格式（英国虚拟）”。
    * 银行自动对帐系统供应商付款格式（英国虚构）  
    * 有效配置提供商将自动在此输入。 此提供商可以维护此配置。 其他提供商可以使用此配置，但不能对其进行维护。  
    * 电子文档的特定格式可进行定义。 如果您想要选择运行时间的格式，则将此字段保留为空。  
8. 在“数据模型定义”字段中，输入或选择一个值。
9. 单击“创建配置”。
    * 已创建新的配置。 草稿版本可用于存储用于管理电子文档的设计格式。  

## <a name="design-format-of-electronic-document"></a>设计电子单据的格式
1. 单击“设计器”。
2. 单击“添加根”以打开下拉对话框。
3. 在树结构中，选择“常见\文件”。
4. 在“名称”字段中，键入“Xml”。
    * Xml  
5. 在“编码”字段中，键入“UTF-8”。
    * UTF-8  
6. 单击“确定”。
7. 单击“添加”以打开下拉对话框。
8. 在树结构中，选择“XML\元素”。
9. 在“名称”字段中，键入“消息”。
    * 消息  
10. 单击“确定”。
11. 在树结构中，选择“Xml\消息”。
12. 单击“添加元素”。
13. 在“名称”字段中，键入“处理日期”。
    * 处理日期  
14. 单击“确定”。
15. 单击“添加元素”。
16. 在“名称”字段中，键入“消息 ID”。
    * 消息标识  
17. 单击“确定”。
18. 单击“添加元素”。
19. 在“名称”字段中，键入“付款”。
    * 付款  
20. 单击“确定”。
21. 在树结构中，选择“Xml\消息\付款”。
22. 单击“添加元素”。
23. 在“名称”字段中，键入“物料”。
    * 项目  
24. 单击“确定”。
25. 在树结构中，选择“Xml\消息\付款\项”。
26. 单击“添加”以打开下拉对话框。
27. 在树结构中，选择“Xml：文件\属性”。
28. 在“名称”字段中，键入“ID”。
    * ID  
29. 单击“确定”。
30. 单击“添加”以打开下拉对话框。
31. 在树结构中，选择“XML\元素”。
32. 在“名称”字段中，键入“供应商”。
    * 供应商  
33. 单击“确定”。
34. 在树结构中，选择“Xml\消息\付款\项\供应商”。
35. 单击“添加元素”。
36. 在“名称”字段中，键入“名称”。
    * 姓名  
37. 单击“确定”。
38. 单击“添加元素”。
39. 在“名称”字段中，键入“银行”。
    * 银行  
40. 单击“确定”。
41. 在树结构中，选择“Xml\消息\付款\项\供应商\银行”。
42. 单击“添加元素”。
43. 在“名称”字段中，键入“银行代号”。
    * 银行代号  
44. 单击“确定”。
45. 单击“添加元素”。
46. 在“名称”字段中，键入“帐号”。
    * 帐号  
47. 单击“确定”。
48. 在树结构中，选择“Xml\消息\付款\项\供应商”。
49. 单击“复制”。
50. 在树结构中，选择“Xml\消息\付款\项”。
51. 单击“粘贴”。
52. 在“名称”字段中，键入“付款人”。
    * 付款人  
53. 在树结构中，选择“Xml\消息\付款\项”。
54. 单击“添加元素”。
55. 在“名称”字段中，键入“货币”。
    * 币种  
56. 单击“确定”。
57. 单击“添加元素”。
58. 在“名称”字段中，键入“描述”。
    * 说明  
59. 单击“确定”。
60. 单击“添加元素”。
61. 在“名称”字段中，键入“交易日期”。
    * 交易日期  
62. 单击“确定”。
63. 单击“添加元素”。
64. 在“名称”字段中，键入“金额”。
    * 本币金额  
65. 单击“确定”。

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>准备映射到数据模型元素的格式部分
1. 在树结构中，选择“Xml\消息\处理日期”。
2. 单击“添加”以打开下拉对话框。
3. 在树结构中，选择“文本'日期时间”。
4. 在“格式”字段中，键入“年-月-日”。
    * yyyy-MM-dd  
5. 单击“确定”。
6. 在树结构中，选择“Xml\消息\付款\项\交易日期”。
7. 单击"添加日期时间"。
8. 在“格式”字段中，键入“年-月-日”。
    * yyyy-MM-dd  
9. 在“日期时间类型”字段中，选择“日期”。
10. 单击“确定”。
11. 在树结构中，选择“Xml\消息\消息标识”。
12. 单击“添加”以打开下拉对话框。
13. 在树结构中，选择“文本\字符串”。
14. 单击“确定”。
15. 在树结构中，选择“Xml\消息\付款\项\供应商\名称”。
16. 单击“添加字符串”。
17. 单击“确定”。
18. 在树结构中，选择“Xml\消息\付款\项\供应商\银行\银行代号”。
19. 单击“添加字符串”。
20. 单击“确定”。
21. 在树结构中，选择“Xml\消息\付款\项\供应商\银行\帐号”。
22. 单击“添加字符串”。
23. 单击“确定”。
24. 在树结构中，选择“Xml\消息\付款\项\付款人\名称”。
25. 单击“添加字符串”。
26. 单击“确定”。
27. 在树结构中，选择“Xml\消息\付款\项\付款人\银行\银行代号”。
28. 单击“添加字符串”。
29. 单击“确定”。
30. 在树结构中，选择“Xml\消息\付款\项\付款人\银行\帐号”。
31. 单击“添加字符串”。
32. 单击“确定”。
33. 在树结构中，选择“Xml\消息\付款\项\货币”。
34. 单击“添加字符串”。
35. 单击“确定”。
36. 在树结构中，选择“Xml\消息\付款\项\描述”。
37. 单击“添加字符串”。
38. 单击“确定”。
39. 在树结构中，选择“Xml\消息\付款\项\金额”。
40. 单击“添加字符串”。
41. 单击“确定”。
42. 单击“保存”。
43. 关闭该页面。

