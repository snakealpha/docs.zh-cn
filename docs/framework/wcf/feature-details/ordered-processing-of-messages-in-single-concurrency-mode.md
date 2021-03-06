---
title: "单并发模式中的有序消息处理"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: a90f5662-a796-46cd-ae33-30a4072838af
caps.latest.revision: "2"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 4c677ed869c0e5dd0df1288de48668ba403df5aa
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/02/2017
---
# <a name="ordered-processing-of-messages-in-single-concurrency-mode"></a>单并发模式中的有序消息处理
WCF 可使消息的处理顺序无法保证，除非基础通道是会话。  例如，使用 MsmqInputChannel，不是会话通道，WCF 服务将无法按顺序处理信息。 有某些情况下，其中开发人员可能想在订单处理行为，但不是想使用会话。 本主题介绍在单一并发模式中运行服务时，如何配置这种行为。  
  
## <a name="in-order-message-processing"></a>有序消息处理  
 名为 <xref:System.ServiceModel.ServiceBehaviorAttribute.EnsureOrderedDispatch%2A> 的新特性已添加到 <xref:System.ServiceModel.ServiceBehaviorAttribute>。 当 <xref:System.ServiceModel.ServiceBehaviorAttribute.EnsureOrderedDispatch%2A> 设置为 true 并且<xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A> 设置为 <xref:System.ServiceModel.ConcurrencyMode.Single> 时，将按顺序处理发送到服务的消息。 下面的代码段演示如何设置这些特性。  
  
```  
[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Single, EnsureOrderedDispatch = true )]  
    class Service : IService  
    {  
         // ...  
    }  
```  
  
 如果 <xref:System.ServiceModel.ServiceBehaviorAttribute.ConcurrencyMode%2A> 设置为任何其他值，则引发 <xref:System.InvalidOperationException>。  
  
## <a name="see-also"></a>另请参阅  
 [会话，实例化和并发](../../../../docs/framework/wcf/feature-details/sessions-instancing-and-concurrency.md)  
 [并发](../../../../docs/framework/wcf/samples/concurrency.md)
