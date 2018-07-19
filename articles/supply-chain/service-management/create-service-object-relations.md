---
title: "创建服务对象关系"
description: "本主题介绍如何为服务协议和服务订单创建服务对象关系。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c27070436139f784af690900a3f1ab108a809d03
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-object-relations"></a><span data-ttu-id="8b9ca-103">创建服务对象关系</span><span class="sxs-lookup"><span data-stu-id="8b9ca-103">Create service object relations</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8b9ca-104">本主题介绍如何为服务协议和服务订单创建服务对象关系。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-104">This topic describes how to create service object relations for a service agreement and a service order.</span></span> <span data-ttu-id="8b9ca-105">在您创建服务对象关系时，将服务对象关联到服务协议或服务订单。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-105">When you a create service object relation, you associate the service object to a service agreement or service order.</span></span> <span data-ttu-id="8b9ca-106">当客户针对作为服务对象的物料请求服务时，您可以从服务对象关系列表中选择服务对象。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-106">When a customer requests service for an item that is a service object, you can select the service object from the list of service object relations.</span></span>

## <a name="create-a-service-object-relation-for-a-service-agreement"></a><span data-ttu-id="8b9ca-107">为服务协议创建服务对象关系</span><span class="sxs-lookup"><span data-stu-id="8b9ca-107">Create a service object relation for a service agreement</span></span>

<span data-ttu-id="8b9ca-108">使用以下步骤来为服务协议创建服务对象关系：</span><span class="sxs-lookup"><span data-stu-id="8b9ca-108">Use the following steps to create a service object relation for a service agreement:</span></span>

1.  <span data-ttu-id="8b9ca-109">单击**服务管理** \> **常用** \> **服务协议** \> **服务协议**。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-109">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="8b9ca-110">在**服务协议**列表中，选择某一现有服务协议，或单击**新建**来创建新服务协议。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-110">In the **Service agreements** list, select an existing service agreement, or click **New** to create a new service agreement.</span></span>

3.  <span data-ttu-id="8b9ca-111">在**服务协议**窗体**操作窗格**，**服务协议**选项卡**关系**组中，单击**服务对象**。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-111">In the **Service agreements** form, on the **Action Pane**, on the **Service agreement** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="8b9ca-112">在**服务对象**窗体中，单击**新建**，然后为该服务协议选择服务对象。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-112">In the **Service objects** form, click **New**, and then select a service object for this service agreement.</span></span>

5.  <span data-ttu-id="8b9ca-113">要将模板物料清单物料 (BOM) 分配到服务协议，请单击**功能**，然后选择 **附加物料清单模板**。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-113">To assign a template bill of materials (BOM) to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="8b9ca-114">在**选择物料清单模板**窗体的**物料清单模板**字段中，选择一个模板。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-114">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 

## <a name="create-a-service-object-relation-for-a-service-order"></a><span data-ttu-id="8b9ca-115">为服务订单创建服务对象关系</span><span class="sxs-lookup"><span data-stu-id="8b9ca-115">Create a service object relation for a service order</span></span>

<span data-ttu-id="8b9ca-116">使用以下步骤来为服务订单创建服务对象关系：</span><span class="sxs-lookup"><span data-stu-id="8b9ca-116">Use the following steps to create a service object relation for a service order:</span></span>

1.  <span data-ttu-id="8b9ca-117">单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-117">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="8b9ca-118">在**服务订单**列表中，选择某一现有服务订单，或创建新服务订单。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-118">In the **Service orders** list, select an existing service order, or create a new service order.</span></span>

3.  <span data-ttu-id="8b9ca-119">在**服务订单**窗体**操作窗格**，**服务订单**选项卡**关系**组中，单击**服务对象**。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-119">In the **Service orders** form, on the **Action Pane**, on the **Service order** tab, in the **Relations** group, click **Service objects**.</span></span>

4.  <span data-ttu-id="8b9ca-120">在**服务对象**窗体中，单击**新建**，然后为该服务订单选择服务对象。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-120">In the **Service objects** form, click **New**, and then select a service object for this service order.</span></span>

5.  <span data-ttu-id="8b9ca-121">要将物料清单模板分配到服务协议，请单击**功能**，然后选择 **附加物料清单模板**。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-121">To assign a template BOM to the service agreement, click **Functions**, and then select **Attach template BOM**.</span></span> <span data-ttu-id="8b9ca-122">在**选择物料清单模板**窗体的**物料清单模板**字段中，选择一个模板。</span><span class="sxs-lookup"><span data-stu-id="8b9ca-122">In the **Select template BOM** form, in the **Template BOM** field, select a template.</span></span> 


## <a name="see-also"></a><span data-ttu-id="8b9ca-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="8b9ca-123">See also</span></span>

[<span data-ttu-id="8b9ca-124">服务对象</span><span class="sxs-lookup"><span data-stu-id="8b9ca-124">Service objects</span></span>](service-objects.md)

[<span data-ttu-id="8b9ca-125">服务对象关系</span><span class="sxs-lookup"><span data-stu-id="8b9ca-125">service object relations</span></span>](service-object-relations.md)

[<span data-ttu-id="8b9ca-126">物料清单模板</span><span class="sxs-lookup"><span data-stu-id="8b9ca-126">Template BOMs</span></span>](template-boms.md)

  


