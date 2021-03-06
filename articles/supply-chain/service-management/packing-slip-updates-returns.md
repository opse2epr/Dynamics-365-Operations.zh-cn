---
title: 退货的装箱单更新
description: 在退回物料可以入库前，它们所属于的订单的装箱单必须更新。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4aba61e6acf5fb959917da9ddea94c21fe1460d1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552876"
---
# <a name="packing-slip-updates-for-returns"></a>退货的装箱单更新  

[!include [banner](../includes/banner.md)]


在退回物料可以入库前，它们所属于的订单的装箱单必须更新。 就像发票更新流程是对财务交易记录进行的更新一样，装箱单更新流程是对库存记录的物理更新；这意味着它对库存进行更改。 在退货时，分配给处置操作的步骤在装箱单更新期间执行。

装箱单更新可通过物料到达日志或退货单进行处理。

作为过账装箱单的流程，可以选择将来自客户装运文档的装箱单参考编号与订单行相关联。 此关联可选和仅供参考。 它并不创建任何交易记录更新。

如果不是所有的预期退货物料都已到达，则应只包括在装箱单更新中接收的数量。 保留订单上的剩余物料，直至其余的退货装运已到达。

如果某一物料在经过检验后发送回装运和接收部门，例如，在检验人员不知道在库存中何处存储物料时，必须更新相应的装箱单，正确登记和操作指定为检验结果的处置代码。

在更新来自销售协议的退回物料的装箱单时，自动更新该物料的销售协议承诺反映数量或金额的变化。 

## <a name="see-also"></a>请参阅

[为退货执行发票更新](perform-invoice-updates-for-returns.md)

  


