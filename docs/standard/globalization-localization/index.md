---
title: "对 .NET Framework 应用程序进行全球化和本地化"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- international applications [.NET Framework]
- globalization [.NET Framework], encoding
- global applications
- internationalization
- world-ready applications
- application development [.NET Framework], globalization
- multilingual application development
ms.assetid: 9a59696b-d89b-45bd-946d-c75da4732d02
caps.latest.revision: "42"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 3f6beb720819a1be4e45bf4cefac3d805d7ee5e7
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="globalizing-and-localizing-net-framework-applications"></a>对 .NET Framework 应用程序进行全球化和本地化
开发[全球通用的应用程序](http://msdn.microsoft.com/goglobal/bb978433.aspx)（包括可本地化为一种或多种语言的应用程序）分为三步：全球化、可本地化性审核和本地化。  
  
 [全球化](../../../docs/standard/globalization-localization/globalization.md)  
 此步骤包括设计和编码非特定区域性和非特定语言的应用程序，以及设计和编码支持所有用户的本地化用户界面和区域数据的应用程序。 它涉及做出不基于区域性特定的假设的设计和编程决策。 虽然全球化应用程序未本地化，但它经过设计和编写，因此随后可相对容易地将其本地化为一种或多种语言。  
  
 [可本地化性审核](../../../docs/standard/globalization-localization/localizability-review.md)  
 此步骤包括评审应用程序的代码和设计，以确保能轻松本地化应用程序和标识本地化的潜在障碍，并验证应用程序的可执行代码是否与其资源分隔开。 如果全球化阶段有效，则本地化检查将确认全球化过程中做出的设计和编码选择。 本地化阶段还可以标识任何遗留问题，以便在本地化阶段不必修改应用程序的源代码。  
  
 [本地化](../../../docs/standard/globalization-localization/localization.md)  
 此步骤包括为特定区域性或区域自定义应用程序。 如果已正确执行全球化和本地化分析这两个步骤，则本地化主要包括用户界面的翻译。  
  
 遵循这三个步骤有两大好处：  
  
-   让你无需改进为支持单个区域性（如美国英语）而专门设计的应用程序以支持其他区域性。英语，以支持其他区域性。  
  
-   这会产生更加稳定并有少量 Bug 的本地化应用程序。  
  
 .NET Framework 为开发全球通用和本地化的应用程序提供了广泛支持。 特别是，.NET Framework 类库中许多类成员通过返回可反映当前用户区域性或指定区域性约定的值来帮助全球化。 此外，.NET Framework 支持附属程序集，这可推动本地化应用程序的过程。  
  
 有关详细信息，请访问 [Go Global 开发人员中心](http://go.microsoft.com/fwlink/?LinkId=235015)。  
  
## <a name="in-this-section"></a>本节内容  
 [全球化](../../../docs/standard/globalization-localization/globalization.md)  
 讨论创建全球通用的应用程序的第一个阶段，该阶段包括设计和编码为非特定区域性和非特定语言的应用程序。  
  
 [可本地化性审核](../../../docs/standard/globalization-localization/localizability-review.md)  
 讨论创建本地化应用程序的第二个阶段，该阶段包含标识本地化的潜在路障。  
  
 [本地化](../../../docs/standard/globalization-localization/localization.md)  
 讨论创建本地化应用程序的最后阶段，该阶段包含自定义应用程序的特定区域或区域性的用户界面。  
  
 [不区分区域性的字符串操作](../../../docs/standard/globalization-localization/culture-insensitive-string-operations.md)  
 描述默认情况下如何使用区分区域性的 .NET Framework 方法和类来获得不区分区域性的结果。  
  
 [开发全球通用应用程序的最佳做法](../../../docs/standard/globalization-localization/best-practices-for-developing-world-ready-apps.md)  
 描述在全球化、本地化和开发全球通用的 ASP.NET 应用程序时遵循的最佳做法。  
  
## <a name="reference"></a>参考  
 <xref:System.Globalization?displayProperty=nameWithType> 命名空间  
 包含定义区域性相关信息的类，这些信息包括语言、国家/地区、正在使用的日历、日期的格式模式、货币、数字以及字符串的排序顺序。  
  
 <xref:System.Resources> 命名空间  
 提供用于创建、操作和使用资源的类。  
  
 <xref:System.Text> 命名空间  
 包含表示 ASCII、ANSI、Unicode 以及其他字符编码的类。  
  
 [Resgen.exe（资源文件生成器）](../../../docs/framework/tools/resgen-exe-resource-file-generator.md)  
 描述如何使用 Resgen.exe 将 .txt 文件和基于 XML 的资源格式 (.resx) 文件转换为公共语言运行时二进制 .resources 文件。  
  
 [Winres.exe（Windows 窗体资源编辑器）](../../../docs/framework/tools/winres-exe-windows-forms-resource-editor.md)  
 描述如何使用 Winres.exe 本地化 Windows 窗体。
