---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 9d0fb4f188b3753e22258a27cf8632d85fe866dc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882521"
---
# <span data-ttu-id="199d0-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="199d0-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="199d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="199d0-102">SYNOPSIS</span></span>
<span data-ttu-id="199d0-103">새 azure active directory service principal을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="199d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="199d0-104">SYNTAX</span></span>

### <span data-ttu-id="199d0-105">SimpleParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="199d0-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="199d0-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="199d0-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="199d0-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="199d0-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="199d0-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="199d0-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="199d0-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="199d0-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="199d0-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="199d0-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="199d0-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="199d0-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="199d0-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="199d0-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="199d0-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="199d0-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="199d0-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="199d0-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="199d0-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="199d0-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="199d0-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="199d0-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="199d0-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="199d0-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="199d0-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="199d0-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="199d0-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="199d0-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="199d0-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="199d0-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="199d0-121">설명은</span><span class="sxs-lookup"><span data-stu-id="199d0-121">DESCRIPTION</span></span>
<span data-ttu-id="199d0-122">새 azure active directory service principal을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="199d0-123">사용자가 매개 변수에 대 한 기본값을 제공 하지 않는 경우 기본 매개 변수 집합에는 기본 값이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="199d0-124">사용 되는 기본값에 대 한 자세한 내용은 아래의 해당 매개 변수에 대 한 설명을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="199d0-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="199d0-125">이 cmdlet에는 and 매개 변수를 사용 하 여 서비스 사용자에 게 역할을 할당 하는 기능이 있습니다 `Role` `Scope` . 이러한 매개 변수 중 하나도 제공 하지 않으면 서비스 사용자에 게 역할이 할당 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="199d0-126">`Role`And `Scope` 매개 변수의 기본값은 각각 "참가자"이 고, 현재 구독은 사용자가 두 매개 _note_ 변수 중 하나에 대 한 값을 제공 하는 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="199d0-127">또한 cmdlet은 응용 프로그램을 암시적으로 만들고 해당 속성 (ApplicationId이 제공 되지 않은 경우)을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="199d0-128">응용 프로그램별 매개 변수를 업데이트 하려면 Set-AzureRmADApplication cmdlet을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="199d0-128">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="199d0-129">예제의</span><span class="sxs-lookup"><span data-stu-id="199d0-129">EXAMPLES</span></span>

