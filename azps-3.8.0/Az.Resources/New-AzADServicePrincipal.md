---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: f921cceb3692032f61f99db825efeea074773faa
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/05/2020
ms.locfileid: "94311717"
---
# <span data-ttu-id="a0dcb-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a0dcb-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="a0dcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="a0dcb-103">새 azure active directory service principal을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="a0dcb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0dcb-104">SYNTAX</span></span>

### <span data-ttu-id="a0dcb-105">SimpleParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a0dcb-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0dcb-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0dcb-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0dcb-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0dcb-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0dcb-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0dcb-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0dcb-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0dcb-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0dcb-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0dcb-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0dcb-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0dcb-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0dcb-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0dcb-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0dcb-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0dcb-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0dcb-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0dcb-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0dcb-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0dcb-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0dcb-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0dcb-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0dcb-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0dcb-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0dcb-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0dcb-118">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0dcb-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0dcb-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0dcb-120">설명은</span><span class="sxs-lookup"><span data-stu-id="a0dcb-120">DESCRIPTION</span></span>
<span data-ttu-id="a0dcb-121">새 azure active directory service principal을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-121">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="a0dcb-122">사용자가 매개 변수에 대 한 기본값을 제공 하지 않는 경우 기본 매개 변수 집합에는 기본 값이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-122">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="a0dcb-123">사용 되는 기본값에 대 한 자세한 내용은 아래의 해당 매개 변수에 대 한 설명을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-123">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="a0dcb-124">이 cmdlet에는 and 매개 변수를 사용 하 여 서비스 사용자에 게 역할을 할당 하는 기능이 있습니다 `Role` `Scope` . 이러한 매개 변수 중 하나도 제공 하지 않으면 서비스 사용자에 게 역할이 할당 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-124">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="a0dcb-125">`Role`And `Scope` 매개 변수의 기본값은 각각 "참가자"이 고, 현재 구독은 사용자가 두 매개 _note_ 변수 중 하나에 대 한 값을 제공 하는 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-125">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="a0dcb-126">또한 cmdlet은 응용 프로그램을 암시적으로 만들고 해당 속성 (ApplicationId이 제공 되지 않은 경우)을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-126">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="a0dcb-127">응용 프로그램별 매개 변수를 업데이트 하려면 Set-AzADApplication cmdlet을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-127">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="a0dcb-128">**새-AzADServicePrincipal** 명령을 사용 하 여 서비스 사용자를 만드는 경우 출력에는 보호 해야 하는 자격 증명이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-128">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="a0dcb-129">이러한 자격 증명을 코드에 포함 하지 않도록 하거나 자격 증명을 소스 제어에 체크 인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-129">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="a0dcb-130">다른 방법으로는 자격 증명을 사용할 필요가 없도록 [관리 되는 id](/azure/active-directory/managed-identities-azure-resources/overview) 를 사용 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="a0dcb-131">기본적으로 **AzADServicePrincipal** 는 구독 범위에서 [참가자](/azure/role-based-access-control/built-in-roles#contributor) 역할을 서비스 사용자에 게 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="a0dcb-132">손상 된 서비스 보안 주체의 위험을 줄이려면 더 구체적인 역할을 할당 하 고 리소스 또는 리소스 그룹으로 범위를 좁힙니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="a0dcb-133">자세한 내용은 [역할 할당을 추가 하는 단계를](/azure/role-based-access-control/role-assignments-steps) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="a0dcb-134">예제의</span><span class="sxs-lookup"><span data-stu-id="a0dcb-134">EXAMPLES</span></span>

### <span data-ttu-id="a0dcb-135">예제 1-간단한 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="a0dcb-135">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="a0dcb-136">위의 명령은 제공 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-136">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="a0dcb-137">응용 프로그램 id가 제공 되지 않았으므로 서비스 사용자를 위해 응용 프로그램이 생성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-137">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="a0dcb-138">Or에 대 한 값이 제공 되지 않았으므로 `Role` `Scope` 만든 서비스 주체에는 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-138">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="a0dcb-139">예제 2-지정 된 역할 및 기본 범위의 간단한 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="a0dcb-139">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

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

<span data-ttu-id="a0dcb-140">위의 명령은 제공 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-140">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="a0dcb-141">응용 프로그램 id가 제공 되지 않았으므로 서비스 사용자를 위해 응용 프로그램이 생성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-141">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="a0dcb-142">서비스 사용자가 현재 구독에 대해 "읽기" 권한으로 생성 되었습니다 (매개 변수에 대 한 값이 제공 되지 않았으므로 `Scope` ).</span><span class="sxs-lookup"><span data-stu-id="a0dcb-142">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="a0dcb-143">예제 3-지정 된 범위 및 기본 역할을 가진 간단한 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="a0dcb-143">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

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

