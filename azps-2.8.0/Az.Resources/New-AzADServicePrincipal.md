---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 9db3e3d0fcb52869a53b4bd2b76603d2935c4dd0
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/05/2020
ms.locfileid: "93883366"
---
# <span data-ttu-id="6ba5e-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6ba5e-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="6ba5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ba5e-102">SYNOPSIS</span></span>
<span data-ttu-id="6ba5e-103">새 azure active directory service principal을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="6ba5e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ba5e-104">SYNTAX</span></span>

### <span data-ttu-id="6ba5e-105">SimpleParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6ba5e-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba5e-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba5e-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ba5e-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba5e-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba5e-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba5e-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba5e-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba5e-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba5e-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba5e-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba5e-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba5e-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ba5e-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba5e-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba5e-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba5e-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba5e-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba5e-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba5e-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba5e-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba5e-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba5e-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba5e-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba5e-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba5e-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba5e-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba5e-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba5e-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba5e-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ba5e-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ba5e-121">설명은</span><span class="sxs-lookup"><span data-stu-id="6ba5e-121">DESCRIPTION</span></span>
<span data-ttu-id="6ba5e-122">새 azure active directory service principal을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="6ba5e-123">사용자가 매개 변수에 대 한 기본값을 제공 하지 않는 경우 기본 매개 변수 집합에는 기본 값이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="6ba5e-124">사용 되는 기본값에 대 한 자세한 내용은 아래의 해당 매개 변수에 대 한 설명을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="6ba5e-125">이 cmdlet에는 and 매개 변수를 사용 하 여 서비스 사용자에 게 역할을 할당 하는 기능이 있습니다 `Role` `Scope` . 이러한 매개 변수 중 하나도 제공 하지 않으면 서비스 사용자에 게 역할이 할당 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="6ba5e-126">`Role`And `Scope` 매개 변수의 기본값은 각각 "참가자"이 고, 현재 구독은 사용자가 두 매개 _note_ 변수 중 하나에 대 한 값을 제공 하는 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="6ba5e-127">또한 cmdlet은 응용 프로그램을 암시적으로 만들고 해당 속성 (ApplicationId이 제공 되지 않은 경우)을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="6ba5e-128">응용 프로그램별 매개 변수를 업데이트 하려면 Set-AzADApplication cmdlet을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-128">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="6ba5e-129">**새-AzADServicePrincipal** 명령을 사용 하 여 서비스 사용자를 만드는 경우 출력에는 보호 해야 하는 자격 증명이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="6ba5e-130">이러한 자격 증명을 코드에 포함 하지 않도록 하거나 자격 증명을 소스 제어에 체크 인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="6ba5e-131">다른 방법으로는 자격 증명을 사용할 필요가 없도록 [관리 되는 id](/azure/active-directory/managed-identities-azure-resources/overview) 를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="6ba5e-132">기본적으로 **AzADServicePrincipal** 는 구독 범위에서 [참가자](/azure/role-based-access-control/built-in-roles#contributor) 역할을 서비스 사용자에 게 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="6ba5e-133">손상 된 서비스 보안 주체의 위험을 줄이려면 더 구체적인 역할을 할당 하 고 리소스 또는 리소스 그룹으로 범위를 좁힙니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="6ba5e-134">자세한 내용은 [역할 할당을 추가 하는 단계를](/azure/role-based-access-control/role-assignments-steps) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="6ba5e-135">예제의</span><span class="sxs-lookup"><span data-stu-id="6ba5e-135">EXAMPLES</span></span>

