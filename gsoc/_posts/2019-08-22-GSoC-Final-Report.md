---
id: 5
title: GSoC'19 Final Report
date: 2019-08-22T02:21:44+00:00
author: Sumit Chauhan
layout: post
permalink: /gsoc-final-report/
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

**Work Done :**

* Created customization support for Notebookbar<sup><a href="/customization-support/">[1]</a></sup>.
* Created extension support for Notebookbar<sup><a href="/extension-support/">[2]</a></sup>.

**Customization Support:**

* Rendering notebookbar*.ui file from user/share directory - <a href="https://cgit.freedesktop.org/libreoffice/core/commit/?id=889a4fed08aecfd45e5706af27510e40932f2732">Patch</a>
* Using registrymodifications.xcu for storing customized uiitem data - <a href ="https://cgit.freedesktop.org/libreoffice/core/commit/?id=c473c5b462f33df439b4b62b394c5d7811a05c7c">Patch</a>
* UI for the Notebookbar Customization tab - <a href="https://cgit.freedesktop.org/libreoffice/core/commit/?id=015dc88a595c1c92d2b724cd868aecb07199f995">Patch</a>
* Reload Notebookbar, when customization is being done - <a href="https://cgit.freedesktop.org/libreoffice/core/commit/?id=6b888ac476fe6ac2ee96c7086cb8c24249f08473">Patch</a>
* Category Target, now available for customization tab - <a href="https://cgit.freedesktop.org/libreoffice/core/commit/?id=7eab1e14c5874901757a291609f289911ac64031">Patch</a>
* Category Target and Function Target enhanced in customization Tab- <a href="https://cgit.freedesktop.org/libreoffice/core/commit/?id=9105b85c708f42024ce063b9a944466c0afdfe9a">Patch</a>

**Extension Support :**

* Addons(extension) support is extended for NotebookBar - <a href ="https://cgit.freedesktop.org/libreoffice/core/commit/?id=147e820cc1bd7110331a6ea73db678a4a6c324e0 "> Patch </a>
* Engine to add Extension inside extension tab in NotebookBar - <a href = "https://cgit.freedesktop.org/libreoffice/core/commit/?id=fbcd5f074ca3dc105f4fe45b6975c6de2bf60f35"> Patch </a>
* Patch fixes the image rendering issue of extension in NotebookBar <a href = "https://cgit.freedesktop.org/libreoffice/core/commit/?id=22f2ecbcabf3928d5486690ca6465b7b37bc8a10"> Patch </a>
* Extension support for gtkmenuItem and notebookbar.ui file added for writer <a href= "https://cgit.freedesktop.org/libreoffice/core/commit/?id=7b0dd98941911c686c0d127810d1c333df5026c3"> Patch </a>
* GtkWidget for the priority of extension under Extension Tab <a href="https://gerrit.libreoffice.org/#/c/76987/"> Patch </a>

<a href = "https://gerrit.libreoffice.org/#/q/sumit+chauhan">Gerrit</a> for more details and patches.

**To do:**

**Customization:**

There are many <a href="https://opengrok.libreoffice.org/xref/core/cui/source/customize/SvxNotebookbarConfigPage.cxx?r=74f6acf0#105">features</a> still locked and need to finish. Also,

* The use registrymodifications.xcu to retrieve the configuration and use them during an update is not complete.
* It would be better to open the customization dialog based on the tab opened in the Notebookbar interface.

**Extension :**

* The task to add extension anywhere in the NotebookBar 
* Checking the compatibility with other Notebookbar interfaces(other than Tabbed) and refine the existing work.


** Follow <a href="/customization-support/">[1]</a> , <a href="/extension-support/">[2]</a> for more details.