### <span data-ttu-id="199d0-130">예제 1-간단한 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="199d0-130">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzureRmADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="199d0-131">위의 명령은 제공 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-131">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="199d0-132">응용 프로그램 id가 제공 되지 않았으므로 서비스 사용자를 위해 응용 프로그램이 생성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-132">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="199d0-133">Or에 대 한 값이 제공 되지 않았으므로 `Role` `Scope` 만든 서비스 주체에는 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-133">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="199d0-134">예제 2-지정 된 역할 및 기본 범위의 간단한 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="199d0-134">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="199d0-135">위의 명령은 제공 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-135">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="199d0-136">응용 프로그램 id가 제공 되지 않았으므로 서비스 사용자를 위해 응용 프로그램이 생성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-136">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="199d0-137">서비스 사용자가 현재 구독에 대해 "읽기" 권한으로 생성 되었습니다 (매개 변수에 대 한 값이 제공 되지 않았으므로 `Scope` ).</span><span class="sxs-lookup"><span data-stu-id="199d0-137">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="199d0-138">예제 3-지정 된 범위 및 기본 역할을 가진 간단한 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="199d0-138">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="199d0-139">위의 명령은 제공 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-139">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="199d0-140">응용 프로그램 id가 제공 되지 않았으므로 서비스 사용자를 위해 응용 프로그램이 생성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-140">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="199d0-141">제공 된 리소스 그룹 범위를 통해 서비스 사용자가 "참가자" 권한으로 생성 되었습니다 (매개 변수에 대 한 값이 제공 되지 않았으므로 `Role` ).</span><span class="sxs-lookup"><span data-stu-id="199d0-141">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="199d0-142">예제 4-단순 광고 서비스 주도자 만들기 지정 된 범위 및 역할</span><span class="sxs-lookup"><span data-stu-id="199d0-142">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="199d0-143">위의 명령은 제공 되지 않은 매개 변수에 대 한 기본값을 사용 하 여 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-143">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="199d0-144">응용 프로그램 id가 제공 되지 않았으므로 서비스 사용자를 위해 응용 프로그램이 생성 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-144">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="199d0-145">서비스 사용자가 제공 된 리소스 그룹 범위에 대해 "읽기" 권한을 사용 하 여 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-145">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="199d0-146">예제 5-역할을 할당 하 여 응용 프로그램 id를 사용 하 여 새 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="199d0-146">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="199d0-147">응용 프로그램 id가 ' 4a28ad2-3| 4-4a41-bc3b-d22ddf90000e ' 인 응용 프로그램에 대 한 새 광고 서비스 사용자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-147">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="199d0-148">Or에 대 한 값이 제공 되지 않았으므로 `Role` `Scope` 만든 서비스 주체에는 권한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-148">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="199d0-149">예제 6-파이핑을 사용 하 여 새 광고 서비스 사용자 만들기</span><span class="sxs-lookup"><span data-stu-id="199d0-149">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzureRmADServicePrincipal
```

<span data-ttu-id="199d0-150">개체 id가 ' 3ede3c26-b443-4e0b-9efc-b05e68338dc3 ' 인 응용 프로그램을 가져오고 해당 응용 프로그램에 대 한 새 광고 서비스 사용자를 만들기 위해 New-AzureRmADServicePrincipal cmdlet에 대 한 파이프를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-150">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzureRmADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="199d0-151">변수</span><span class="sxs-lookup"><span data-stu-id="199d0-151">PARAMETERS</span></span>

### <span data-ttu-id="199d0-152">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="199d0-152">-ApplicationId</span></span>
<span data-ttu-id="199d0-153">테 넌 트의 서비스 사용자에 대 한 고유한 응용 프로그램 id입니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-153">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="199d0-154">만든 후에는이 속성을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-154">Once created this property cannot be changed.</span></span>
<span data-ttu-id="199d0-155">응용 프로그램 id가 지정 되지 않은 경우 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-155">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="199d0-156">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="199d0-156">-ApplicationObject</span></span>
<span data-ttu-id="199d0-157">서비스 사용자를 만들 응용 프로그램을 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-157">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="199d0-158">-CertValue</span><span class="sxs-lookup"><span data-stu-id="199d0-158">-CertValue</span></span>
<span data-ttu-id="199d0-159">"비대칭" 자격 증명 형식의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-159">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="199d0-160">Base 64 인코딩된 인증서를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-160">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="199d0-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="199d0-161">-DefaultProfile</span></span>
<span data-ttu-id="199d0-162">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="199d0-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="199d0-163">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="199d0-163">-DisplayName</span></span>
<span data-ttu-id="199d0-164">서비스 사용자의 식별 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-164">The friendly name of the service principal.</span></span> <span data-ttu-id="199d0-165">표시 이름이 제공 되지 않은 경우이 값은 기본적으로 ' azure-powershell-MM-dd-yyyy-mm-dd-ss ' 이며, 여기서 접미사는 응용 프로그램을 만드는 데 걸리는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-165">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="199d0-166">-EndDate</span><span class="sxs-lookup"><span data-stu-id="199d0-166">-EndDate</span></span>
<span data-ttu-id="199d0-167">자격 증명 사용의 유효 종료 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-167">The effective end date of the credential usage.</span></span>
<span data-ttu-id="199d0-168">기본 끝 날짜 값은 오늘부터 1 년입니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-168">The default end date value is one year from today.</span></span> <span data-ttu-id="199d0-169">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 이전으로 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-169">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="199d0-170">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="199d0-170">-KeyCredential</span></span>
<span data-ttu-id="199d0-171">응용 프로그램과 연결 된 키 자격 증명의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-171">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="199d0-172">-암호</span><span class="sxs-lookup"><span data-stu-id="199d0-172">-Password</span></span>
<span data-ttu-id="199d0-173">서비스 사용자와 연결할 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-173">The password to be associated with the service principal.</span></span> <span data-ttu-id="199d0-174">암호를 제공 하지 않으면 임의의 GUID가 생성 되어 암호로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-174">If a password is not provided, a random GUID will be generated and used as the password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="199d0-175">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="199d0-175">-PasswordCredential</span></span>
<span data-ttu-id="199d0-176">응용 프로그램과 연결 된 암호 자격 증명 모음입니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-176">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="199d0-177">-역할</span><span class="sxs-lookup"><span data-stu-id="199d0-177">-Role</span></span>
<span data-ttu-id="199d0-178">서비스 사용자가 범위를 초과 하는 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-178">The role that the service principal has over the scope.</span></span> <span data-ttu-id="199d0-179">값이 `Scope` 제공 되지만 값이 제공 되지 않으면 `Role` 기본적으로 `Role` ' 참가자 ' 역할이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-179">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="199d0-180">-범위</span><span class="sxs-lookup"><span data-stu-id="199d0-180">-Scope</span></span>
<span data-ttu-id="199d0-181">서비스 사용자에 게 사용 권한이 있는 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-181">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="199d0-182">값이 `Role` 제공 되지만 값이 제공 되지 않으면 `Scope` `Scope` 현재 구독이 기본값으로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-182">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="199d0-183">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="199d0-183">-SkipAssignment</span></span>
<span data-ttu-id="199d0-184">설정 하는 경우 서비스 사용자에 대 한 기본 역할 할당 만들기를 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-184">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="199d0-185">-시작 날짜</span><span class="sxs-lookup"><span data-stu-id="199d0-185">-StartDate</span></span>
<span data-ttu-id="199d0-186">자격 증명 사용의 유효 시작 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-186">The effective start date of the credential usage.</span></span>
<span data-ttu-id="199d0-187">기본 시작 날짜 값은 오늘입니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-187">The default start date value is today.</span></span> <span data-ttu-id="199d0-188">"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후에이를 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-188">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="199d0-189">-확인</span><span class="sxs-lookup"><span data-stu-id="199d0-189">-Confirm</span></span>
<span data-ttu-id="199d0-190">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="199d0-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="199d0-191">-WhatIf</span></span>
<span data-ttu-id="199d0-192">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="199d0-193">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="199d0-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="199d0-194">CommonParameters</span></span>
<span data-ttu-id="199d0-195">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="199d0-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="199d0-196">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="199d0-196">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="199d0-197">입력</span><span class="sxs-lookup"><span data-stu-id="199d0-197">INPUTS</span></span>

### <span data-ttu-id="199d0-198">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="199d0-198">System.Guid</span></span>

### <span data-ttu-id="199d0-199">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="199d0-199">System.String</span></span>

### <span data-ttu-id="199d0-200">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adapplication</span><span class="sxs-lookup"><span data-stu-id="199d0-200">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="199d0-201">매개 변수: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="199d0-201">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="199d0-202">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adpasswordcredential []</span><span class="sxs-lookup"><span data-stu-id="199d0-202">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="199d0-203">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adkeycredential []</span><span class="sxs-lookup"><span data-stu-id="199d0-203">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="199d0-204">System.webserver</span><span class="sxs-lookup"><span data-stu-id="199d0-204">System.Security.SecureString</span></span>

### <span data-ttu-id="199d0-205">시스템. 날짜/시간</span><span class="sxs-lookup"><span data-stu-id="199d0-205">System.DateTime</span></span>

## <span data-ttu-id="199d0-206">출력</span><span class="sxs-lookup"><span data-stu-id="199d0-206">OUTPUTS</span></span>

### <span data-ttu-id="199d0-207">Microsoft.Azure.Graph.RBAC.Version1_6 ActiveDirectory Adserviceprincipal</span><span class="sxs-lookup"><span data-stu-id="199d0-207">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="199d0-208">PSADServicePrincipalWrapper에 대 한 권한 부여.</span><span class="sxs-lookup"><span data-stu-id="199d0-208">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="199d0-209">상속자</span><span class="sxs-lookup"><span data-stu-id="199d0-209">NOTES</span></span>
<span data-ttu-id="199d0-210">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="199d0-210">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="199d0-211">관련 링크</span><span class="sxs-lookup"><span data-stu-id="199d0-211">RELATED LINKS</span></span>

[<span data-ttu-id="199d0-212">제거-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="199d0-212">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="199d0-213">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="199d0-213">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="199d0-214">새로운 AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="199d0-214">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="199d0-215">제거-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="199d0-215">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="199d0-216">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="199d0-216">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="199d0-217">새로운 AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="199d0-217">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="199d0-218">제거-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="199d0-218">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