### <span data-ttu-id="6ba5e-136">예제 1-간단한 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="6ba5e-136">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="6ba5e-137">위의 명령은 제공 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-137">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="6ba5e-138">응용 프로그램 id가 제공 되지 않았으므로 서비스 사용자를 위해 응용 프로그램이 생성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-138">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="6ba5e-139">Or에 대 한 값이 제공 되지 않았으므로 `Role` `Scope` 만든 서비스 주체에는 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-139">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="6ba5e-140">예제 2-지정 된 역할 및 기본 범위의 간단한 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="6ba5e-140">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="6ba5e-141">위의 명령은 제공 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-141">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="6ba5e-142">응용 프로그램 id가 제공 되지 않았으므로 서비스 사용자를 위해 응용 프로그램이 생성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-142">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="6ba5e-143">서비스 사용자가 현재 구독에 대해 "읽기" 권한으로 생성 되었습니다 (매개 변수에 대 한 값이 제공 되지 않았으므로 `Scope` ).</span><span class="sxs-lookup"><span data-stu-id="6ba5e-143">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="6ba5e-144">예제 3-지정 된 범위 및 기본 역할을 가진 간단한 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="6ba5e-144">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="6ba5e-145">위의 명령은 제공 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-145">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="6ba5e-146">응용 프로그램 id가 제공 되지 않았으므로 서비스 사용자를 위해 응용 프로그램이 생성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-146">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="6ba5e-147">제공 된 리소스 그룹 범위를 통해 서비스 사용자가 "참가자" 권한으로 생성 되었습니다 (매개 변수에 대 한 값이 제공 되지 않았으므로 `Role` ).</span><span class="sxs-lookup"><span data-stu-id="6ba5e-147">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="6ba5e-148">예제 4-단순 광고 서비스 주도자 만들기 지정 된 범위 및 역할</span><span class="sxs-lookup"><span data-stu-id="6ba5e-148">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="6ba5e-149">위의 명령은 제공 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-149">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="6ba5e-150">응용 프로그램 id가 제공 되지 않았으므로 서비스 사용자를 위해 응용 프로그램이 생성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-150">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="6ba5e-151">서비스 사용자가 제공 된 리소스 그룹 범위에 대해 "읽기" 권한을 사용 하 여 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-151">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="6ba5e-152">예제 5-역할을 할당 하 여 응용 프로그램 id를 사용 하 여 새 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="6ba5e-152">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="6ba5e-153">응용 프로그램 id가 ' 4a28ad2-3| 4-4a41-bc3b-d22ddf90000e ' 인 응용 프로그램에 대 한 새 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-153">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="6ba5e-154">Or에 대 한 값이 제공 되지 않았으므로 `Role` `Scope` 만든 서비스 주체에는 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-154">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="6ba5e-155">예제 6-파이핑을 사용 하 여 새 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="6ba5e-155">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="6ba5e-156">개체 id가 ' 3ede3c26-b443-4e0b-9efc-b05e68338dc3 ' 인 응용 프로그램을 가져오고 해당 응용 프로그램에 대 한 새 광고 서비스 사용자를 만들기 위해 New-AzADServicePrincipal cmdlet에 대 한 파이프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-156">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="6ba5e-157">변수</span><span class="sxs-lookup"><span data-stu-id="6ba5e-157">PARAMETERS</span></span>

