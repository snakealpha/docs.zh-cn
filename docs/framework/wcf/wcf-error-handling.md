---
title: "WCF 错误处理"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 1e4b1e0f-9598-449d-9d73-90bda62305b8
caps.latest.revision: "3"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 26dfea83400b5d601fabc5cfb52bc71a4d5e4f6f
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/02/2017
---
# <a name="wcf-error-handling"></a>WCF 错误处理
WCF 应用程序遇到的错误属于下列三组中的一组：  
  
1.  通信错误  
  
2.  代理/通道错误  
  
3.  应用程序错误  
  
 网络不可用、客户端使用错误地址或服务主机未侦听传入消息时，会发生通信错误。 这种类型的错误将作为 <xref:System.ServiceModel.CommunicationException> 或 <xref:System.ServiceModel.CommunicationException> 派生的类返回到客户端。  
  
 代理/通道错误是通道或代理自身内部发生的错误。 这种类型的错误包括：尝试使用已关闭的代理或通道，客户端和服务之间存在协定不匹配，或者客户端凭据被服务拒绝。 此类别中存在许多不同类型的错误，错误太多，恕不在此列出。 这种类型的错误将按原样返回到客户端（不对异常对象执行任何转换）。  
  
 执行服务操作过程中发生应用程序错误。 这种类型的错误将作为 <xref:System.ServiceModel.FaultException> 或 <xref:System.ServiceModel.FaultException%601> 发送到客户端。  
  
 通过以下一种或多种方法执行 WCF 中的错误处理：  
  
-   直接处理引发的异常。 只能针对通信错误以及代理/通道错误执行此操作。  
  
-   使用错误协定  
  
-   实现 <xref:System.ServiceModel.Dispatcher.IErrorHandler> 接口  
  
-   处理 <xref:System.ServiceModel.ServiceHost> 事件  
  
## <a name="fault-contracts"></a>错误协定  
 利用错误协定，您可以独立于平台的方式定义服务操作期间会发生的错误。 默认情况下，所有从服务操作内引发的异常都将作为 <xref:System.ServiceModel.FaultException> 对象返回到客户端。 <xref:System.ServiceModel.FaultException> 对象将包含很少的信息。 通过定义错误协定并作为 <xref:System.ServiceModel.FaultException%601> 返回错误，可以控制发送到客户端的信息。 [!INCLUDE[crdefault](../../../includes/crdefault-md.md)][指定和处理在协定和服务中的错误](../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)。  
  
## <a name="ierrorhandler"></a>IErrorHandler  
 利用 <xref:System.ServiceModel.Dispatcher.IErrorHandler> 接口，您可以对 WCF 应用程序响应错误的方式进行更多的控制。  您可以完全控制返回到客户端的故障消息，还可以执行自定义错误处理，例如日志记录。  [!INCLUDE[crdefault](../../../includes/crabout-md.md)]<xref:System.ServiceModel.Dispatcher.IErrorHandler>和[扩展对错误处理和报告的控制](../../../docs/framework/wcf/samples/extending-control-over-error-handling-and-reporting.md)  
  
## <a name="servicehost-events"></a>ServiceHost 事件  
 <xref:System.ServiceModel.ServiceHost> 类承载服务，并定义处理错误可能需要的几个事件。 例如:   
  
1.  <!--zz <xref:System.ServiceModel.ServiceHost.Faulted>-->  `System.ServiceModel.ServiceHost.Faulted`
  
2. <!--zz  <xref:System.ServiceModel.ServiceHost.UnknownMessageReceived>  --> `System.ServiceModel.ServiceHost.UnknownMessageReceived`
  
 [!INCLUDE[crdefault](../../../includes/crdefault-md.md)] <xref:System.ServiceModel.ServiceHost>
