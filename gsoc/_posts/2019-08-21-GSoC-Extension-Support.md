---
id: 4
title: Extension Support
date: 2019-08-21T02:21:44+00:00
author: Sumit Chauhan
layout: post
permalink: /extension-support/
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


**What is Extension Suppport ?**
 
Extension Support allows users to add extensions in NotebookBar. There is an extension tab in all the NotebookBar interfaces where the added extension will be available.Add extension: Tool -> Extension Manager.


![extension](/static/img/extensionsupport.png){:class="img-responsive"}



**Schema for Extension Developer**

There are two ways of adding an extension.

**1.** To add an extension under Extension Tab:


{% highlight xml %}
<node oor:name="OfficeNotebookBar">
    <node oor:name="*.OfficeNotebookBar" oor:op="replace">
            <node oor:name="m001" oor:op="replace">
                <prop oor:name="URL" oor:type="xs:string">
                    <value> </value>
                </prop>
                <prop oor:name="Title" oor:type="xs:string">
                    <value> </value>
                </prop>
                <prop oor:name="ImageIdentifier" oor:type="xs:string">
                    <value> </value>
                </prop>
                <prop oor:name="Target" oor:type="xs:string">
                    <value> </value>
                </prop>
                <prop oor:name="Context" oor:type="xs:string">
                    <value> </value>
                </prop>
                <prop oor:name="ControlType" oor:type="xs:string">
                    <value> </value>
                </prop>
                <prop oor:name="Width" oor:type="xs:string">
                    <value> </value>
                </prop>
                <prop oor:name="Style" oor:type="xs:string">
                    <value> </value>
                </prop>
            </node>
    </node>
</node>
{% endhighlight %}

Developers should add the following code in the addons.xcu to make an extension compatible for Notebookbar.For more <a href="https://opengrok.libreoffice.org/xref/core/officecfg/registry/schema/org/openoffice/Office/Addons.xcs#338">reading </a>


**2.** To add extension anywhere in the Notebookbar.

The <a href="https://opengrok.libreoffice.org/xref/core/officecfg/registry/schema/org/openoffice/Office/Addons.xcs#298">Schema </a> is available here but the backend is still under progress.


**What is done ?**

The task to add extension under the extension tab is almost finished. There are some open patches and expected to be finished soon.


**Future Work**

* The task to add extension anywhere in the NotebookBar 
* Checking the compatibility with other Notebookbar interfaces(other than Tabbed) and refine the existing work.

Notebookbar extension patches <a href ="https://gerrit.libreoffice.org/#/q/sumit+extension">Gerrit</a>.

Extensions compatible with Notebookbar : <a href = "https://drive.google.com/drive/folders/1cl_sr201_pnnOPp-Ka--zwKseQZB7oAf?usp=sharing">Download</a>





