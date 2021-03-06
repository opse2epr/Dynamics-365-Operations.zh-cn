---
title: 取消服务订单
description: 您可以取消某一服务订单或从服务订单本身中取消服务订单行，或者您可以通过运行定期作业来取消多个服务订单。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1495fa139ea2c3cb7f2450b402126822f5549f60
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546586"
---
# <a name="cancel-service-orders"></a>取消服务订单   

[!include [banner](../includes/banner.md)]


您可以取消某一服务订单或从服务订单本身中取消服务订单行，或者您可以通过运行定期作业来取消多个服务订单。


> [!NOTE]
> <P>在以下情况下不能取消服务订单：服务订单的阶段不允许取消，服务订单具有物料需求，或者服务订单已过帐。</P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a>在“服务订单”窗体中取消服务订单

1.  单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。 选择服务订单，然后在操作窗格上单击**取消订单**。

## <a name="cancel-a-service-order-line"></a>取消服务订单行

1.  单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。 双击包含要取消的服务订单。

2.  选择您想取消的服务订单行，然后单击**取消订单行**以将该行的状态更改为 **已取消**。


> [!TIP]
> <P>若要冲销服务订单行的取消并将状态更改回为<STRONG>已创建</STRONG> ，请单击<STRONG>撤消取消</STRONG>。</P>


## <a name="cancel-multiple-service-orders"></a>取消多个服务订单

1.  单击**服务管理** \> **定期** \> **服务订单** \> **取消服务订单**。

2.  单击**选择**按钮。

3.  在**查询**窗体的**条件**列中，选择您想要取消的服务订单。

4.  单击**确定**关闭**查询**窗体。

5.  选中**显示信息日志**复选框，以便生成列举已取消服务订单的信息日志。

6.  如果您想要撤消某一服务订单的**已取消**状态，则选中**撤消取消**复选框。

7.  单击**确定**。

取消已选服务订单，或它们的进度状态**已取消**已冲销为**进行中**。


> [!NOTE]
> <P>如果您选中了<STRONG>撤消取消</STRONG>复选框，将冲销进度状态为<STRONG>已取消</STRONG>的服务订单，而不会取消进度状态为<STRONG>进行中</STRONG>的服务订单。</P>


  


