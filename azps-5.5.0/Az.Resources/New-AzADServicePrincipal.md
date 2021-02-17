---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: e7c77dc4daf38634e7661f4579dd5bbcc81d0443
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208493"
---
# <span data-ttu-id="9ad7e-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9ad7e-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="9ad7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ad7e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ad7e-103">새 Azure Active Directory 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="9ad7e-104">구문</span><span class="sxs-lookup"><span data-stu-id="9ad7e-104">SYNTAX</span></span>

### <span data-ttu-id="9ad7e-105">SimpleParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9ad7e-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad7e-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad7e-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ad7e-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad7e-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad7e-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad7e-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad7e-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad7e-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad7e-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad7e-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad7e-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad7e-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ad7e-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad7e-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad7e-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad7e-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad7e-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad7e-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad7e-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad7e-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad7e-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad7e-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad7e-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad7e-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad7e-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad7e-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ad7e-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ad7e-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ad7e-120">설명</span><span class="sxs-lookup"><span data-stu-id="9ad7e-120">DESCRIPTION</span></span>

<span data-ttu-id="9ad7e-121">새 Azure Active Directory 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="9ad7e-122">기본 매개 변수 집합은 매개 변수가 제공되지 않은 경우 기본값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="9ad7e-123">기본값에 대한 자세한 내용은 각 매개 변수에 대한 설명을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="9ad7e-124">이 cmdlet에는 역할 및 범위 매개 변수를 사용하여 서비스 주체에 역할을 **할당할** **수** 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="9ad7e-125">둘 다 생략하면 기여자 역할이 서비스 주체에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="9ad7e-126">역할 및 범위  매개  변수의 기본값은 현재 **구독에 대한** 참가자입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="9ad7e-127">이 cmdlet은 애플리케이션을 만들고 ApplicationId가 제공되지 않은 경우 해당 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="9ad7e-128">애플리케이션별 매개 변수를 업데이트하기 위해 [Update-AzADApplication](./update-azadapplication.md) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="9ad7e-129">**New-AzADServicePrincipal** 명령을 사용하여 서비스 주체를 만들 때 출력에는 보호해야 하는 자격 증명이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="9ad7e-130">또는 관리 ID를 [](/azure/active-directory/managed-identities-azure-resources/overview) 사용하여 자격 증명을 사용할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="9ad7e-131">기본적으로 **New-AzADServicePrincipal은** 구독 [](/azure/role-based-access-control/built-in-roles#contributor) 범위의 서비스 주체에 기여자 역할을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="9ad7e-132">손상된 서비스 주체의 위험을 줄이기 위해 보다 구체적인 역할을 할당하고 리소스 또는 리소스 그룹으로 범위를 좁힐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="9ad7e-133">자세한 [내용은 역할 할당을 추가하는](/azure/role-based-access-control/role-assignments-steps) 단계를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="9ad7e-134">예제</span><span class="sxs-lookup"><span data-stu-id="9ad7e-134">EXAMPLES</span></span>

### <span data-ttu-id="9ad7e-135">예제 1: 간단한 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="9ad7e-135">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="9ad7e-136">다음 예제에서는 지정되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-136">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="9ad7e-137">애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-137">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="9ad7e-138">역할 또는 범위에 대한 값이 제공되지 않습니다.  생성된 서비스 주체에는 현재 구독에 대한 참가자 역할이 할당됩니다. </span><span class="sxs-lookup"><span data-stu-id="9ad7e-138">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="9ad7e-139">예제 2: 지정된 역할 및 기본 범위를 통해 간단한 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="9ad7e-139">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="9ad7e-140">다음 예제에서는 지정되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-140">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="9ad7e-141">애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-141">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="9ad7e-142">범위 매개 변수에  대한 값이 제공되지 않고 현재 구독에 대한 읽기 권한자 권한으로 서비스 **주체가** 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-142">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

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

### <span data-ttu-id="9ad7e-143">예제 3: 지정된 범위 및 기본 역할로 간단한 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="9ad7e-143">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="9ad7e-144">다음 예제에서는 지정되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-144">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="9ad7e-145">애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-145">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="9ad7e-146">서비스 주체는  역할 매개 변수에 대한 값이 제공되지 않고 제공된 리소스 그룹 범위에 대한 참가자 권한으로 **만들어집니다.**</span><span class="sxs-lookup"><span data-stu-id="9ad7e-146">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

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

### <span data-ttu-id="9ad7e-147">예제 4: 지정된 범위 및 역할을 통해 간단한 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="9ad7e-147">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="9ad7e-148">다음 예제에서는 지정되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-148">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="9ad7e-149">애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-149">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="9ad7e-150">서비스 주체는 제공된 리소스 그룹 **범위에 대한 읽기** 권한자 권한으로 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-150">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

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

### <span data-ttu-id="9ad7e-151">예제 5: 역할 할당과 함께 애플리케이션 ID를 사용하여 새 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="9ad7e-151">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="9ad7e-152">다음 예제에서는 애플리케이션 ID가 '000000000-0000-0000-0000-0000-000000000000'인 애플리케이션에 대한 새 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-152">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="9ad7e-153">역할 또는 범위에 대한 값이 제공되지 않습니다.  생성된 서비스 주체에는 현재 구독에 대한 참가자 역할이 할당됩니다. </span><span class="sxs-lookup"><span data-stu-id="9ad7e-153">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="9ad7e-154">예제 6: 파이핑을 사용하여 새 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="9ad7e-154">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="9ad7e-155">다음 예제에서는 [Get-AzADApplication](./get-azadapplication.md) cmdlet을 사용하여 개체 ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3'을 사용하여 애플리케이션을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-155">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="9ad7e-156">결과는 cmdlet에 파이프하여 애플리케이션에 대한 새 AD 서비스 `New-AzADServicePrincipal` 주체를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-156">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="9ad7e-157">예제 7: DisplayName 및 암호 자격 증명을 사용하여 새 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="9ad7e-157">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="9ad7e-158">다음 예제에서는 **ServicePrincipalName** 이름과 **StrongPassworld!23의** 암호를 사용하여 새 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-158">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="9ad7e-159">생성된 애플리케이션을 기반으로 서비스 주체가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-159">It creates the service principal based on the created application.</span></span> <span data-ttu-id="9ad7e-160">시작 날짜 및 종료 날짜가 암호 자격 증명에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-160">The start date and end date are added to the password credential.</span></span>

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

### <span data-ttu-id="9ad7e-161">예제 8: DisplayName 및 일반 키 자격 증명을 사용하여 새 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="9ad7e-161">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="9ad7e-162">다음 예제에서는 **ServicePrincipalName** 이름과 인증서 이름을 지정하여 새 애플리케이션을 **$cert.** 만든 애플리케이션을 기반으로 서비스 주체가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-162">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="9ad7e-163">종료 날짜가 키 자격 증명에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-163">The end date is added to key credential.</span></span>

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

## <span data-ttu-id="9ad7e-164">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ad7e-164">PARAMETERS</span></span>

### <span data-ttu-id="9ad7e-165">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9ad7e-165">-ApplicationId</span></span>

<span data-ttu-id="9ad7e-166">테넌트의 서비스 주체에 대한 고유한 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-166">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="9ad7e-167">만든 후 이 속성을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-167">Once created this property cannot be changed.</span></span> <span data-ttu-id="9ad7e-168">기존 애플리케이션에 대한 애플리케이션 ID를 지정하지 않으면 애플리케이션이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-168">If an application ID for an existing application is not specified, an application is created.</span></span>

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

### <span data-ttu-id="9ad7e-169">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="9ad7e-169">-ApplicationObject</span></span>

<span data-ttu-id="9ad7e-170">서비스 주체가 생성되는 애플리케이션을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-170">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="9ad7e-171">-CertValue</span><span class="sxs-lookup"><span data-stu-id="9ad7e-171">-CertValue</span></span>

<span data-ttu-id="9ad7e-172">비대칭 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-172">The value of the asymmetric credential type.</span></span> <span data-ttu-id="9ad7e-173">Base64로 인코딩된 인증서를 나타났습니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-173">It represents the Base64 encoded certificate.</span></span>

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

### <span data-ttu-id="9ad7e-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ad7e-174">-DefaultProfile</span></span>

<span data-ttu-id="9ad7e-175">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ad7e-176">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9ad7e-176">-DisplayName</span></span>

<span data-ttu-id="9ad7e-177">서비스 주체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-177">The friendly name of the service principal.</span></span> <span data-ttu-id="9ad7e-178">표시 이름을 지정하지 않은 경우 이 값은 기본적으로 접미사는 애플리케이션을 만들 때인 **azure-powershell-MM-dd-yyyy-HH-mm-ss로** 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-178">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="9ad7e-179">-EndDate</span><span class="sxs-lookup"><span data-stu-id="9ad7e-179">-EndDate</span></span>

<span data-ttu-id="9ad7e-180">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-180">The effective end date of the credential usage.</span></span> <span data-ttu-id="9ad7e-181">기본 종료 날짜 값은 오늘부터 1년입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-181">The default end date value is one year from today.</span></span>
<span data-ttu-id="9ad7e-182">비대칭 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이전으로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-182">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="9ad7e-183">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="9ad7e-183">-KeyCredential</span></span>

<span data-ttu-id="9ad7e-184">애플리케이션과 연결된 키 자격 증명의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-184">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="9ad7e-185">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="9ad7e-185">-PasswordCredential</span></span>

<span data-ttu-id="9ad7e-186">애플리케이션과 연결된 암호 자격 증명의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-186">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="9ad7e-187">-Role</span><span class="sxs-lookup"><span data-stu-id="9ad7e-187">-Role</span></span>

<span data-ttu-id="9ad7e-188">서비스 주체가 범위를 통해 있는 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-188">The role that the service principal has over the scope.</span></span> <span data-ttu-id="9ad7e-189">값이 제공되지 않고 **역할은** 기본적으로 기여자 **역할로 설정됩니다.**</span><span class="sxs-lookup"><span data-stu-id="9ad7e-189">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

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

### <span data-ttu-id="9ad7e-190">-Scope</span><span class="sxs-lookup"><span data-stu-id="9ad7e-190">-Scope</span></span>

<span data-ttu-id="9ad7e-191">서비스 주체에 대한 권한이 있는 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-191">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="9ad7e-192">값이 제공되지 않고 **범위는** 기본적으로 현재 구독으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-192">If no value is provided, **Scope** defaults to the current subscription.</span></span>

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

### <span data-ttu-id="9ad7e-193">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="9ad7e-193">-SkipAssignment</span></span>

<span data-ttu-id="9ad7e-194">설정된 경우 서비스 주체에 대한 기본 역할 할당 만들기를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-194">If set, skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="9ad7e-195">-StartDate</span><span class="sxs-lookup"><span data-stu-id="9ad7e-195">-StartDate</span></span>

<span data-ttu-id="9ad7e-196">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-196">The effective start date of the credential usage.</span></span> <span data-ttu-id="9ad7e-197">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-197">The default start date value is today.</span></span> <span data-ttu-id="9ad7e-198">비대칭 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-198">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="9ad7e-199">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ad7e-199">-Confirm</span></span>

<span data-ttu-id="9ad7e-200">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ad7e-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ad7e-201">-WhatIf</span></span>

<span data-ttu-id="9ad7e-202">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9ad7e-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ad7e-203">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ad7e-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ad7e-204">CommonParameters</span></span>
<span data-ttu-id="9ad7e-205">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ad7e-206">자세한 내용은 [다음](/powershell/module/microsoft.powershell.core/about/about_commonparameters)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9ad7e-206">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="9ad7e-207">입력</span><span class="sxs-lookup"><span data-stu-id="9ad7e-207">INPUTS</span></span>

### <span data-ttu-id="9ad7e-208">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9ad7e-208">System.Guid</span></span>

### <span data-ttu-id="9ad7e-209">System.String</span><span class="sxs-lookup"><span data-stu-id="9ad7e-209">System.String</span></span>

### <span data-ttu-id="9ad7e-210">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="9ad7e-210">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="9ad7e-211">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="9ad7e-211">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="9ad7e-212">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="9ad7e-212">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="9ad7e-213">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="9ad7e-213">System.DateTime</span></span>

## <span data-ttu-id="9ad7e-214">출력</span><span class="sxs-lookup"><span data-stu-id="9ad7e-214">OUTPUTS</span></span>

### <span data-ttu-id="9ad7e-215">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9ad7e-215">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="9ad7e-216">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="9ad7e-216">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="9ad7e-217">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9ad7e-217">NOTES</span></span>

<span data-ttu-id="9ad7e-218">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="9ad7e-218">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="9ad7e-219">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ad7e-219">RELATED LINKS</span></span>

[<span data-ttu-id="9ad7e-220">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9ad7e-220">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="9ad7e-221">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9ad7e-221">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="9ad7e-222">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9ad7e-222">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="9ad7e-223">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9ad7e-223">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="9ad7e-224">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9ad7e-224">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="9ad7e-225">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9ad7e-225">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="9ad7e-226">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9ad7e-226">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)