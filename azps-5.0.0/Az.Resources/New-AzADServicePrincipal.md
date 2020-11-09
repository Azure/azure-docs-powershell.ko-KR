---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 6d268c2378c93bcfb98e64c654880e8055bcede8
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/05/2020
ms.locfileid: "94311720"
---
# <span data-ttu-id="14906-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="14906-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="14906-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14906-102">SYNOPSIS</span></span>
<span data-ttu-id="14906-103">새 Azure active directory service principal을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14906-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="14906-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14906-104">SYNTAX</span></span>

### <span data-ttu-id="14906-105">SimpleParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="14906-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14906-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="14906-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14906-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="14906-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14906-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="14906-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14906-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="14906-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14906-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="14906-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14906-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="14906-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14906-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="14906-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14906-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="14906-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14906-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="14906-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14906-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="14906-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14906-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="14906-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14906-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="14906-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14906-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="14906-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14906-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="14906-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14906-120">설명은</span><span class="sxs-lookup"><span data-stu-id="14906-120">DESCRIPTION</span></span>

<span data-ttu-id="14906-121">새 Azure active directory service principal을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14906-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="14906-122">매개 변수를 제공 하지 않은 경우 기본 매개 변수 집합에서 기본 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="14906-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="14906-123">기본값에 대 한 자세한 내용은 각 매개 변수에 대 한 설명을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14906-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="14906-124">이 cmdlet에는 **역할** 및 **범위** 매개 변수를 사용 하 여 서비스 사용자에 게 역할을 할당 하는 기능이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="14906-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="14906-125">둘 다 생략 하면 참가자 역할이 서비스 사용자에 게 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14906-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="14906-126">**Role** 및 **Scope** 매개 변수의 기본값은 현재 구독에 대 한 **참가자** 입니다.</span><span class="sxs-lookup"><span data-stu-id="14906-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="14906-127">이 cmdlet은 응용 프로그램을 만들고 ApplicationId이 제공 되지 않은 경우 해당 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="14906-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="14906-128">응용 프로그램 관련 매개 변수를 업데이트 하려면 [AzADApplication](./update-azadapplication.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="14906-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="14906-129">**새-AzADServicePrincipal** 명령을 사용 하 여 서비스 사용자를 만드는 경우 출력에는 보호 해야 하는 자격 증명이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14906-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="14906-130">이러한 자격 증명을 코드에 포함 하지 않도록 하거나 자격 증명을 소스 제어에 체크 인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="14906-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="14906-131">다른 방법으로는 자격 증명을 사용할 필요가 없도록 [관리 되는 id](/azure/active-directory/managed-identities-azure-resources/overview) 를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="14906-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="14906-132">기본적으로 **AzADServicePrincipal** 는 구독 범위에서 [참가자](/azure/role-based-access-control/built-in-roles#contributor) 역할을 서비스 사용자에 게 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="14906-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="14906-133">손상 된 서비스 보안 주체의 위험을 줄이려면 더 구체적인 역할을 할당 하 고 리소스 또는 리소스 그룹으로 범위를 좁힙니다.</span><span class="sxs-lookup"><span data-stu-id="14906-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="14906-134">자세한 내용은 [역할 할당을 추가 하는 단계를](/azure/role-based-access-control/role-assignments-steps) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14906-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="14906-135">예제의</span><span class="sxs-lookup"><span data-stu-id="14906-135">EXAMPLES</span></span>

### <span data-ttu-id="14906-136">예제 1: 간단한 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="14906-136">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="14906-137">다음 예에서는 지정 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14906-137">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="14906-138">응용 프로그램 ID가 제공 되지 않으므로 서비스 사용자를 위해 응용 프로그램이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14906-138">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="14906-139">**역할** 또는 **범위** 에 대 한 값은 제공 되지 않으므로 만든 서비스 사용자에 게는 현재 구독에 대 한 **참가자** 역할이 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14906-139">Since no values are provided for **Role** or **Scope** , the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="14906-140">예제 2: 지정 된 역할 및 기본 범위를 사용 하 여 간단한 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="14906-140">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="14906-141">다음 예에서는 지정 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14906-141">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="14906-142">응용 프로그램 ID가 제공 되지 않으므로 서비스 사용자를 위해 응용 프로그램이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14906-142">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="14906-143">**범위** 매개 변수에 대 한 값이 제공 되지 않았으므로 현재 구독에 대 한 **읽기** 권한이 있는 서비스 사용자가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="14906-143">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### <span data-ttu-id="14906-144">예제 3: 지정 된 범위 및 기본 역할을 사용 하 여 간단한 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="14906-144">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="14906-145">다음 예에서는 지정 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14906-145">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="14906-146">응용 프로그램 ID가 제공 되지 않으므로 서비스 사용자를 위해 응용 프로그램이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14906-146">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="14906-147">**역할** 매개 변수에 대 한 값이 제공 되지 않았으므로 서비스 사용자는 제공 된 리소스 그룹 범위에 대 한 **참가자** 권한을 사용 하 여 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="14906-147">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="14906-148">예제 4: 지정 된 범위와 역할이 있는 간단한 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="14906-148">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="14906-149">다음 예에서는 지정 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14906-149">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="14906-150">응용 프로그램 ID가 제공 되지 않으므로 서비스 사용자를 위해 응용 프로그램이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14906-150">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="14906-151">제공 된 리소스 그룹 범위에 대 한 **읽기** 권한으로 서비스 사용자가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="14906-151">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="14906-152">예제 5: 역할을 할당 하 여 응용 프로그램 ID를 사용 하 여 새 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="14906-152">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="14906-153">다음 예제에서는 응용 프로그램 ID가 ' 00000000-0000-0000-0000-000000000000 ' 인 응용 프로그램에 대 한 새 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14906-153">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="14906-154">**역할** 또는 **범위** 에 대 한 값은 제공 되지 않으므로 만든 서비스 사용자에 게는 현재 구독에 대 한 **참가자** 역할이 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14906-154">Since no values are provided for **Role** or **Scope** , the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="14906-155">예제 6: 파이핑을 사용 하 여 새 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="14906-155">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="14906-156">다음 예제에서는 [Get-AzADApplication](./get-azadapplication.md) cmdlet을 사용 하 여 개체 ID가 ' 3ede3c26-b443-4e0b-9efc-b05e68338dc3 ' 인 응용 프로그램을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="14906-156">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="14906-157">결과는 `New-AzADServicePrincipal` 해당 응용 프로그램에 대 한 새 광고 서비스 사용자를 만들기 위해 cmdlet에 파이프라인으로 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14906-157">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="14906-158">예제 7: DisplayName 및 password 자격 증명을 사용 하 여 새 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="14906-158">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="14906-159">다음 예에서는 이름 **ServicePrincipalName** 와 **StrongPassworld! 23** 의 비밀 번호를 사용 하 여 새 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14906-159">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="14906-160">생성 된 응용 프로그램을 기반으로 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14906-160">It creates the service principal based on the created application.</span></span> <span data-ttu-id="14906-161">시작 날짜 및 종료 날짜가 암호 자격 증명에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14906-161">The start date and end date are added to the password credential.</span></span>

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### <span data-ttu-id="14906-162">예제 8: DisplayName 및 일반 키 자격 증명을 사용 하 여 새 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="14906-162">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="14906-163">다음 예제에서는 **ServicePrincipalName** 이름 및 인증서를 사용 하 여 새 응용 프로그램을 만듭니다 **$cert**. 생성 된 응용 프로그램을 기반으로 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14906-163">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="14906-164">끝 날짜가 키 자격 증명에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14906-164">The end date is added to key credential.</span></span>

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## <span data-ttu-id="14906-165">변수</span><span class="sxs-lookup"><span data-stu-id="14906-165">PARAMETERS</span></span>

### <span data-ttu-id="14906-166">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="14906-166">-ApplicationId</span></span>

<span data-ttu-id="14906-167">테 넌 트의 서비스 사용자에 대 한 고유한 응용 프로그램 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="14906-167">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="14906-168">만든 후에는이 속성을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="14906-168">Once created this property cannot be changed.</span></span> <span data-ttu-id="14906-169">기존 응용 프로그램의 응용 프로그램 ID를 지정 하지 않으면 응용 프로그램이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="14906-169">If an application ID for an existing application is not specified, an application is created.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14906-170">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="14906-170">-ApplicationObject</span></span>

<span data-ttu-id="14906-171">서비스 사용자를 만들 응용 프로그램을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="14906-171">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14906-172">-CertValue</span><span class="sxs-lookup"><span data-stu-id="14906-172">-CertValue</span></span>

<span data-ttu-id="14906-173">비대칭 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="14906-173">The value of the asymmetric credential type.</span></span> <span data-ttu-id="14906-174">이는 Base64로 인코딩된 인증서를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="14906-174">It represents the Base64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14906-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14906-175">-DefaultProfile</span></span>

<span data-ttu-id="14906-176">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14906-176">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14906-177">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="14906-177">-DisplayName</span></span>

<span data-ttu-id="14906-178">서비스 사용자의 식별 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14906-178">The friendly name of the service principal.</span></span> <span data-ttu-id="14906-179">표시 이름이 제공 되지 않은 경우이 값은 기본적으로 **azure-** i d-mm-dd-yyyy-ss 이며, 여기서 접미사는 응용 프로그램을 만드는 데 걸리는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="14906-179">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14906-180">-EndDate</span><span class="sxs-lookup"><span data-stu-id="14906-180">-EndDate</span></span>

<span data-ttu-id="14906-181">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="14906-181">The effective end date of the credential usage.</span></span> <span data-ttu-id="14906-182">기본 끝 날짜 값은 오늘부터 1 년입니다.</span><span class="sxs-lookup"><span data-stu-id="14906-182">The default end date value is one year from today.</span></span>
<span data-ttu-id="14906-183">비대칭 형식 자격 증명의 경우이를 X509 인증서가 유효한 날짜 또는 그 이전으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="14906-183">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14906-184">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="14906-184">-KeyCredential</span></span>

<span data-ttu-id="14906-185">응용 프로그램과 연결 된 키 자격 증명의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="14906-185">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14906-186">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="14906-186">-PasswordCredential</span></span>

<span data-ttu-id="14906-187">응용 프로그램과 연결 된 암호 자격 증명 모음입니다.</span><span class="sxs-lookup"><span data-stu-id="14906-187">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14906-188">-역할</span><span class="sxs-lookup"><span data-stu-id="14906-188">-Role</span></span>

<span data-ttu-id="14906-189">서비스 사용자가 범위를 초과 하는 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="14906-189">The role that the service principal has over the scope.</span></span> <span data-ttu-id="14906-190">값을 지정 하지 않으면 **역할** 은 기본적으로 **기여자** 역할을 합니다.</span><span class="sxs-lookup"><span data-stu-id="14906-190">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14906-191">-범위</span><span class="sxs-lookup"><span data-stu-id="14906-191">-Scope</span></span>

<span data-ttu-id="14906-192">서비스 사용자에 게 사용 권한이 있는 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="14906-192">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="14906-193">값을 지정 하지 않으면 현재 구독이 기본적으로 **Scope** 로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14906-193">If no value is provided, **Scope** defaults to the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14906-194">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="14906-194">-SkipAssignment</span></span>

<span data-ttu-id="14906-195">설정 된 경우 서비스 사용자에 대 한 기본 역할 할당 만들기를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="14906-195">If set, skip creating the default role assignment for the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14906-196">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="14906-196">-StartDate</span></span>

<span data-ttu-id="14906-197">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="14906-197">The effective start date of the credential usage.</span></span> <span data-ttu-id="14906-198">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="14906-198">The default start date value is today.</span></span> <span data-ttu-id="14906-199">비대칭 형식 자격 증명의 경우 X509 인증서를 사용할 수 있는 날짜 또는 그 이후에이를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="14906-199">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14906-200">-확인</span><span class="sxs-lookup"><span data-stu-id="14906-200">-Confirm</span></span>

<span data-ttu-id="14906-201">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="14906-201">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14906-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14906-202">-WhatIf</span></span>

<span data-ttu-id="14906-203">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="14906-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14906-204">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14906-204">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14906-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14906-205">CommonParameters</span></span>
<span data-ttu-id="14906-206">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14906-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14906-207">자세한 내용은 [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14906-207">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="14906-208">입력</span><span class="sxs-lookup"><span data-stu-id="14906-208">INPUTS</span></span>

### <span data-ttu-id="14906-209">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="14906-209">System.Guid</span></span>

### <span data-ttu-id="14906-210">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="14906-210">System.String</span></span>

### <span data-ttu-id="14906-211">ActiveDirectory PSADApplication 프로그램</span><span class="sxs-lookup"><span data-stu-id="14906-211">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="14906-212">ActiveDirectory PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="14906-212">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="14906-213">ActiveDirectory PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="14906-213">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="14906-214">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="14906-214">System.DateTime</span></span>

## <span data-ttu-id="14906-215">출력</span><span class="sxs-lookup"><span data-stu-id="14906-215">OUTPUTS</span></span>

### <span data-ttu-id="14906-216">ActiveDirectory PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="14906-216">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="14906-217">PSADServicePrincipalWrapper에 대 한 권한 부여.</span><span class="sxs-lookup"><span data-stu-id="14906-217">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="14906-218">상속자</span><span class="sxs-lookup"><span data-stu-id="14906-218">NOTES</span></span>

<span data-ttu-id="14906-219">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="14906-219">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="14906-220">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14906-220">RELATED LINKS</span></span>

[<span data-ttu-id="14906-221">제거-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="14906-221">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="14906-222">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="14906-222">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="14906-223">새로운 AzADApplication</span><span class="sxs-lookup"><span data-stu-id="14906-223">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="14906-224">제거-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="14906-224">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="14906-225">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="14906-225">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="14906-226">새로운 AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="14906-226">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="14906-227">제거-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="14906-227">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)