### <span data-ttu-id="6ba5e-158">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6ba5e-158">-ApplicationId</span></span>
<span data-ttu-id="6ba5e-159">테 넌 트의 서비스 사용자에 대 한 고유한 응용 프로그램 id입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-159">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="6ba5e-160">만든 후에는이 속성을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-160">Once created this property cannot be changed.</span></span>
<span data-ttu-id="6ba5e-161">응용 프로그램 id가 지정 되지 않은 경우 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-161">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="6ba5e-162">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="6ba5e-162">-ApplicationObject</span></span>
<span data-ttu-id="6ba5e-163">서비스 사용자를 만들 응용 프로그램을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-163">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ba5e-164">-CertValue</span><span class="sxs-lookup"><span data-stu-id="6ba5e-164">-CertValue</span></span>
<span data-ttu-id="6ba5e-165">"비대칭" 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-165">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="6ba5e-166">Base 64 인코딩된 인증서를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-166">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="6ba5e-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ba5e-167">-DefaultProfile</span></span>
<span data-ttu-id="6ba5e-168">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6ba5e-168">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ba5e-169">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6ba5e-169">-DisplayName</span></span>
<span data-ttu-id="6ba5e-170">서비스 사용자의 식별 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-170">The friendly name of the service principal.</span></span> <span data-ttu-id="6ba5e-171">표시 이름이 제공 되지 않은 경우이 값은 기본적으로 ' azure-powershell-MM-dd-yyyy-mm-dd-ss ' 이며, 여기서 접미사는 응용 프로그램을 만드는 데 걸리는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-171">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="6ba5e-172">-EndDate</span><span class="sxs-lookup"><span data-stu-id="6ba5e-172">-EndDate</span></span>
<span data-ttu-id="6ba5e-173">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-173">The effective end date of the credential usage.</span></span>
<span data-ttu-id="6ba5e-174">기본 끝 날짜 값은 오늘부터 1 년입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-174">The default end date value is one year from today.</span></span> <span data-ttu-id="6ba5e-175">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 이전으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-175">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="6ba5e-176">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="6ba5e-176">-KeyCredential</span></span>
<span data-ttu-id="6ba5e-177">응용 프로그램과 연결 된 키 자격 증명의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-177">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="6ba5e-178">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="6ba5e-178">-PasswordCredential</span></span>
<span data-ttu-id="6ba5e-179">응용 프로그램과 연결 된 암호 자격 증명 모음입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-179">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="6ba5e-180">-역할</span><span class="sxs-lookup"><span data-stu-id="6ba5e-180">-Role</span></span>
<span data-ttu-id="6ba5e-181">서비스 사용자가 범위를 초과 하는 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-181">The role that the service principal has over the scope.</span></span> <span data-ttu-id="6ba5e-182">값이 `Scope` 제공 되지만 값이 제공 되지 않으면 `Role` 기본적으로 `Role` ' 참가자 ' 역할이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-182">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="6ba5e-183">-범위</span><span class="sxs-lookup"><span data-stu-id="6ba5e-183">-Scope</span></span>
<span data-ttu-id="6ba5e-184">서비스 사용자에 게 사용 권한이 있는 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-184">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="6ba5e-185">값이 `Role` 제공 되지만 값이 제공 되지 않으면 `Scope` `Scope` 현재 구독이 기본값으로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-185">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="6ba5e-186">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="6ba5e-186">-SkipAssignment</span></span>
<span data-ttu-id="6ba5e-187">설정 하는 경우 서비스 사용자에 대 한 기본 역할 할당 만들기를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-187">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="6ba5e-188">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="6ba5e-188">-StartDate</span></span>
<span data-ttu-id="6ba5e-189">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-189">The effective start date of the credential usage.</span></span>
<span data-ttu-id="6ba5e-190">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-190">The default start date value is today.</span></span> <span data-ttu-id="6ba5e-191">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후에이를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-191">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="6ba5e-192">-확인</span><span class="sxs-lookup"><span data-stu-id="6ba5e-192">-Confirm</span></span>
<span data-ttu-id="6ba5e-193">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ba5e-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ba5e-194">-WhatIf</span></span>
<span data-ttu-id="6ba5e-195">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-195">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ba5e-196">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ba5e-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ba5e-197">CommonParameters</span></span>
<span data-ttu-id="6ba5e-198">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ba5e-199">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ba5e-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ba5e-200">입력</span><span class="sxs-lookup"><span data-stu-id="6ba5e-200">INPUTS</span></span>

### <span data-ttu-id="6ba5e-201">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="6ba5e-201">System.Guid</span></span>

### <span data-ttu-id="6ba5e-202">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6ba5e-202">System.String</span></span>

### <span data-ttu-id="6ba5e-203">ActiveDirectory PSADApplication 프로그램</span><span class="sxs-lookup"><span data-stu-id="6ba5e-203">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="6ba5e-204">ActiveDirectory PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="6ba5e-204">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="6ba5e-205">ActiveDirectory PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="6ba5e-205">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="6ba5e-206">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="6ba5e-206">System.DateTime</span></span>

## <span data-ttu-id="6ba5e-207">출력</span><span class="sxs-lookup"><span data-stu-id="6ba5e-207">OUTPUTS</span></span>

### <span data-ttu-id="6ba5e-208">ActiveDirectory PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6ba5e-208">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="6ba5e-209">PSADServicePrincipalWrapper에 대 한 권한 부여.</span><span class="sxs-lookup"><span data-stu-id="6ba5e-209">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="6ba5e-210">상속자</span><span class="sxs-lookup"><span data-stu-id="6ba5e-210">NOTES</span></span>
<span data-ttu-id="6ba5e-211">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="6ba5e-211">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="6ba5e-212">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ba5e-212">RELATED LINKS</span></span>

[<span data-ttu-id="6ba5e-213">제거-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6ba5e-213">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="6ba5e-214">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6ba5e-214">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="6ba5e-215">새로운 AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6ba5e-215">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="6ba5e-216">제거-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6ba5e-216">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="6ba5e-217">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6ba5e-217">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="6ba5e-218">새로운 AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6ba5e-218">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="6ba5e-219">제거-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="6ba5e-219">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

