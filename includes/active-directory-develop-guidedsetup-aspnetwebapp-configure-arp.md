---
title: include 文件
description: include 文件
services: active-directory
documentationcenter: dev-center-name
author: andretms
manager: mtillman
editor: ''
ms.service: active-directory
ms.devlang: na
ms.topic: include
ms.tgt_pltfrm: na
ms.workload: identity
ms.date: 09/17/2018
ms.author: andret
ms.custom: include file
ms.openlocfilehash: f3048daa7d597d92041733cdf5c6f299cebc2f73
ms.sourcegitcommit: 0f54b9dbcf82346417ad69cbef266bc7804a5f0e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/26/2018
ms.locfileid: "50142672"
---
## <a name="configure-your-aspnet-web-app-with-the-applications-registration-information"></a>使用应用程序的注册信息配置 ASP.NET Web 应用

此步将配置项目以使用 SSL，并使用 SSL URL 配置应用程序的注册信息。 此后通过 web.config 将应用程序注册信息添加到解决方案。

1. 在解决方案资源管理器中，选择项目并查看`Properties`窗口（如果看不到“属性”窗口，请按 F4）
2. 将 `SSL Enabled` 更改为 `True`
3. 复制以上 `SSL URL` 中的值，并将其粘贴到此页顶部的`Redirect URL` 字段，单击“更新”:<br/><br/>![项目属性](media/active-directory-develop-guidedsetup-aspnetwebapp-configure/vsprojectproperties.png)<br />
4. 在 `configuration\appSettings` 节下根文件夹内 `web.config` 文件中添加以下内容：

```xml
<add key="ClientId" value="[Enter the application Id here]" />
<add key="RedirectUri" value="[Enter the Redirect URL here]" />
<add key="Tenant" value="common" />
<add key="Authority" value="https://login.microsoftonline.com/{0}/v2.0" /> 
```
