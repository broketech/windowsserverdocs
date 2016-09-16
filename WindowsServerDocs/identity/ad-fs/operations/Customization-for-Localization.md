---
title: Customization for Localization 
description:
author: billmath
ms.author: billmath
manager: femila
ms.date: 08/31/2016
ms.topic: article
ms.prod: windows-server-threshold
ms.service: active-directory
ms.technology: identity-adfs
---
# Customization for Localization 

>Applies To: Windows Server 2016, Windows Server 2012 R2

Localizing web content into languages other than English is possible. Be aware of the following considerations when you localize.  
  
After the content is customized, the customization takes precedence; therefore, you should customize for all languages that you want to support. All customized content takes a locale parameter. When you configure localized content, configure it with a country\-less locale first, for example, "en", before you configure a country and region\-specific locale such as "en\-us".  
  
The following shows some additional code examples.  
  
    
    Set-AdfsWebTheme -TargetName default -Logo @{Locale="";Path="c:\contoso.png"}  
      
    Set-AdfsWebTheme -TargetName default -Illustration @{Locale="";Path="c:\illustration.png"}  

  
The following shows some additional code examples.  
  
 
    Set-AdfsGlobalWebContent -ErrorPageDescriptionText "This is Contoso's error page description" –locale "en"  
  
  

    Set-AdfsGlobalWebContent -ErrorPageDescriptionText "Il s'agit de description de page erreur de Contoso" –locale "fr"  
 
  
If you want to customize the web content to languages other than English that requires the input of Unicode, we recommend that you use the Windows PowerShell ISE. For additional information see [Introducing the Windows PowerShell ISE](http://technet.microsoft.com/library/dd315244.aspx).  

## Additional references 
[AD FS User Sign-in Customization](AD-FS-user-sign-in-customization.md) 