---
title: "-unsafe（C# 编译器选项）"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
f1_keywords: /unsafe
helpviewer_keywords:
- -unsafe compiler option [C#]
- unsafe compiler option [C#]
- /unsafe compiler option [C#]
ms.assetid: fdb77ed9-da03-45bd-bb7f-250704da1bcc
caps.latest.revision: "19"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 146977522b400418a26f6a83e1a0ccdca8675bf9
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="unsafe-c-compiler-options"></a>/unsafe（C# 编译器选项）
/unsafe 编译器选项允许使用[不安全](../../../csharp/language-reference/keywords/unsafe.md)关键字进行编译的代码。  
  
## <a name="syntax"></a>语法  
  
```console  
/unsafe  
```  
  
## <a name="remarks"></a>备注  
 有关不安全代码的详细信息，请参阅[不安全代码和指针](../../../csharp/programming-guide/unsafe-code-pointers/index.md)。  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>在 Visual Studio 开发环境中设置此编译器选项  
  
1.  打开项目的“属性”页。  
  
2.  单击“生成”属性页。  
  
3.  选中“允许不安全代码”复选框。  
  
 有关如何以编程方式设置此编译器选项的信息，请参阅 <xref:VSLangProj80.CSharpProjectConfigurationProperties3.AllowUnsafeBlocks%2A>。  
  
## <a name="example"></a>示例  
 针对不安全模式编译 `in.cs`：  
  
```console  
csc /unsafe in.cs  
```  
  
## <a name="see-also"></a>另请参阅  
 [C# 编译器选项](../../../csharp/language-reference/compiler-options/index.md)  
 [管理项目和解决方案属性](/visualstudio/ide/managing-project-and-solution-properties)
