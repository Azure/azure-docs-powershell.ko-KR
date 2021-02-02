---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 3a410dfb43cc767b0a73086147042425d42764d1
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251627"
---
# <span data-ttu-id="b2e1b-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b2e1b-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="b2e1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e1b-103">새 Azure Active Directory 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="b2e1b-104">구문</span><span class="sxs-lookup"><span data-stu-id="b2e1b-104">SYNTAX</span></span>

### <span data-ttu-id="b2e1b-105">SimpleParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b2e1b-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2e1b-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2e1b-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2e1b-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2e1b-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2e1b-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2e1b-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2e1b-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2e1b-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2e1b-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2e1b-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2e1b-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2e1b-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2e1b-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2e1b-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2e1b-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2e1b-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2e1b-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2e1b-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2e1b-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2e1b-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2e1b-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2e1b-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2e1b-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2e1b-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2e1b-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2e1b-118">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2e1b-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2e1b-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2e1b-120">설명</span><span class="sxs-lookup"><span data-stu-id="b2e1b-120">DESCRIPTION</span></span>
<span data-ttu-id="b2e1b-121">새 Azure Active Directory 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-121">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="b2e1b-122">사용자가 매개 변수를 제공하지 않는 경우 기본 매개 변수 집합은 매개 변수에 대한 기본값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-122">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="b2e1b-123">사용되는 기본값에 대한 자세한 내용은 아래 제공된 매개 변수에 대한 설명을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-123">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="b2e1b-124">이 cmdlet에는 매개 변수 및 매개 변수를 사용하여 서비스 주체에 역할을 할당할 수 있습니다. 이러한 매개 변수가 제공되지 않은 경우 서비스 주체에 역할이 `Role` `Scope` 할당되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-124">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="b2e1b-125">매개 변수 및 매개 변수의 기본값은 각각 "기여자" 및 현재 구독입니다(참고: 기본값은 사용자가 두 매개 변수 중 하나에 값을 제공하는 경우만 사용되지만 다른 하나는 제공되지 `Role` `Scope` 않습니다).</span><span class="sxs-lookup"><span data-stu-id="b2e1b-125">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively (_note_: the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="b2e1b-126">또한 cmdlet은 암시적으로 애플리케이션을 만들고 해당 속성을 설정합니다(ApplicationId가 제공되지 않은 경우).</span><span class="sxs-lookup"><span data-stu-id="b2e1b-126">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="b2e1b-127">애플리케이션 특정 매개 변수를 업데이트하기 위해 Set-AzADApplication cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-127">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="b2e1b-128">**New-AzADServicePrincipal** 명령을 사용하여 서비스 주체를 만들 때 출력에는 보호해야 하는 자격 증명이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-128">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="b2e1b-129">또는 관리 ID를 [](/azure/active-directory/managed-identities-azure-resources/overview) 사용하여 자격 증명을 사용할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-129">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="b2e1b-130">기본적으로 **New-AzADServicePrincipal은** 구독 [](/azure/role-based-access-control/built-in-roles#contributor) 범위의 서비스 주체에 기여자 역할을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-130">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="b2e1b-131">손상된 서비스 주체의 위험을 줄이기 위해 보다 구체적인 역할을 할당하고 리소스 또는 리소스 그룹으로 범위를 좁힐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-131">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="b2e1b-132">자세한 [내용은 역할 할당을 추가하는](/azure/role-based-access-control/role-assignments-steps) 단계를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-132">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="b2e1b-133">예제</span><span class="sxs-lookup"><span data-stu-id="b2e1b-133">EXAMPLES</span></span>

### <span data-ttu-id="b2e1b-134">예제 1 - 간단한 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="b2e1b-134">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="b2e1b-135">위의 명령은 제공되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-135">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="b2e1b-136">애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-136">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="b2e1b-137">값이 제공되지 않은 경우 또는 생성된 서비스 `Role` `Scope` 주체에는 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-137">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="b2e1b-138">예제 2 - 지정된 역할 및 기본 범위를 통해 간단한 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="b2e1b-138">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

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

<span data-ttu-id="b2e1b-139">위의 명령은 제공되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-139">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="b2e1b-140">애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-140">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="b2e1b-141">매개 변수에 대한 값이 제공되지 않았습니다. 현재 구독에 대한 "읽기 권한자" 권한으로 서비스 주체가 `Scope` 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-141">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="b2e1b-142">예제 3 - 지정된 범위 및 기본 역할을 통해 간단한 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="b2e1b-142">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

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

<span data-ttu-id="b2e1b-143">위의 명령은 제공되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-143">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="b2e1b-144">애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-144">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="b2e1b-145">제공된 리소스 그룹 범위에 대해 "기여자" 권한(매개 변수에 대한 값이 제공되지 아니기 때문에)을 사용하여 서비스 `Role` 주체가 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-145">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="b2e1b-146">예제 4 - 지정된 범위 및 역할을 통해 간단한 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="b2e1b-146">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

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

<span data-ttu-id="b2e1b-147">위의 명령은 제공되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-147">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="b2e1b-148">애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-148">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="b2e1b-149">제공된 리소스 그룹 범위에 대한 "읽기 권한자" 권한으로 서비스 주체가 생성되었습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-149">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="b2e1b-150">예제 5 - 역할 할당과 함께 애플리케이션 ID를 사용하여 새 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="b2e1b-150">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="b2e1b-151">애플리케이션 ID '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'를 통해 애플리케이션에 대한 새 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-151">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="b2e1b-152">값이 제공되지 않은 경우 또는 생성된 서비스 `Role` `Scope` 주체에는 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-152">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="b2e1b-153">예제 6 - 파이핑을 사용하여 새 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="b2e1b-153">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="b2e1b-154">개체 ID가 '3ede3c26-b443-4e0b-9efc-b05e68338dc3'인 애플리케이션을 만들고 New-AzADServicePrincipal cmdlet에 파이프하여 해당 애플리케이션에 대한 새 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-154">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

### <span data-ttu-id="b2e1b-155">예제 7 - DisplayName 및 암호 자격 증명을 사용하여 새 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="b2e1b-155">Example 7 - Create a new AD service principal using DisplayName and password credential</span></span>

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

<span data-ttu-id="b2e1b-156">"ServicePrincipalName" 및 암호 "StrongPassworld!23"을 사용하여 새 애플리케이션을 만들고 방금 만든 애플리케이션을 기반으로 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-156">Creates a new application with name "ServicePrincipalName" and password "StrongPassworld!23" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="b2e1b-157">시작 날짜 및 종료 날짜가 암호 자격 증명에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-157">The start date and end date are added to password credential.</span></span>

### <span data-ttu-id="b2e1b-158">예제 8 - DisplayName 및 일반 키 자격 증명을 사용하여 새 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="b2e1b-158">Example 8 - Create a new AD service principal using DisplayName and plain key credential</span></span>

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

<span data-ttu-id="b2e1b-159">이름이 "ServicePrincipalName"인 새 애플리케이션을 만들고 "$cert"를 인증하고 방금 만든 애플리케이션을 기반으로 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-159">Creates a new application with name "ServicePrincipalName" and certifcate "$cert" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="b2e1b-160">종료 날짜가 키 자격 증명에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-160">The end date is added to key credential.</span></span>

## <span data-ttu-id="b2e1b-161">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2e1b-161">PARAMETERS</span></span>

### <span data-ttu-id="b2e1b-162">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b2e1b-162">-ApplicationId</span></span>
<span data-ttu-id="b2e1b-163">테넌트의 서비스 주체에 대한 고유한 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-163">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="b2e1b-164">만든 후 이 속성을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-164">Once created this property cannot be changed.</span></span>
<span data-ttu-id="b2e1b-165">애플리케이션 ID를 지정하지 않으면 애플리케이션 ID가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-165">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="b2e1b-166">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="b2e1b-166">-ApplicationObject</span></span>
<span data-ttu-id="b2e1b-167">서비스 주체가 생성되는 애플리케이션을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-167">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="b2e1b-168">-CertValue</span><span class="sxs-lookup"><span data-stu-id="b2e1b-168">-CertValue</span></span>
<span data-ttu-id="b2e1b-169">"비대칭" 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-169">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="b2e1b-170">기본 64로 인코딩된 인증서를 나타났습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-170">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="b2e1b-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e1b-171">-DefaultProfile</span></span>
<span data-ttu-id="b2e1b-172">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b2e1b-172">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2e1b-173">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b2e1b-173">-DisplayName</span></span>
<span data-ttu-id="b2e1b-174">서비스 주체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-174">The friendly name of the service principal.</span></span> <span data-ttu-id="b2e1b-175">표시 이름을 지정하지 않은 경우 이 값은 기본적으로 'azure-powershell-MM-dd-yy-HH-mm-ss'로 설정됩니다. 여기서 접미사는 애플리케이션을 만들 때입니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-175">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="b2e1b-176">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b2e1b-176">-EndDate</span></span>
<span data-ttu-id="b2e1b-177">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-177">The effective end date of the credential usage.</span></span>
<span data-ttu-id="b2e1b-178">기본 종료 날짜 값은 오늘부터 1년입니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-178">The default end date value is one year from today.</span></span> <span data-ttu-id="b2e1b-179">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이전으로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-179">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="b2e1b-180">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="b2e1b-180">-KeyCredential</span></span>
<span data-ttu-id="b2e1b-181">애플리케이션과 연결된 키 자격 증명의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-181">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="b2e1b-182">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="b2e1b-182">-PasswordCredential</span></span>
<span data-ttu-id="b2e1b-183">애플리케이션과 연결된 암호 자격 증명의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-183">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="b2e1b-184">-Role</span><span class="sxs-lookup"><span data-stu-id="b2e1b-184">-Role</span></span>
<span data-ttu-id="b2e1b-185">서비스 주체가 범위를 통해 있는 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-185">The role that the service principal has over the scope.</span></span> <span data-ttu-id="b2e1b-186">값이 제공되지만 값이 제공되지 않습니다. 그러면 기본적으로 `Scope` `Role` `Role` '기여자' 역할이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-186">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="b2e1b-187">-Scope</span><span class="sxs-lookup"><span data-stu-id="b2e1b-187">-Scope</span></span>
<span data-ttu-id="b2e1b-188">서비스 주체에 권한이 있는 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-188">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="b2e1b-189">값이 제공되지만 값이 제공되지 않습니다. 그러면 현재 구독이 `Role` `Scope` `Scope` 기본값으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-189">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="b2e1b-190">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="b2e1b-190">-SkipAssignment</span></span>
<span data-ttu-id="b2e1b-191">설정된 경우 서비스 주체에 대한 기본 역할 할당 만들기를 건너뜁습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-191">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="b2e1b-192">-StartDate</span><span class="sxs-lookup"><span data-stu-id="b2e1b-192">-StartDate</span></span>
<span data-ttu-id="b2e1b-193">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-193">The effective start date of the credential usage.</span></span>
<span data-ttu-id="b2e1b-194">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-194">The default start date value is today.</span></span> <span data-ttu-id="b2e1b-195">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-195">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="b2e1b-196">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2e1b-196">-Confirm</span></span>
<span data-ttu-id="b2e1b-197">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2e1b-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2e1b-198">-WhatIf</span></span>
<span data-ttu-id="b2e1b-199">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b2e1b-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2e1b-200">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2e1b-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e1b-201">CommonParameters</span></span>
<span data-ttu-id="b2e1b-202">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e1b-203">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b2e1b-203">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e1b-204">입력</span><span class="sxs-lookup"><span data-stu-id="b2e1b-204">INPUTS</span></span>

### <span data-ttu-id="b2e1b-205">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b2e1b-205">System.Guid</span></span>

### <span data-ttu-id="b2e1b-206">System.String</span><span class="sxs-lookup"><span data-stu-id="b2e1b-206">System.String</span></span>

### <span data-ttu-id="b2e1b-207">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="b2e1b-207">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="b2e1b-208">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="b2e1b-208">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="b2e1b-209">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="b2e1b-209">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="b2e1b-210">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="b2e1b-210">System.DateTime</span></span>

## <span data-ttu-id="b2e1b-211">출력</span><span class="sxs-lookup"><span data-stu-id="b2e1b-211">OUTPUTS</span></span>

### <span data-ttu-id="b2e1b-212">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b2e1b-212">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="b2e1b-213">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="b2e1b-213">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="b2e1b-214">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b2e1b-214">NOTES</span></span>
<span data-ttu-id="b2e1b-215">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="b2e1b-215">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b2e1b-216">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2e1b-216">RELATED LINKS</span></span>

[<span data-ttu-id="b2e1b-217">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b2e1b-217">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="b2e1b-218">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b2e1b-218">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="b2e1b-219">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b2e1b-219">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="b2e1b-220">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b2e1b-220">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="b2e1b-221">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b2e1b-221">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="b2e1b-222">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b2e1b-222">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="b2e1b-223">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b2e1b-223">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

