---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: aa46a09eec134797f1dcacfeb0541769c4569e9e
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251814"
---
# <span data-ttu-id="c875f-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c875f-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="c875f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c875f-102">SYNOPSIS</span></span>
<span data-ttu-id="c875f-103">새 Azure Active Directory 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="c875f-104">구문</span><span class="sxs-lookup"><span data-stu-id="c875f-104">SYNTAX</span></span>

### <span data-ttu-id="c875f-105">SimpleParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c875f-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c875f-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c875f-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c875f-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="c875f-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c875f-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c875f-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c875f-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="c875f-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c875f-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c875f-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c875f-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c875f-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c875f-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="c875f-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c875f-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c875f-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c875f-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="c875f-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c875f-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c875f-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c875f-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c875f-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c875f-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="c875f-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c875f-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c875f-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c875f-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="c875f-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c875f-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c875f-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c875f-121">설명</span><span class="sxs-lookup"><span data-stu-id="c875f-121">DESCRIPTION</span></span>
<span data-ttu-id="c875f-122">새 Azure Active Directory 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="c875f-123">사용자가 매개 변수를 제공하지 않는 경우 기본 매개 변수 집합은 매개 변수에 대한 기본값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="c875f-124">사용되는 기본값에 대한 자세한 내용은 아래 제공된 매개 변수에 대한 설명을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c875f-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="c875f-125">이 cmdlet에는 매개 변수 및 매개 변수를 사용하여 서비스 주체에 역할을 할당할 수 있습니다. 이러한 매개 변수가 제공되지 않은 경우 서비스 주체에 역할이 `Role` `Scope` 할당되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="c875f-126">매개 변수 및 매개 변수의 기본값은 각각 "기여자" 및 현재 구독입니다(참고: 기본값은 사용자가 두 매개 변수 중 하나에 값을 제공하는 경우만 사용되지만 다른 하나는 제공되지 `Role` `Scope` 않습니다).</span><span class="sxs-lookup"><span data-stu-id="c875f-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively (_note_: the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="c875f-127">또한 cmdlet은 암시적으로 애플리케이션을 만들고 해당 속성을 설정합니다(ApplicationId가 제공되지 않은 경우).</span><span class="sxs-lookup"><span data-stu-id="c875f-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="c875f-128">애플리케이션 특정 매개 변수를 업데이트하기 위해 Set-AzADApplication cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-128">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="c875f-129">**New-AzADServicePrincipal** 명령을 사용하여 서비스 주체를 만들 때 출력에는 보호해야 하는 자격 증명이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="c875f-130">또는 관리 ID를 [](/azure/active-directory/managed-identities-azure-resources/overview) 사용하여 자격 증명을 사용할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="c875f-131">기본적으로 **New-AzADServicePrincipal은** 구독 [](/azure/role-based-access-control/built-in-roles#contributor) 범위의 서비스 주체에 기여자 역할을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="c875f-132">손상된 서비스 주체의 위험을 줄이기 위해 보다 구체적인 역할을 할당하고 리소스 또는 리소스 그룹으로 범위를 좁힐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="c875f-133">자세한 [내용은 역할 할당을 추가하는](/azure/role-based-access-control/role-assignments-steps) 단계를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c875f-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="c875f-134">예제</span><span class="sxs-lookup"><span data-stu-id="c875f-134">EXAMPLES</span></span>

### <span data-ttu-id="c875f-135">예제 1 - 간단한 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="c875f-135">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="c875f-136">위의 명령은 제공되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-136">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="c875f-137">애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-137">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="c875f-138">값이 제공되지 않은 경우 또는 생성된 서비스 `Role` `Scope` 주체에는 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-138">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="c875f-139">예제 2 - 지정된 역할 및 기본 범위를 통해 간단한 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="c875f-139">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

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

<span data-ttu-id="c875f-140">위의 명령은 제공되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-140">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="c875f-141">애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-141">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="c875f-142">매개 변수에 대한 값이 제공되지 않았습니다. 현재 구독에 대한 "읽기 권한자" 권한으로 서비스 주체가 `Scope` 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-142">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="c875f-143">예제 3 - 지정된 범위 및 기본 역할을 통해 간단한 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="c875f-143">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

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

<span data-ttu-id="c875f-144">위의 명령은 제공되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-144">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="c875f-145">애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-145">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="c875f-146">제공된 리소스 그룹 범위에 대해 "기여자" 권한(매개 변수에 대한 값이 제공되지 아니기 때문에)을 사용하여 서비스 `Role` 주체가 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-146">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="c875f-147">예제 4 - 지정된 범위 및 역할을 통해 간단한 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="c875f-147">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

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

<span data-ttu-id="c875f-148">위의 명령은 제공되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-148">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="c875f-149">애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-149">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="c875f-150">제공된 리소스 그룹 범위에 대한 "읽기 권한자" 권한으로 서비스 주체가 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-150">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="c875f-151">예제 5 - 역할 할당과 함께 애플리케이션 ID를 사용하여 새 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="c875f-151">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="c875f-152">애플리케이션 ID '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'를 통해 애플리케이션에 대한 새 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-152">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="c875f-153">값이 제공되지 않은 경우 또는 생성된 서비스 `Role` `Scope` 주체에는 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-153">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="c875f-154">예제 6 - 파이핑을 사용하여 새 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="c875f-154">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="c875f-155">개체 ID가 '3ede3c26-b443-4e0b-9efc-b05e68338dc3'인 애플리케이션을 만들고 New-AzADServicePrincipal cmdlet에 파이프하여 해당 애플리케이션에 대한 새 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-155">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="c875f-156">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c875f-156">PARAMETERS</span></span>