<span data-ttu-id="a0dcb-144">위의 명령은 제공 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-144">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="a0dcb-145">응용 프로그램 id가 제공 되지 않았으므로 서비스 사용자를 위해 응용 프로그램이 생성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-145">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="a0dcb-146">제공 된 리소스 그룹 범위를 통해 서비스 사용자가 "참가자" 권한으로 생성 되었습니다 (매개 변수에 대 한 값이 제공 되지 않았으므로 `Role` ).</span><span class="sxs-lookup"><span data-stu-id="a0dcb-146">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="a0dcb-147">예제 4-단순 광고 서비스 주도자 만들기 지정 된 범위 및 역할</span><span class="sxs-lookup"><span data-stu-id="a0dcb-147">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

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

<span data-ttu-id="a0dcb-148">위의 명령은 제공 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-148">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="a0dcb-149">응용 프로그램 id가 제공 되지 않았으므로 서비스 사용자를 위해 응용 프로그램이 생성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-149">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="a0dcb-150">서비스 사용자가 제공 된 리소스 그룹 범위에 대해 "읽기" 권한을 사용 하 여 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-150">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="a0dcb-151">예제 5-역할을 할당 하 여 응용 프로그램 id를 사용 하 여 새 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="a0dcb-151">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="a0dcb-152">응용 프로그램 id가 ' 4a28ad2-3| 4-4a41-bc3b-d22ddf90000e ' 인 응용 프로그램에 대 한 새 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-152">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="a0dcb-153">Or에 대 한 값이 제공 되지 않았으므로 `Role` `Scope` 만든 서비스 주체에는 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-153">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="a0dcb-154">예제 6-파이핑을 사용 하 여 새 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="a0dcb-154">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="a0dcb-155">개체 id가 ' 3ede3c26-b443-4e0b-9efc-b05e68338dc3 ' 인 응용 프로그램을 가져오고 해당 응용 프로그램에 대 한 새 광고 서비스 사용자를 만들기 위해 New-AzADServicePrincipal cmdlet에 대 한 파이프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-155">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

### <span data-ttu-id="a0dcb-156">예제 7-DisplayName 및 password 자격 증명을 사용 하 여 새 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="a0dcb-156">Example 7 - Create a new AD service principal using DisplayName and password credential</span></span>

```
PS C:\> $credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password="StrongPassworld!23"}
PS C:\> $sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials

ServicePrincipalNames : {exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc, http://ServicePrincipalName}
ApplicationId         : exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxcc
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 6xxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxb
Type                  :
```

<span data-ttu-id="a0dcb-157">이름이 "ServicePrincipalName"이 고 암호가 "StrongPassworld! 23" 인 새 응용 프로그램을 만들고 방금 만든 응용 프로그램을 기반으로 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-157">Creates a new application with name "ServicePrincipalName" and password "StrongPassworld!23" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="a0dcb-158">시작 날짜 및 종료 날짜가 암호 자격 증명에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-158">The start date and end date are added to password credential.</span></span>

### <span data-ttu-id="a0dcb-159">예제 8-DisplayName 및 일반 키 자격 증명을 사용 하 여 새 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="a0dcb-159">Example 8 - Create a new AD service principal using DisplayName and plain key credential</span></span>

```
PS C:\> $cert = <public certificate as base64-encoded string>
PS C:\> $sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate "2021-01-01"

ServicePrincipalNames : {cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6, http://ServicePrincipalName}
ApplicationId         : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc
Type                  :
```

<span data-ttu-id="a0dcb-160">이름이 "ServicePrincipalName"이 고 certifcate "$cert" 인 새 응용 프로그램을 만들고 방금 만든 응용 프로그램을 기반으로 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-160">Creates a new application with name "ServicePrincipalName" and certifcate "$cert" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="a0dcb-161">끝 날짜가 키 자격 증명에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-161">The end date is added to key credential.</span></span>

## <span data-ttu-id="a0dcb-162">변수</span><span class="sxs-lookup"><span data-stu-id="a0dcb-162">PARAMETERS</span></span>

