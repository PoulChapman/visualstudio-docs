---
title: "Accessibility in Office Projects | Microsoft Docs"
ms.custom: ""
ms.date: "02/02/2017"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "office-development"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
helpviewer_keywords: 
  - "Office development in Visual Studio, accessibility"
  - "shortcut keys [Office development in Visual Studio]"
  - "Ribbon [Office development in Visual Studio], shortcut keys"
  - "accessibility [Office development in Visual Studio]"
ms.assetid: 48efcf1f-ca49-47ce-99f0-cc99f051aeae
caps.latest.revision: 24
author: "kempb"
ms.author: "kempb"
manager: "ghogen"
---
# Accessibility in Office Projects
  Microsoft Visual Studio and Microsoft Office include many accessibility features that enable you to build custom solutions that meet standard accessibility requirements. Microsoft publishes guidelines for accessibility on the Web. For details, see the [Accessibility Web site](http://go.microsoft.com/fwlink/?LinkID=37113).  
  
 In most cases, Office projects in Visual Studio meet accessibility standards or exposes properties that you can set to make your solutions accessible. However, there are some features that have limited accessibility.  
  
 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]  
  
## Accessibility at Design Time  
  
### Using Shortcut Keys in Document-Level Projects  
 When a Microsoft Office Word document or a Microsoft Office Excel workbook is open in Visual Studio, only one application at a time receives the shortcut key commands. By default, Visual Studio receives all shortcut key commands, but you can make Word or Excel receive them when the document has focus by selecting **Dynamic keyboard scheme** on the **Keyboard Settings** page of the **Options** dialog box. For more information, see [Microsoft Office Word Keyboard, Microsoft Office Keyboard Settings, Options Dialog Box](../vsto/microsoft-office-word-keyboard-microsoft-office-keyboard-settings-options-dialog-box.md) and [Microsoft Office Excel Keyboard, Microsoft Office Keyboard Settings, Options Dialog Box](../vsto/microsoft-office-excel-keyboard-microsoft-office-keyboard-settings-options-dialog-box.md).  
  
### Displaying Shortcut Keys for the Ribbon in Document-Level Projects  
 When a Word document or an Excel workbook is open in Visual Studio, you cannot press the Alt key to view shortcut keys for the tabs and controls on the Ribbon. To view the shortcut keys while the document or workbook is open in the designer, perform the following steps.  
  
##### To view shortcut keys for Ribbon tabs and controls in the designer  
  
1.  In Visual Studio, on the **Tools** menu, click **Options**.  
  
2.  Expand the **Office Tools** node, and select **Microsoft Office Excel Keyboard** or **Microsoft Office Word Keyboard**, as appropriate.  
  
3.  Select **Dynamic keyboard scheme**.  
  
     A message appears that states that you must restart Visual Studio for the change to take effect.  
  
4.  Click **OK**.  
  
5.  Restart Visual Studio, and reopen your project.  
  
6.  Open the document or workbook designer for your project.  
  
7.  Press F6 to display the shortcut keys for the Ribbon.  
  
## Accessibility at Run Time  
  
### Windows Forms Controls on Office Documents  
 Windows Forms controls expose accessibility properties to provide information about the control to accessibility aids, such as screen readers. You can take advantage of these accessibility properties when the controls are on an Office document in a document-level customization. For more information, see [Providing Accessibility Information for Controls on a Windows Form](../Topic/Providing%20Accessibility%20Information%20for%20Controls%20on%20a%20Windows%20Form.md).  
  
 However, there are some accessibility limitations at run time when Windows Forms controls are hosted on an Excel workbook or Word document:  
  
-   You cannot tab from one control to another.  
  
-   Controls on a document are disabled when you change the zoom setting of the document to anything other than 100%.  
  
 For information about limitations of Windows Forms controls on documents, see [Limitations of Windows Forms Controls on Office Documents](../vsto/limitations-of-windows-forms-controls-on-office-documents.md).  
  
### Actions Panes and Custom Task Panes  
 When an actions pane or custom task pane has focus, you access controls the same way you would access controls on a Windows Forms application. To move your cursor between the actions pane and the document, you can press **F6**.  
  
 For more information about actions panes and custom task panes, see [Actions Pane Overview](../vsto/actions-pane-overview.md) and [Custom Task Panes](../vsto/custom-task-panes.md).  
  
### Display Modes  
 Visual Studio has the following limitations related to display modes:  
  
-   Controls on a Word document or Excel worksheet are disabled when you change the zoom setting of the document to anything other than 100%.  
  
-   The **New Project** dialog box does not display controls correctly if a user changes the computer's accessibility options to **Use High Contrast**.  
  
 You can use Magnifier to overcome these limitations. Magnifier is a display utility in Windows that creates a separate window that displays a magnified portion of the screen.  
  
## See Also  
 [Developing Office Solutions](../vsto/developing-office-solutions.md)   
 [Controls on Office Documents](../vsto/controls-on-office-documents.md)   
 [Accessibility for People with Disabilities](/visual-studio/ide/reference/accessibility-for-people-with-disabilities)   
 [Accessibility Features of Visual Studio](/visual-studio/ide/reference/accessibility-features-of-visual-studio)  
  
  