### <span data-ttu-id="c875f-157">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c875f-157">-ApplicationId</span></span>
<span data-ttu-id="c875f-158">테넌트의 서비스 주체에 대한 고유한 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-158">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="c875f-159">만든 후 이 속성을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-159">Once created this property cannot be changed.</span></span>
<span data-ttu-id="c875f-160">애플리케이션 ID를 지정하지 않으면 애플리케이션 ID가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-160">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="c875f-161">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="c875f-161">-ApplicationObject</span></span>
<span data-ttu-id="c875f-162">서비스 주체가 생성되는 애플리케이션을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-162">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="c875f-163">-CertValue</span><span class="sxs-lookup"><span data-stu-id="c875f-163">-CertValue</span></span>
<span data-ttu-id="c875f-164">"비대칭" 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-164">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="c875f-165">기본 64로 인코딩된 인증서를 나타났습니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-165">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="c875f-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c875f-166">-DefaultProfile</span></span>
<span data-ttu-id="c875f-167">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c875f-167">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c875f-168">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c875f-168">-DisplayName</span></span>
<span data-ttu-id="c875f-169">서비스 주체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-169">The friendly name of the service principal.</span></span> <span data-ttu-id="c875f-170">표시 이름을 지정하지 않은 경우 이 값은 기본적으로 'azure-powershell-MM-dd-yy-HH-mm-ss'로 설정됩니다. 여기서 접미사는 애플리케이션을 만들 때입니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-170">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="c875f-171">-EndDate</span><span class="sxs-lookup"><span data-stu-id="c875f-171">-EndDate</span></span>
<span data-ttu-id="c875f-172">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-172">The effective end date of the credential usage.</span></span>
<span data-ttu-id="c875f-173">기본 종료 날짜 값은 오늘부터 1년입니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-173">The default end date value is one year from today.</span></span> <span data-ttu-id="c875f-174">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이전으로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-174">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="c875f-175">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="c875f-175">-KeyCredential</span></span>
<span data-ttu-id="c875f-176">애플리케이션과 연결된 키 자격 증명의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-176">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="c875f-177">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="c875f-177">-PasswordCredential</span></span>
<span data-ttu-id="c875f-178">애플리케이션과 연결된 암호 자격 증명의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-178">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="c875f-179">-Role</span><span class="sxs-lookup"><span data-stu-id="c875f-179">-Role</span></span>
<span data-ttu-id="c875f-180">서비스 주체가 범위를 통해 있는 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-180">The role that the service principal has over the scope.</span></span> <span data-ttu-id="c875f-181">값이 제공되지만 값이 제공되지 않습니다. 그러면 기본적으로 `Scope` `Role` `Role` '기여자' 역할이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-181">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="c875f-182">-Scope</span><span class="sxs-lookup"><span data-stu-id="c875f-182">-Scope</span></span>
<span data-ttu-id="c875f-183">서비스 주체에 권한이 있는 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-183">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="c875f-184">값이 제공되지만 값이 제공되지 않습니다. 그러면 현재 구독이 `Role` `Scope` `Scope` 기본값으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-184">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="c875f-185">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="c875f-185">-SkipAssignment</span></span>
<span data-ttu-id="c875f-186">설정된 경우 서비스 주체에 대한 기본 역할 할당 만들기를 건너뜁습니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-186">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="c875f-187">-StartDate</span><span class="sxs-lookup"><span data-stu-id="c875f-187">-StartDate</span></span>
<span data-ttu-id="c875f-188">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-188">The effective start date of the credential usage.</span></span>
<span data-ttu-id="c875f-189">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-189">The default start date value is today.</span></span> <span data-ttu-id="c875f-190">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-190">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="c875f-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c875f-191">-Confirm</span></span>
<span data-ttu-id="c875f-192">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c875f-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c875f-193">-WhatIf</span></span>
<span data-ttu-id="c875f-194">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c875f-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c875f-195">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c875f-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c875f-196">CommonParameters</span></span>
<span data-ttu-id="c875f-197">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c875f-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c875f-198">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c875f-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c875f-199">입력</span><span class="sxs-lookup"><span data-stu-id="c875f-199">INPUTS</span></span>

### <span data-ttu-id="c875f-200">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c875f-200">System.Guid</span></span>

### <span data-ttu-id="c875f-201">System.String</span><span class="sxs-lookup"><span data-stu-id="c875f-201">System.String</span></span>

### <span data-ttu-id="c875f-202">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c875f-202">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="c875f-203">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="c875f-203">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="c875f-204">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="c875f-204">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="c875f-205">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="c875f-205">System.DateTime</span></span>

## <span data-ttu-id="c875f-206">출력</span><span class="sxs-lookup"><span data-stu-id="c875f-206">OUTPUTS</span></span>

### <span data-ttu-id="c875f-207">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c875f-207">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="c875f-208">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="c875f-208">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="c875f-209">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c875f-209">NOTES</span></span>
<span data-ttu-id="c875f-210">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="c875f-210">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c875f-211">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c875f-211">RELATED LINKS</span></span>

[<span data-ttu-id="c875f-212">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c875f-212">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="c875f-213">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c875f-213">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="c875f-214">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c875f-214">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="c875f-215">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c875f-215">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="c875f-216">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c875f-216">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="c875f-217">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c875f-217">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="c875f-218">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c875f-218">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

