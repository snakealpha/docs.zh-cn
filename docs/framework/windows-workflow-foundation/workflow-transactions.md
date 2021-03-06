---
title: "工作流事务"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 6081fb02-c0f2-483d-97b8-f3b7dc03011d
caps.latest.revision: "14"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: dba6762017877824308608bc58f80aed71ca9f21
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/02/2017
---
# <a name="workflow-transactions"></a>工作流事务
[!INCLUDE[wf1](../../../includes/wf1-md.md)] 支持通过使用 <xref:System.Transactions> 活动确定事务处理工作单元的范围来参与 <xref:System.Activities.Statements.TransactionScope> 事务。 尽管必须显式完成 <xref:System.Transactions.TransactionScope?displayProperty=nameWithType>，但 <xref:System.Activities.Statements.TransactionScope?displayProperty=nameWithType> 活动在成功完成后将对事务隐式调用完成。 <xref:System.Activities.Statements.TransactionScope.Body%2A> 活动的 <xref:System.Activities.Statements.TransactionScope> 中包含的所有活动都会参与该事务。 通过使用 <xref:System.ServiceModel.Activities.TransactedReceiveScope> 活动，WF 可以使事务流入某个工作流中。 与 <xref:System.Activities.Statements.TransactionScope> 活动一样，<xref:System.ServiceModel.Activities.TransactedReceiveScope.Body%2A> 中包含的所有活动都会参与该事务。 WF 确保依赖于 <xref:System.Transactions.Transaction.Current%2A?displayProperty=nameWithType> 的活动使用 <xref:System.Activities.Statements.TransactionScope> 和 <xref:System.ServiceModel.Activities.TransactedReceiveScope>。 如果系统提供的活动无法满足所有需求，可以使用 <xref:System.Activities.RuntimeTransactionHandle> 生成自定义活动，以便支持高级流控制和事务控制方案。  
  
 在下面的示例，摘自[基本 TransactionScope](../../../docs/framework/windows-workflow-foundation/samples/basic-transactionscope.md)示例构造一个工作流是组成<xref:System.Activities.Statements.Sequence>活动包含子活动包括<xref:System.Activities.Statements.TransactionScope>活动。 <xref:System.Activities.Statements.TransactionScope.Body%2A> 的 <xref:System.Activities.Statements.TransactionScope> 活动在 <xref:System.Activities.Statements.TransactionScope> 活动初始化的事务下执行。  
  
```csharp  
static Activity ScenarioOne()  
{  
    return new Sequence  
    {  
        Activities =  
        {  
            new WriteLine { Text = "    Begin workflow" },  
  
            new TransactionScope  
            {  
                Body = new Sequence  
                {  
                    Activities =   
                    {  
                        new WriteLine { Text = "    Begin TransactionScope" },  
  
                        new PrintTransactionId(),  
  
                        new TransactionScopeTest(),  
  
                        new WriteLine { Text = "    End TransactionScope" },  
                    },  
                },  
            },  
  
            new WriteLine { Text = "    End workflow" },  
        }  
    };  
}  
```  
  
 [!INCLUDE[crdefault](../../../includes/crdefault-md.md)]基本[事务](../../../docs/framework/windows-workflow-foundation/samples/transactions.md)示例和基于方案[事务](../../../docs/framework/windows-workflow-foundation/samples/transactions.md)示例。 [!INCLUDE[crdefault](../../../includes/crdefault-md.md)]有关使用<xref:System.ServiceModel.Activities.TransactedReceiveScope>，请参阅[流动的事务流入和流出工作流服务](../../../docs/framework/wcf/feature-details/flowing-transactions-into-and-out-of-workflow-services.md)。  
  
## <a name="see-also"></a>另请参阅  
 <xref:System.Activities.Statements.TransactionScope>  
 <xref:System.Transactions.TransactionScope>  
 <xref:System.Transactions.Transaction.Current%2A?displayProperty=nameWithType>
