---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 6d268c2378c93bcfb98e64c654880e8055bcede8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358058"
---
# <span data-ttu-id="a65f7-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a65f7-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="a65f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a65f7-102">SYNOPSIS</span></span>
<span data-ttu-id="a65f7-103">새 Azure Active Directory 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="a65f7-104">구문</span><span class="sxs-lookup"><span data-stu-id="a65f7-104">SYNTAX</span></span>

### <span data-ttu-id="a65f7-105">SimpleParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a65f7-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a65f7-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a65f7-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a65f7-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a65f7-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a65f7-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a65f7-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a65f7-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a65f7-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a65f7-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a65f7-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a65f7-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a65f7-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a65f7-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a65f7-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a65f7-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a65f7-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a65f7-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a65f7-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a65f7-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a65f7-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a65f7-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a65f7-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a65f7-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a65f7-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a65f7-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="a65f7-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a65f7-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="a65f7-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a65f7-120">설명</span><span class="sxs-lookup"><span data-stu-id="a65f7-120">DESCRIPTION</span></span>

<span data-ttu-id="a65f7-121">새 Azure Active Directory 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="a65f7-122">기본 매개 변수 집합은 매개 변수가 제공되지 않은 경우 기본값을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="a65f7-123">기본값에 대한 자세한 내용은 각 매개 변수에 대한 설명을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a65f7-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="a65f7-124">이 cmdlet에는 역할 및 범위 매개 변수를 사용하여 서비스 주체에 역할을 **할당할** **수** 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="a65f7-125">둘 다 생략하면 기여자 역할이 서비스 주체에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="a65f7-126">역할 및 범위  매개  변수의 기본값은 현재 **구독에 대한** 참가자입니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="a65f7-127">이 cmdlet은 애플리케이션을 만들고 ApplicationId가 제공되지 않은 경우 해당 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="a65f7-128">애플리케이션별 매개 변수를 업데이트하기 위해 [Update-AzADApplication](./update-azadapplication.md) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="a65f7-129">**New-AzADServicePrincipal** 명령을 사용하여 서비스 주체를 만들 때 출력에는 보호해야 하는 자격 증명이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="a65f7-130">코드에 이러한 자격 증명을 포함하지 않는지 또는 소스 제어에 자격 증명을 검사해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="a65f7-131">또는 관리 ID를 [](/azure/active-directory/managed-identities-azure-resources/overview) 사용하여 자격 증명을 사용할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="a65f7-132">기본적으로 **New-AzADServicePrincipal은** 구독 [](/azure/role-based-access-control/built-in-roles#contributor) 범위의 서비스 주체에 기여자 역할을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="a65f7-133">손상된 서비스 주체의 위험을 줄이기 위해 보다 구체적인 역할을 할당하고 리소스 또는 리소스 그룹으로 범위를 좁힐 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="a65f7-134">자세한 [내용은 역할 할당을 추가하는](/azure/role-based-access-control/role-assignments-steps) 단계를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a65f7-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="a65f7-135">예제</span><span class="sxs-lookup"><span data-stu-id="a65f7-135">EXAMPLES</span></span>

### <span data-ttu-id="a65f7-136">예제 1: 간단한 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="a65f7-136">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="a65f7-137">다음 예제에서는 지정되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-137">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="a65f7-138">애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-138">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="a65f7-139">역할 또는 범위에 대한 값이 제공되지 않습니다.  생성된 서비스 주체에는 현재 구독에 대한 참가자 역할이 할당됩니다. </span><span class="sxs-lookup"><span data-stu-id="a65f7-139">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="a65f7-140">예제 2: 지정된 역할 및 기본 범위를 통해 간단한 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="a65f7-140">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="a65f7-141">다음 예제에서는 지정되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-141">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="a65f7-142">애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-142">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="a65f7-143">범위 매개 변수에  대한 값이 제공되지 않고 현재 구독에 대한 읽기 권한자 권한으로 서비스 **주체가** 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-143">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

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

### <span data-ttu-id="a65f7-144">예제 3: 지정된 범위 및 기본 역할로 간단한 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="a65f7-144">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="a65f7-145">다음 예제에서는 지정되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-145">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="a65f7-146">애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-146">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="a65f7-147">서비스 주체는  제공된 리소스 그룹 범위에 대한 기여자 권한으로 생성됩니다. 역할 매개 변수에 대한 값이 **제공되지** 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-147">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

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

### <span data-ttu-id="a65f7-148">예제 4: 지정된 범위 및 역할을 통해 간단한 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="a65f7-148">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="a65f7-149">다음 예제에서는 지정되지 않은 매개 변수에 대한 기본값을 사용하여 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-149">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="a65f7-150">애플리케이션 ID가 제공되지 않은 경우 서비스 주체에 대한 애플리케이션이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-150">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="a65f7-151">서비스 주체는 제공된 리소스 그룹 **범위에 대한 읽기** 권한자 권한으로 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-151">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

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

### <span data-ttu-id="a65f7-152">예제 5: 역할 할당과 함께 애플리케이션 ID를 사용하여 새 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="a65f7-152">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="a65f7-153">다음 예제에서는 애플리케이션 ID가 '000000000-0000-0000-0000-0000-00000000000'인 애플리케이션에 대한 새 AD 서비스 주체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-153">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="a65f7-154">역할 또는 범위에 대한 값이 제공되지 않습니다.  생성된 서비스 주체에는 현재 구독에 대한 참가자 역할이 할당됩니다. </span><span class="sxs-lookup"><span data-stu-id="a65f7-154">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="a65f7-155">예제 6: 파이핑을 사용하여 새 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="a65f7-155">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="a65f7-156">다음 예제에서는 [Get-AzADApplication](./get-azadapplication.md) cmdlet을 사용하여 개체 ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3'을 사용하여 애플리케이션을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-156">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="a65f7-157">결과는 cmdlet에 파이프하여 애플리케이션에 대한 새 AD 서비스 `New-AzADServicePrincipal` 주체를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-157">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="a65f7-158">예제 7: DisplayName 및 암호 자격 증명을 사용하여 새 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="a65f7-158">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="a65f7-159">다음 예제에서는 **ServicePrincipalName** 이름과 **StrongPassworld!23의** 암호를 사용하여 새 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-159">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="a65f7-160">생성된 애플리케이션을 기반으로 서비스 주체가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-160">It creates the service principal based on the created application.</span></span> <span data-ttu-id="a65f7-161">시작 날짜 및 종료 날짜가 암호 자격 증명에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-161">The start date and end date are added to the password credential.</span></span>

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

### <span data-ttu-id="a65f7-162">예제 8: DisplayName 및 일반 키 자격 증명을 사용하여 새 AD 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="a65f7-162">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="a65f7-163">다음 예제에서는 **ServicePrincipalName** 이름과 인증서 이름을 지정하여 새 애플리케이션을 **$cert.** 만든 애플리케이션을 기반으로 서비스 주체가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-163">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="a65f7-164">종료 날짜가 키 자격 증명에 추가됩니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-164">The end date is added to key credential.</span></span>

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

## <span data-ttu-id="a65f7-165">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a65f7-165">PARAMETERS</span></span>

### <span data-ttu-id="a65f7-166">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a65f7-166">-ApplicationId</span></span>

<span data-ttu-id="a65f7-167">테넌트의 서비스 주체에 대한 고유한 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-167">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="a65f7-168">만든 후 이 속성을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-168">Once created this property cannot be changed.</span></span> <span data-ttu-id="a65f7-169">기존 애플리케이션에 대한 애플리케이션 ID를 지정하지 않으면 애플리케이션이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-169">If an application ID for an existing application is not specified, an application is created.</span></span>

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

### <span data-ttu-id="a65f7-170">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="a65f7-170">-ApplicationObject</span></span>

<span data-ttu-id="a65f7-171">서비스 주체가 생성되는 애플리케이션을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-171">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="a65f7-172">-CertValue</span><span class="sxs-lookup"><span data-stu-id="a65f7-172">-CertValue</span></span>

<span data-ttu-id="a65f7-173">비대칭 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-173">The value of the asymmetric credential type.</span></span> <span data-ttu-id="a65f7-174">Base64로 인코딩된 인증서를 나타났습니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-174">It represents the Base64 encoded certificate.</span></span>

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

### <span data-ttu-id="a65f7-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a65f7-175">-DefaultProfile</span></span>

<span data-ttu-id="a65f7-176">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-176">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a65f7-177">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a65f7-177">-DisplayName</span></span>

<span data-ttu-id="a65f7-178">서비스 주체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-178">The friendly name of the service principal.</span></span> <span data-ttu-id="a65f7-179">표시 이름을 지정하지 않은 경우 이 값은 기본적으로 접미사는 애플리케이션을 만들 때인 **azure-powershell-MM-dd-yy-HH-mm-ss로** 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-179">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="a65f7-180">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a65f7-180">-EndDate</span></span>

<span data-ttu-id="a65f7-181">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-181">The effective end date of the credential usage.</span></span> <span data-ttu-id="a65f7-182">기본 종료 날짜 값은 오늘부터 1년입니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-182">The default end date value is one year from today.</span></span>
<span data-ttu-id="a65f7-183">비대칭 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이전으로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-183">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="a65f7-184">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="a65f7-184">-KeyCredential</span></span>

<span data-ttu-id="a65f7-185">애플리케이션과 연결된 키 자격 증명의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-185">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="a65f7-186">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="a65f7-186">-PasswordCredential</span></span>

<span data-ttu-id="a65f7-187">애플리케이션과 연결된 암호 자격 증명의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-187">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="a65f7-188">-Role</span><span class="sxs-lookup"><span data-stu-id="a65f7-188">-Role</span></span>

<span data-ttu-id="a65f7-189">서비스 주체가 범위를 통해 있는 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-189">The role that the service principal has over the scope.</span></span> <span data-ttu-id="a65f7-190">값이 제공되지 않고 **역할은** 기본적으로 기여자 **역할로 설정됩니다.**</span><span class="sxs-lookup"><span data-stu-id="a65f7-190">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

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

### <span data-ttu-id="a65f7-191">-Scope</span><span class="sxs-lookup"><span data-stu-id="a65f7-191">-Scope</span></span>

<span data-ttu-id="a65f7-192">서비스 주체에 대한 권한이 있는 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-192">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="a65f7-193">값이 제공되지 않고 **범위는** 기본적으로 현재 구독으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-193">If no value is provided, **Scope** defaults to the current subscription.</span></span>

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

### <span data-ttu-id="a65f7-194">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="a65f7-194">-SkipAssignment</span></span>

<span data-ttu-id="a65f7-195">설정된 경우 서비스 주체에 대한 기본 역할 할당 만들기를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="a65f7-195">If set, skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="a65f7-196">-StartDate</span><span class="sxs-lookup"><span data-stu-id="a65f7-196">-StartDate</span></span>

<span data-ttu-id="a65f7-197">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-197">The effective start date of the credential usage.</span></span> <span data-ttu-id="a65f7-198">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-198">The default start date value is today.</span></span> <span data-ttu-id="a65f7-199">비대칭 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후로 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-199">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="a65f7-200">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a65f7-200">-Confirm</span></span>

<span data-ttu-id="a65f7-201">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a65f7-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a65f7-202">-WhatIf</span></span>

<span data-ttu-id="a65f7-203">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a65f7-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a65f7-204">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a65f7-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a65f7-205">CommonParameters</span></span>
<span data-ttu-id="a65f7-206">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a65f7-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a65f7-207">자세한 내용은 [다음](/powershell/module/microsoft.powershell.core/about/about_commonparameters)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a65f7-207">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="a65f7-208">입력</span><span class="sxs-lookup"><span data-stu-id="a65f7-208">INPUTS</span></span>

### <span data-ttu-id="a65f7-209">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a65f7-209">System.Guid</span></span>

### <span data-ttu-id="a65f7-210">System.String</span><span class="sxs-lookup"><span data-stu-id="a65f7-210">System.String</span></span>

### <span data-ttu-id="a65f7-211">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="a65f7-211">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="a65f7-212">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="a65f7-212">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="a65f7-213">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="a65f7-213">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="a65f7-214">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="a65f7-214">System.DateTime</span></span>

## <span data-ttu-id="a65f7-215">출력</span><span class="sxs-lookup"><span data-stu-id="a65f7-215">OUTPUTS</span></span>

### <span data-ttu-id="a65f7-216">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a65f7-216">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="a65f7-217">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="a65f7-217">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="a65f7-218">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a65f7-218">NOTES</span></span>

<span data-ttu-id="a65f7-219">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="a65f7-219">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a65f7-220">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a65f7-220">RELATED LINKS</span></span>

[<span data-ttu-id="a65f7-221">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a65f7-221">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="a65f7-222">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a65f7-222">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="a65f7-223">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a65f7-223">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="a65f7-224">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a65f7-224">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="a65f7-225">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a65f7-225">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="a65f7-226">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a65f7-226">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="a65f7-227">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a65f7-227">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)