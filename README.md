# macro-linshare

## Integration with LinShare

This macro integrates LinShare in XWiki, allowing to display linShare (https://linshare.org) documents inside XWiki.

The LinShare Macro allows to display a document from a [[LinShare Instance>>url:http://www.linshare.org/]]. 

## Installation

To make this macro work you will need to:

* XWiki 11.0+. This is needed for the LinShare picker to work in the Macro box.
* Have a LinShare instance and be logged on it. Ideally the XWiki and LinShare instance should be on the same single-sign on system. It is possible to connect LinShare and XWiki to LemonLDAP. The XWiki guide for LemonLDAP is [[available here>>url:https://extensions.xwiki.org/xwiki/bin/view/Extension/OpenID%20Connect/OpenID%20Connect%20Authenticator/ConfigurationLemonLDAP/]].
* Set the LinShare URL and Workgroup in [[the preferences>>XWiki.XWikiPreferences||queryString="editor=globaladmin&section=LinShare"]].
* Add a template in your skin. This is necessary to activate the LinShare picker in the macro box. The picker is necessary to not have to find the LinShare document uuid yourself.

To add the template to your skin you need to [[access your skin from the preferences>>XWiki.XWikiPreferences||queryString="editor=globaladmin&section=Themes"]] and edit it skin and add a template named "html_displayer/stringbuffer/edit.vm" with the following code in it "$xwiki.includeForm("Macros.LinShare.LinSharePicker")"

image:linshare-skin.png

## Example usage

This example would display the document with uuid 4af0518d-449d-463d-bd25-0280afc3b70f from the [[workgroup set in the XWiki preferences>>XWiki.XWikiPreferences||queryString="editor=globaladmin&section=LinShare"]].

{{linshare linshareId="4af0518d-449d-463d-bd25-0280afc3b70f"/}}

## Credits 

This Macro has been produced by XWiki SAS as part of the OpenPAAS-NG project funded by BPI France.
