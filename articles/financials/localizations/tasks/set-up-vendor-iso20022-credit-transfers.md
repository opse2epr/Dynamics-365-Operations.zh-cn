--- 
title: "设置 ISO20022 贷方转帐的供应商及供应商银行帐户"
description: "此过程可以演示如何设置供应商及其所需的特定银行帐户信息以生成 ISO20022 贷方转帐或其他任何供应商付款文件。"
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
ms.openlocfilehash: 147d8fa82bf15c984ad263cada42789038fa7371
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>设置 ISO20022 贷方转帐的供应商及供应商银行帐户

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程可以演示如何设置供应商及其所需的特定银行帐户信息以生成 ISO20022 贷方转帐或其他任何供应商付款文件。 

用于创建此过程的演示数据公司是 DEMF。
这是五个用于演示使用电子申报配置的供应商付款流程的流程中的第四个。 此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。


## <a name="set-up-bank-details"></a>设置银行详情
1. 转到“应付帐款”>“供应商”>“所有供应商”。
2. 使用“快速筛选器”以查找记录。 例如，在“供应商帐户”字段中筛选“DE-001”数值。
3. 单击 DE-001 以打开供应商详细信息。
4. 在“操作窗格”上，单击“供应商”。
5. 单击“银行帐户”。
6. 单击“编辑”。
    * 如果没有可用的银行帐户，您需要创建一个新帐户。  
7. 在“SWIFT 代码”字段中，键入 'COBADEFFXXX'。
8. 在 'IBAN' 字段中，键入 'DE36200400000628808808'。
9. 关闭该页面。

## <a name="set-up-a-method-of-payment-for-the-vendor"></a>为供应商设置付款方式
1. 单击“编辑”。
2. 展开或收拢付款窗口。
3. 在“付款方式”字段中，单击下拉按钮以打开查找。
4. 在列表中，单击 SEPA CT 行中的链接。
5. 单击“保存”。