### <span data-ttu-id="a0dcb-163">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a0dcb-163">-ApplicationId</span></span>
<span data-ttu-id="a0dcb-164">테 넌 트의 서비스 사용자에 대 한 고유한 응용 프로그램 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-164">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="a0dcb-165">만든 후에는이 속성을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-165">Once created this property cannot be changed.</span></span>
<span data-ttu-id="a0dcb-166">응용 프로그램 id가 지정 되지 않은 경우 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-166">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="a0dcb-167">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="a0dcb-167">-ApplicationObject</span></span>
<span data-ttu-id="a0dcb-168">서비스 사용자를 만들 응용 프로그램을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-168">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="a0dcb-169">-CertValue</span><span class="sxs-lookup"><span data-stu-id="a0dcb-169">-CertValue</span></span>
<span data-ttu-id="a0dcb-170">"비대칭" 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-170">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="a0dcb-171">Base 64 인코딩된 인증서를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-171">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="a0dcb-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0dcb-172">-DefaultProfile</span></span>
<span data-ttu-id="a0dcb-173">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a0dcb-173">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0dcb-174">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a0dcb-174">-DisplayName</span></span>
<span data-ttu-id="a0dcb-175">서비스 사용자의 식별 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-175">The friendly name of the service principal.</span></span> <span data-ttu-id="a0dcb-176">표시 이름이 제공 되지 않은 경우이 값은 기본적으로 ' azure-powershell-MM-dd-yyyy-mm-dd-ss ' 이며, 여기서 접미사는 응용 프로그램을 만드는 데 걸리는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-176">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="a0dcb-177">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a0dcb-177">-EndDate</span></span>
<span data-ttu-id="a0dcb-178">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-178">The effective end date of the credential usage.</span></span>
<span data-ttu-id="a0dcb-179">기본 끝 날짜 값은 오늘부터 1 년입니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-179">The default end date value is one year from today.</span></span> <span data-ttu-id="a0dcb-180">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 이전으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-180">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="a0dcb-181">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="a0dcb-181">-KeyCredential</span></span>
<span data-ttu-id="a0dcb-182">응용 프로그램과 연결 된 키 자격 증명의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-182">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="a0dcb-183">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="a0dcb-183">-PasswordCredential</span></span>
<span data-ttu-id="a0dcb-184">응용 프로그램과 연결 된 암호 자격 증명 모음입니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-184">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="a0dcb-185">-역할</span><span class="sxs-lookup"><span data-stu-id="a0dcb-185">-Role</span></span>
<span data-ttu-id="a0dcb-186">서비스 사용자가 범위를 초과 하는 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-186">The role that the service principal has over the scope.</span></span> <span data-ttu-id="a0dcb-187">값이 `Scope` 제공 되지만 값이 제공 되지 않으면 `Role` 기본적으로 `Role` ' 참가자 ' 역할이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-187">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="a0dcb-188">-범위</span><span class="sxs-lookup"><span data-stu-id="a0dcb-188">-Scope</span></span>
<span data-ttu-id="a0dcb-189">서비스 사용자에 게 사용 권한이 있는 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-189">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="a0dcb-190">값이 `Role` 제공 되지만 값이 제공 되지 않으면 `Scope` `Scope` 현재 구독이 기본값으로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-190">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="a0dcb-191">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="a0dcb-191">-SkipAssignment</span></span>
<span data-ttu-id="a0dcb-192">설정 하는 경우 서비스 사용자에 대 한 기본 역할 할당 만들기를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-192">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="a0dcb-193">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="a0dcb-193">-StartDate</span></span>
<span data-ttu-id="a0dcb-194">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-194">The effective start date of the credential usage.</span></span>
<span data-ttu-id="a0dcb-195">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-195">The default start date value is today.</span></span> <span data-ttu-id="a0dcb-196">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후에이를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-196">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="a0dcb-197">-확인</span><span class="sxs-lookup"><span data-stu-id="a0dcb-197">-Confirm</span></span>
<span data-ttu-id="a0dcb-198">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-198">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0dcb-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0dcb-199">-WhatIf</span></span>
<span data-ttu-id="a0dcb-200">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-200">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0dcb-201">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-201">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0dcb-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0dcb-202">CommonParameters</span></span>
<span data-ttu-id="a0dcb-203">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0dcb-204">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-204">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0dcb-205">입력</span><span class="sxs-lookup"><span data-stu-id="a0dcb-205">INPUTS</span></span>

### <span data-ttu-id="a0dcb-206">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="a0dcb-206">System.Guid</span></span>

### <span data-ttu-id="a0dcb-207">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a0dcb-207">System.String</span></span>

### <span data-ttu-id="a0dcb-208">ActiveDirectory PSADApplication 프로그램</span><span class="sxs-lookup"><span data-stu-id="a0dcb-208">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="a0dcb-209">ActiveDirectory PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="a0dcb-209">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="a0dcb-210">ActiveDirectory PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="a0dcb-210">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="a0dcb-211">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="a0dcb-211">System.DateTime</span></span>

## <span data-ttu-id="a0dcb-212">출력</span><span class="sxs-lookup"><span data-stu-id="a0dcb-212">OUTPUTS</span></span>

### <span data-ttu-id="a0dcb-213">ActiveDirectory PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a0dcb-213">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="a0dcb-214">PSADServicePrincipalWrapper에 대 한 권한 부여.</span><span class="sxs-lookup"><span data-stu-id="a0dcb-214">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="a0dcb-215">상속자</span><span class="sxs-lookup"><span data-stu-id="a0dcb-215">NOTES</span></span>
<span data-ttu-id="a0dcb-216">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="a0dcb-216">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a0dcb-217">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0dcb-217">RELATED LINKS</span></span>

[<span data-ttu-id="a0dcb-218">제거-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a0dcb-218">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="a0dcb-219">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a0dcb-219">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="a0dcb-220">새로운 AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a0dcb-220">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="a0dcb-221">제거-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a0dcb-221">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="a0dcb-222">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a0dcb-222">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="a0dcb-223">새로운 AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a0dcb-223">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="a0dcb-224">제거-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a0dcb-224">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

