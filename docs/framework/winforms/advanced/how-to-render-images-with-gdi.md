---
title: "如何：使用 GDI+ 呈现图像"
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
helpviewer_keywords:
- images [Windows Forms], creating
- GDI+, rendering existing images
ms.assetid: c128b79a-3e31-47d8-9e66-3470f570a056
caps.latest.revision: "12"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 9c0b4c128667cab04ca8ed015b44dae60d11b474
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-render-images-with-gdi"></a>如何：使用 GDI+ 呈现图像
可在应用程序中使用 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] 呈现以文件形式存在的图像。 执行此操作通过创建的新对象<xref:System.Drawing.Image>类 (如<xref:System.Drawing.Bitmap>)，则创建<xref:System.Drawing.Graphics>对象来引用所需的绘图图面的和调用<xref:System.Drawing.Graphics.DrawImage%2A>方法<xref:System.Drawing.Graphics>对象。 将在图形类所表示的绘图表面上绘制图像。 可在设计时使用图像编辑器创建和编辑图像文件，而在运行时使用 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] 呈现图像。 有关详细信息，请参阅[图标的图像编辑器](/cpp/windows/image-editor-for-icons)。  
  
### <a name="to-render-an-image-with-gdi"></a>使用 GDI+ 呈现图像  
  
1.  创建一个对象，该对象表示要显示的图像。 此对象必须是继承自的类成员<xref:System.Drawing.Image>，如<xref:System.Drawing.Bitmap>或<xref:System.Drawing.Imaging.Metafile>。 下面显示了一个示例：  
  
    ```vb  
    ' Uses the System.Environment.GetFolderPath to get the path to the   
    ' current user's MyPictures folder.  
    Dim myBitmap as New Bitmap _  
       (System.Environment.GetFolderPath _  
          (System.Environment.SpecialFolder.MyPictures))  
    ```  
  
    ```csharp  
    // Uses the System.Environment.GetFolderPath to get the path to the   
    // current user's MyPictures folder.  
    Bitmap myBitmap = new Bitmap  
       (System.Environment.GetFolderPath  
          (System.Environment.SpecialFolder.MyPictures));  
    ```  
  
    ```cpp  
    // Uses the System.Environment.GetFolderPath to get the path to the   
    // current user's MyPictures folder.  
    Bitmap^ myBitmap = gcnew Bitmap  
       (System::Environment::GetFolderPath  
          (System::Environment::SpecialFolder::MyPictures));  
    ```  
  
2.  创建<xref:System.Drawing.Graphics>对象，表示你想要使用的绘图图面。 有关详细信息，请参阅[如何：创建用于绘制的 Graphics 对象](../../../../docs/framework/winforms/advanced/how-to-create-graphics-objects-for-drawing.md)。  
  
    ```vb  
    ' Creates a Graphics object that represents the drawing surface of   
    ' Button1.  
    Dim g as Graphics = Button1.CreateGraphics  
    ```  
  
    ```csharp  
    // Creates a Graphics object that represents the drawing surface of   
    // Button1.  
    Graphics g = Button1.CreateGraphics();  
    ```  
  
    ```cpp  
    // Creates a Graphics object that represents the drawing surface of   
    // Button1.  
    Graphics^ g = button1->CreateGraphics();  
    ```  
  
3.  调用<xref:System.Drawing.Graphics.DrawImage%2A>的图形对象呈现图像。 必须同时指定要绘制的图像以及将绘制它的位置坐标。  
  
    ```vb  
    g.DrawImage(myBitmap, 1, 1)  
    ```  
  
    ```csharp  
    g.DrawImage(myBitmap, 1, 1);  
    ```  
  
    ```cpp  
    g->DrawImage(myBitmap, 1, 1);  
    ```  
  
## <a name="see-also"></a>另请参阅  
 [图形编程入门](../../../../docs/framework/winforms/advanced/getting-started-with-graphics-programming.md)  
 [如何：创建用于绘制的图形对象](../../../../docs/framework/winforms/advanced/how-to-create-graphics-objects-for-drawing.md)  
 [GDI+ 中的笔、直线和矩形](../../../../docs/framework/winforms/advanced/pens-lines-and-rectangles-in-gdi.md)  
 [如何：在 Windows 窗体上绘制文本](../../../../docs/framework/winforms/advanced/how-to-draw-text-on-a-windows-form.md)  
 [Windows 窗体中的图形和绘制](../../../../docs/framework/winforms/advanced/graphics-and-drawing-in-windows-forms.md)  
 [绘制线条或闭合的图形](/cpp/windows/drawing-lines-or-closed-figures-image-editor-for-icons)  
 [图标的图像编辑器](/cpp/windows/image-editor-for-icons)
