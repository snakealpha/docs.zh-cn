---
title: "如何：更改 Windows 窗体的边框"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords: Windows Forms, changing the borders
ms.assetid: b3d5fa56-80c6-4b10-b505-f9672307ed55
caps.latest.revision: "12"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 94c95d1d938ff8038f1057ac7648082819562b98
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-change-the-borders-of-windows-forms"></a>如何：更改 Windows 窗体的边框
当确定 Windows 窗体的外观和行为时，有几种边框样式可供选择。 通过更改 <xref:System.Windows.Forms.Form.FormBorderStyle%2A> 属性，可控制窗体调整大小的行为。 此外，设置 <xref:System.Windows.Forms.Form.FormBorderStyle%2A> 会影响标题栏的显示方式以及其上出现的按钮布局。 有关详细信息，请参阅<xref:System.Windows.Forms.FormBorderStyle>。  
  
 [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)] 中对此任务提供广泛支持。  
  
 另请参阅[如何： 更改使用设计器的 Windows 窗体的边框](http://msdn.microsoft.com/library/yettzh3e\(v=vs.110\))。  
  
### <a name="to-set-the-border-style-of-windows-forms-programmatically"></a>以编程方式设置 Windows 窗体的边框样式  
  
-   将 <xref:System.Windows.Forms.Form.FormBorderStyle%2A> 属性设置为所需的样式。 下面的代码示例设置窗体的边框样式`DlgBx1`到<xref:System.Windows.Forms.FormBorderStyle.FixedDialog>。  
  
    ```vb  
    DlgBx1.FormBorderStyle = System.Windows.Forms.FormBorderStyle.FixedDialog  
    ```  
  
    ```csharp  
    DlgBx1.FormBorderStyle = System.Windows.Forms.FormBorderStyle.FixedDialog;  
    ```  
  
    ```cpp  
    DlgBx1->FormBorderStyle =  
       System::Windows::Forms::FormBorderStyle::FixedDialog;  
    ```  
  
     另请参阅[如何： 在设计时创建对话框](http://msdn.microsoft.com/library/55cz5x2c\(v=vs.110\))。  
  
     此外，如果你已选择提供可选的窗体的边框样式**最小化**和**最大化**按钮，你可以指定是否希望任一或所有这些按钮正常工作。 当想要密切控制用户体验时，这些按钮会非常有用。 **最小化**和**最大化**按钮处于启用状态默认情况下，而且其功能操作通过**属性**窗口。  
  
## <a name="see-also"></a>另请参阅  
 <xref:System.Windows.Forms.FormBorderStyle>  
 <xref:System.Windows.Forms.FormBorderStyle.FixedDialog>  
 [Windows 窗体入门](../../../docs/framework/winforms/getting-started-with-windows-forms.md)
