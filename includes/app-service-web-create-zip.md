---
author: cephalin
ms.service: app-service-web
ms.topic: include
ms.date: 11/03/2016
ms.author: cephalin
ms.openlocfilehash: d804cb310a8638713cabf76c2f4192a0e4d0f43d
ms.sourcegitcommit: 9d7391e11d69af521a112ca886488caff5808ad6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/25/2018
ms.locfileid: "50134448"
---
## <a name="create-a-project-zip-file"></a>创建一个项目 zip 文件

请确保仍处于示例项目的根目录中。 创建一个包含项目中的所有内容的 zip 存档。 以下命令使用终端中的默认工具：

```
# Bash
zip -r myAppFiles.zip .

# PowerShell
Compress-Archive -Path * -DestinationPath myAppFiles.zip
``` 

随后将此 ZIP 文件上传到 Azure 并将其部署到应用服务。