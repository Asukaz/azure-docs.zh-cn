---
title: 教程：Azure Active Directory 与 8x8 Virtual Office 的集成 | Microsoft 文档
description: 了解如何在 Azure Active Directory 和 8x8 Virtual Office 之间配置单一登录。
services: active-directory
documentationCenter: na
author: jeevansd
manager: femila
ms.reviewer: joflore
ms.assetid: b34a6edf-e745-4aec-b0b2-7337473d64c5
ms.service: active-directory
ms.component: saas-app-tutorial
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 10/30/2018
ms.author: jeedes
ms.openlocfilehash: 53db637bf7ad47896747b491fcbe31123fdb104e
ms.sourcegitcommit: ae45eacd213bc008e144b2df1b1d73b1acbbaa4c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2018
ms.locfileid: "50741804"
---
# <a name="tutorial-azure-active-directory-integration-with-8x8-virtual-office"></a>教程：Azure Active Directory 与 8x8 Virtual Office 的集成

在本教程中，了解如何将 8x8 Virtual Office 与 Azure Active Directory (Azure AD) 集成。

将 8x8 Virtual Office 与 Azure AD 集成可带来以下好处：

- 可以在 Azure AD 中控制谁有权访问 8x8 Virtual Office。
- 可让用户使用其 Azure AD 帐户自动登录到 8x8 Virtual Office（单一登录）。
- 可在中心位置（即 Azure 门户）管理帐户。

如需了解有关 SaaS 应用与 Azure AD 集成的详细信息，请参阅 [Azure Active Directory 的应用程序访问与单一登录是什么](../manage-apps/what-is-single-sign-on.md)

## <a name="prerequisites"></a>先决条件

若要配置 Azure AD 与 8x8 Virtual Office 的集成，需要以下各项：

- Azure AD 订阅
- 已启用 8x8 Virtual Office 单一登录的订阅

> [!NOTE]
> 为了测试本教程中的步骤，我们不建议使用生产环境。

测试本教程中的步骤应遵循以下建议：

