---
title: "引用完整性约束"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 3d3ba44b-4302-40d8-a7a9-62932e0395e5
caps.latest.revision: "3"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: 10e469838073b4cf1faba1704b88b47f30b8b3d0
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="referential-integrity-constraint"></a>引用完整性约束
A*引用完整性约束*实体数据模型 (EDM) 中是类似于关系数据库中的引用完整性约束。 与数据库表中一列 （或多） 可以引用另一个表的主键相同的方式[属性](../../../../docs/framework/data/adonet/property.md)（或属性） 的[实体类型](../../../../docs/framework/data/adonet/entity-type.md)可以引用[实体键](../../../../docs/framework/data/adonet/entity-key.md)另一个实体类型。 引用的实体类型称为*主体端*的约束。 引用主体端的实体类型称为*依赖端*的约束。  
  
 引用完整性约束定义的一部分[关联](../../../../docs/framework/data/adonet/association-type.md)两个实体类型之间。 引用完整性约束的定义指定了以下信息：  
  
-   约束的主体端。 （一个实体类型，其实体键由依赖端引用。）  
  
-   主体端的实体键。  
  
-   约束的依赖端。 （一个实体类型，它的一个或多个属性引用主体端的实体键。）  
  
-   依赖端的一个或多个引用属性。  
  
 EDM 中的引用完整性约束的用途是确保始终存在有效关联。 有关详细信息，请参阅[外键属性](../../../../docs/framework/data/adonet/foreign-key-property.md)。  
  
## <a name="example"></a>示例  
 下图显示了一个具有两个关联的概念模型：`WrittenBy` 和 `PublishedBy`。 `Book` 实体类型有一个属性 `PublisherId`，当您为 `Publisher` 关联定义一个引用完整性约束时，它将引用 `PublishedBy` 实体类型的实体键。  
  
 ![RefConstraintModel](../../../../docs/framework/data/adonet/media/refconstraintmodel.gif "RefConstraintModel")  
  
 [ADO.NET 实体框架](../../../../docs/framework/data/adonet/ef/index.md)使用域特定语言 (DSL) 称为概念架构定义语言 ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) 来定义概念模型。 下面的 CSDL 为上图所示的概念模型中的 `PublishedBy` 关联定义了一个引用完整性约束。  
  
 [!code-xml[EDM_Example_Model#RefConstraint](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books4.edmx#refconstraint)]  
  
## <a name="see-also"></a>另请参阅  
 [实体数据模型关键概念](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)  
 [实体数据模型](../../../../docs/framework/data/adonet/entity-data-model.md)
