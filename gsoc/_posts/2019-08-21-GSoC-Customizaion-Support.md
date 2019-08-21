---
id: 3
title: Customization Support
date: 2019-08-21T02:21:44+00:00
author: Sumit Chauhan
layout: post
permalink: /customization-support/
comment: true
dsq_thread_id:
  -
views:
  -
sociallikes:
  -
categories:
  -
tags:
  -
  -
---

**What is Customization Suppport ?**


LibreOffice introduced <a href="https://youtu.be/6HUnR5IoAQk?t=25">NotebookBar user interface</a> in version 6.2 . Customization Support allows users a customize NotebookBar by changing the visibility of buttons.


<iframe width="560" height="315" src="https://www.youtube.com/embed/363QTGaKgJU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



**What is done ?**

I proposed to create a basic Customization dialog that would allow to user to show/hide items in the NotebookBar.You can find the dialog at Tools->Customize -> NotebookBar(tab).

**Backend Engine**

The customization feature was previously available for traditional toolbars. Toolbars have .xml files whereas Notebookbar has .ui files. This problem didn't allow us to reuse the code.

The solution was to modify the .ui files. Then, store and reload them from the user directory. We also stored the modified data in registry modifications.xcu so that configurations can be retrieved if there is a version update.
<a href="https://opengrok.libreoffice.org/xref/core/cui/source/customize/CustomNotebookbarGenerator.cxx">Code</a>

<a href="http://www.xmlsoft.org/">Libxml2</a> is used to parse the .ui files.

**Customization Dialog**

The class SvxNotebookbarConfigPage is inherited from SvxConfigPage. SvxConfigPage is a base class for all the customization dialog in LibreOffice.
<a href="https://opengrok.libreoffice.org/xref/core/cui/source/customize/SvxNotebookbarConfigPage.cxx">Code</a>

**Future Work**

There are many <a href="https://opengrok.libreoffice.org/xref/core/cui/source/customize/SvxNotebookbarConfigPage.cxx?r=74f6acf0#105">features</a> still locked and need to finish. Also,
Also , 
* The use registrymodifications.xcu to retrieve the configuration and use them during an update is not complete.
* It would be better to open the customization dialog based on the tab opened in the Notebookbar interface..

Notebookbar extension patches : <a href="https://gerrit.libreoffice.org/#/q/sumit+customization"> Gerrit </a>