- 除非必要，请勿使用生产环境。
- 如果没有 Azure AD 试用环境，可以[获取一个月的试用版](https://azure.microsoft.com/pricing/free-trial/)。

## <a name="scenario-description"></a>方案描述

在本教程中，将在测试环境中测试 Azure AD 单一登录。 本教程中概述的方案包括两个主要构建基块：

1. 从库中添加 8x8 Virtual Office
2. 配置和测试 Azure AD 单一登录

## <a name="adding-8x8-virtual-office-from-the-gallery"></a>从库中添加 8x8 Virtual Office

要配置 8x8 Virtual Office 到 Azure AD 的集成，需要将 8x8 Virtual Office 从库中添加到托管的 SaaS 应用列表。

**若要从库中添加 8x8 Virtual Office，请执行以下步骤：**

1. 在 **[Azure 门户](https://portal.azure.com)** 的左侧导航面板中，单击“Azure Active Directory”图标。 

    ![“Azure Active Directory”按钮][1]

2. 导航到“企业应用程序”。 然后转到“所有应用程序”。

    ![“企业应用程序”边栏选项卡][2]
    
3. 若要添加新应用程序，请单击对话框顶部的“新建应用程序”按钮。

    ![“新增应用程序”按钮][3]

4. 在搜索框中，键入“8x8 Virtual Office”，在结果面板中选择“8x8 Virtual Office”，然后单击“添加”按钮添加该应用程序。

    ![结果列表中的 8x8 Virtual Office](./media/8x8virtualoffice-tutorial/tutorial_8x8virtualoffice_addfromgallery.png)

## <a name="configure-and-test-azure-ad-single-sign-on"></a>配置和测试 Azure AD 单一登录

在本部分中，将基于名为 Britta Simon 的测试用户配置和测试 8x8 Virtual Office 的 Azure AD 单一登录。

若要运行单一登录，Azure AD 需要知道与 Azure AD 用户相对应的 8x8 Virtual Office 用户。 换言之，需要建立 Azure AD 用户与 8x8 Virtual Office 中的相关用户之间的链接关系。

若要配置和测试 8x8 Virtual Office 的 Azure AD 单一登录，需要完成以下构建基块：

1. **[配置 Azure AD 单一登录](#configuring-azure-ad-single-sign-on)** - 让用户使用此功能。
2. **[创建 Azure AD 测试用户](#creating-an-azure-ad-test-user)** - 使用 Britta Simon 测试 Azure AD 单一登录。
3. [创建 8x8 Virtual Office 测试用户](#creating-a-8x8-virtual-office-test-user) - 在 8x8 Virtual Office 中创建 Britta Simon 的对应用户，并将其链接到该用户的 Azure AD 表示形式。
4. **[分配 Azure AD 测试用户](#assigning-the-azure-ad-test-user)** - 让 Britta Simon 使用 Azure AD 单一登录。
5. **[测试单一登录](#testing-single-sign-on)** - 验证配置是否正常工作。

### <a name="configuring-azure-ad-single-sign-on"></a>配置 Azure AD 单一登录

在本部分中，将在 Azure 门户中启用 Azure AD 单一登录，并在 8x8 Virtual Office 应用程序中配置单一登录。

**若要配置 8x8 Virtual Office 的 Azure AD 单一登录，请执行以下步骤：**

1. 在 Azure 门户中的 8x8 Virtual Office 应用程序集成页上，单击“单一登录”。

    ![配置单一登录链接][4]

2. 在“选择单一登录方法”对话框中，单击“SAML”模式对应的“选择”，以启用单一登录。

    ![配置单一登录](common/tutorial_general_301.png)

3. 在“使用 SAML 设置单一登录”页上，单击“编辑”图标以打开“基本 SAML 配置”对话框。

    ![配置单一登录](common/editconfigure.png)

4. 在“基本 SAML 配置”部分中，按照以下步骤操作：

    ![8x8 Virtual Office 域和 URL 单一登录信息](./media/8x8virtualoffice-tutorial/tutorial_8x8virtualoffice_url.png)

    a. 在“标识符”文本框中，键入一个 URL：`https://sso.8x8.com/saml2`

    b. 在“回复 URL”文本框中，键入 URL：`https://sso.8x8.com/saml2`

5. 在“SAML 签名证书”页的“SAML 签名证书”部分中，单击“下载”以下载“证书(原始)”并将证书文件保存在计算机上。

    ![证书下载链接](./media/8x8virtualoffice-tutorial/tutorial_8x8virtualoffice_certificate.png) 

6. 在“设置 8x8 Virtual Office”部分中，根据要求复制相应的 URL。

    a. 登录 URL

    b. Azure AD 标识符

    c. 注销 URL

    ![8x8 Virtual Office 配置](common/configuresection.png)

7. 以管理员身份登录到 8x8 Virtual Office 租户。

8. 在“应用程序”面板上选择“Virtual Office 帐户管理器”。

    ![在应用端上配置](./media/8x8virtualoffice-tutorial/tutorial_8x8virtualoffice_001.png)

9. 选择要管理的“企业”帐户，并单击“登录”按钮。

    ![在应用端上配置](./media/8x8virtualoffice-tutorial/tutorial_8x8virtualoffice_002.png)

10. 在菜单列表中单击“帐户”选项卡。

    ![在应用端上配置](./media/8x8virtualoffice-tutorial/tutorial_8x8virtualoffice_003.png)

11. 在帐户列表中单击“单一登录”。
  
    ![在应用端上配置](./media/8x8virtualoffice-tutorial/tutorial_8x8virtualoffice_004.png)

12. 在“身份验证”方法下选择“单一登录”，然后单击“SAML”。

    ![在应用端上配置](./media/8x8virtualoffice-tutorial/tutorial_8x8virtualoffice_005.png)

13. 在“SAML 单一登录”部分中，执行以下步骤：

    ![在应用端上配置](./media/8x8virtualoffice-tutorial/tutorial_8x8virtualoffice_006.png)

    a. 在“登录 URL”文本框中，粘贴从 Azure 门户复制的“登录 URL”值。

    b. 在“注销 URL”文本框中，粘贴从 Azure 门户复制的“注销 URL”值。

    c. 在“颁发者 URL”文本框中，粘贴从 Azure 门户复制的“Azure AD 标识符”值。

    d. 单击“浏览”按钮，上传已从 Azure 门户下载的证书。

    e. 单击“保存”按钮  。

### <a name="creating-an-azure-ad-test-user"></a>创建 Azure AD 测试用户

本部分的目的是在 Azure 门户中创建名为 Britta Simon 的测试用户。

1. 在 Azure 门户的左侧窗格中，依次选择“Azure Active Directory”、“用户”和“所有用户”。

    ![创建 Azure AD 用户][100]

2. 选择屏幕顶部的“新建用户”。

    ![创建 Azure AD 测试用户](common/create_aaduser_01.png) 

3. 在“用户属性”中，按照以下步骤操作。

    ![创建 Azure AD 测试用户](common/create_aaduser_02.png)

    a. 在“名称”字段中，输入 BrittaSimon。
  
    b. 在“用户名”字段中键入 **brittasimon@yourcompanydomain.extension**  
    例如： BrittaSimon@contoso.com

    c. 选择“属性”，再选择“显示密码”复选框，然后记下“密码”框中显示的值。

    d. 选择“创建”。
  
### <a name="creating-a-8x8-virtual-office-test-user"></a>创建 8x8 Virtual Office 测试用户

本部分要在 8x8 Virtual Office 中创建名为 Britta Simon 的用户。 8x8 Virtual Office 支持在默认情况下启用的实时预配。

此部分不存在任何操作项。 如果尚不存在用户，则会在尝试访问 8x8 Virtual Office 期间创建一个新用户。

> [!NOTE]
> 如果需要手动创建用户，需要联系 [8x8 Virtual Office 支持团队](https://www.8x8.com/about-us/contact-us)。

### <a name="assigning-the-azure-ad-test-user"></a>分配 Azure AD 测试用户

在本部分中，通过向 Britta Simon 授予 8x8 Virtual Office 的访问权限支持她使用 Azure 单一登录。

1. 在 Azure 门户中，选择“企业应用程序”，然后选择“所有应用程序”。

    ![分配用户][201]

2. 在应用程序列表中，选择“8x8 Virtual Office”。

    ![配置单一登录](./media/8x8virtualoffice-tutorial/tutorial_8x8virtualoffice_app.png) 

3. 在左侧菜单中，单击“用户和组”。

    ![分配用户][202]

4. 单击“添加”按钮。 然后在“添加分配”对话框中选择“用户和组”。

    ![分配用户][203]

5. 在“用户和组”对话框中，选择“用户”列表中的 Britta Simon，然后单击屏幕底部的“选择”按钮。

6. 在“添加分配”对话框中，选择“分配”按钮。

### <a name="testing-single-sign-on"></a>测试单一登录

在本部分中，使用访问面板测试 Azure AD 单一登录配置。

在“访问面板”中单击 8x8 Virtual Office 磁贴时，应自动登录到 8x8 Virtual Office 应用程序。
有关访问面板的详细信息，请参阅[访问面板简介](../user-help/active-directory-saas-access-panel-introduction.md)。

## <a name="additional-resources"></a>其他资源

* [有关如何将 SaaS 应用与 Azure Active Directory 集成的教程列表](tutorial-list.md)
* [Azure Active Directory 的应用程序访问与单一登录是什么？](../manage-apps/what-is-single-sign-on.md)

<!--Image references-->

[1]: common/tutorial_general_01.png
[2]: common/tutorial_general_02.png
[3]: common/tutorial_general_03.png
[4]: common/tutorial_general_04.png

[100]: common/tutorial_general_100.png

[201]: common/tutorial_general_201.png
[202]: common/tutorial_general_202.png
[203]: common/tutorial_general_203.png
