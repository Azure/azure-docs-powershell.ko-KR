---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: bf01232939881feb5a60420cde76e0e809cbcb3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176372"
---
# <span data-ttu-id="97a5b-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="97a5b-101">Set-AzResource</span></span>

## <span data-ttu-id="97a5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="97a5b-103">리소스를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-103">Modifies a resource.</span></span>

## <span data-ttu-id="97a5b-104">구문</span><span class="sxs-lookup"><span data-stu-id="97a5b-104">SYNTAX</span></span>

### <span data-ttu-id="97a5b-105">ByResourceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="97a5b-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97a5b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="97a5b-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97a5b-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="97a5b-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a5b-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="97a5b-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97a5b-109">설명</span><span class="sxs-lookup"><span data-stu-id="97a5b-109">DESCRIPTION</span></span>
<span data-ttu-id="97a5b-110">**Set-AzResource** cmdlet은 기존 Azure 리소스를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="97a5b-111">이름 및 형식 또는 ID별로 수정할 리소스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="97a5b-112">예제</span><span class="sxs-lookup"><span data-stu-id="97a5b-112">EXAMPLES</span></span>

### <span data-ttu-id="97a5b-113">예제 1: 리소스 수정</span><span class="sxs-lookup"><span data-stu-id="97a5b-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="97a5b-114">첫 번째 명령은 Get-AzResource cmdlet을 사용하여 ContosoSite라는 리소스를 $Resource 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="97a5b-115">두 번째 명령은 $Resource.</span><span class="sxs-lookup"><span data-stu-id="97a5b-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="97a5b-116">마지막 명령은 리소스가 리소스와 일치하게 $Resource.</span><span class="sxs-lookup"><span data-stu-id="97a5b-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="97a5b-117">예제 2: 주어진 리소스 그룹의 모든 리소스 수정</span><span class="sxs-lookup"><span data-stu-id="97a5b-117">Example 2: Modify all resources in a given resource group</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceGroupName testrg
PS C:\> $Resource | ForEach-Object { $_.Tags.Add("testkey", "testval") }
PS C:\> $Resource | Set-AzResource -Force

Name              : kv-test
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.KeyVault/vaults/kv-test
ResourceName      : kv-test
ResourceType      : Microsoft.KeyVault/vaults
ResourceGroupName : testrg
Location          : westus
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, key}
Properties        : @{}

Name              : testresource
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Providers.Test/statefulResources/testresource
ResourceName      : testresource
ResourceType      : Providers.Test/statefulResources
ResourceGroupName : testrg
Location          : West US 2
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, anothertesttag}
Properties        : @{key=value}
Sku               : @{name=A0}
```

<span data-ttu-id="97a5b-118">첫 번째 명령은 testrg 리소스 그룹의 리소스를 1차원 변수에 $Resource 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="97a5b-119">두 번째 명령은 리소스 그룹의 이러한 각 리소스에 대해 이들을 통해 이들을 위해 새 태그를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="97a5b-120">마지막 명령은 이러한 각 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="97a5b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97a5b-121">PARAMETERS</span></span>

### <span data-ttu-id="97a5b-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="97a5b-122">-ApiVersion</span></span>
<span data-ttu-id="97a5b-123">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="97a5b-124">버전을 지정하지 않으면 이 cmdlet은 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97a5b-125">-AsJob</span></span>
<span data-ttu-id="97a5b-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="97a5b-126">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a5b-127">-DefaultProfile</span></span>
<span data-ttu-id="97a5b-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="97a5b-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97a5b-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="97a5b-129">-ExtensionResourceName</span></span>
<span data-ttu-id="97a5b-130">리소스에 대한 확장 리소스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="97a5b-131">예를 들어 데이터베이스를 지정하려면 다음 형식을 사용합니다. 서버 이름 `/` 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="97a5b-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="97a5b-132">-ExtensionResourceType</span></span>
<span data-ttu-id="97a5b-133">확장 리소스에 대한 리소스 종류를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="97a5b-134">예를 들어 확장 리소스가 데이터베이스인 경우 다음을 지정합니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="97a5b-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-135">-Force</span><span class="sxs-lookup"><span data-stu-id="97a5b-135">-Force</span></span>
<span data-ttu-id="97a5b-136">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-136">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97a5b-137">-InputObject</span></span>
<span data-ttu-id="97a5b-138">업데이트할 리소스의 개체 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-138">The object representation of the resource to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-139">-Kind</span><span class="sxs-lookup"><span data-stu-id="97a5b-139">-Kind</span></span>
<span data-ttu-id="97a5b-140">리소스에 대한 리소스 종류를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-140">Specifies the resource kind for the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="97a5b-141">-ODataQuery</span></span>
<span data-ttu-id="97a5b-142">OData(Open Data Protocol) 스타일 필터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="97a5b-143">이 cmdlet은 다른 필터 외에도 요청에 이 값을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="97a5b-144">-Plan</span></span>
<span data-ttu-id="97a5b-145">리소스에 대한 리소스 계획 속성을 해시 테이블로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="97a5b-146">-Pre</span></span>
<span data-ttu-id="97a5b-147">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-148">-Properties</span><span class="sxs-lookup"><span data-stu-id="97a5b-148">-Properties</span></span>
<span data-ttu-id="97a5b-149">리소스에 대한 리소스 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-149">Specifies resource properties for the resource.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97a5b-150">-ResourceGroupName</span></span>
<span data-ttu-id="97a5b-151">이 cmdlet이 리소스를 수정하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97a5b-152">-ResourceId</span></span>
<span data-ttu-id="97a5b-153">다음 예제와 같이 구독을 포함하여 정식 리소스 `/subscriptions/` ID를 지정합니다.`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="97a5b-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="97a5b-154">-ResourceName</span></span>
<span data-ttu-id="97a5b-155">리소스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="97a5b-156">예를 들어 데이터베이스를 지정하려면 다음 형식을 사용합니다. `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="97a5b-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="97a5b-157">-ResourceType</span></span>
<span data-ttu-id="97a5b-158">리소스의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="97a5b-159">예를 들어 데이터베이스의 경우 리소스 종류는 다음과 같습니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="97a5b-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-160">-Sku</span><span class="sxs-lookup"><span data-stu-id="97a5b-160">-Sku</span></span>
<span data-ttu-id="97a5b-161">리소스의 SKU 개체를 해시 테이블로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-161">Specifies the SKU object of the resource as a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="97a5b-162">-Tag</span></span>
<span data-ttu-id="97a5b-163">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="97a5b-164">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="97a5b-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="97a5b-165">-TenantLevel</span></span>
<span data-ttu-id="97a5b-166">이 cmdlet이 테넌트 수준에서 작동하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-166">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="97a5b-167">-UsePatchSemantics</span></span>
<span data-ttu-id="97a5b-168">이 cmdlet은 HTTP PATCH를 사용하여 HTTP PUT 대신 개체를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97a5b-169">-Confirm</span></span>
<span data-ttu-id="97a5b-170">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97a5b-171">-WhatIf</span></span>
<span data-ttu-id="97a5b-172">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="97a5b-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97a5b-173">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-173">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a5b-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a5b-174">CommonParameters</span></span>
<span data-ttu-id="97a5b-175">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="97a5b-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a5b-176">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="97a5b-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a5b-177">입력</span><span class="sxs-lookup"><span data-stu-id="97a5b-177">INPUTS</span></span>

### <span data-ttu-id="97a5b-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span><span class="sxs-lookup"><span data-stu-id="97a5b-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="97a5b-179">System.String</span><span class="sxs-lookup"><span data-stu-id="97a5b-179">System.String</span></span>

### <span data-ttu-id="97a5b-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="97a5b-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="97a5b-181">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="97a5b-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="97a5b-182">출력</span><span class="sxs-lookup"><span data-stu-id="97a5b-182">OUTPUTS</span></span>

### <span data-ttu-id="97a5b-183">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="97a5b-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="97a5b-184">참고 사항</span><span class="sxs-lookup"><span data-stu-id="97a5b-184">NOTES</span></span>

## <span data-ttu-id="97a5b-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97a5b-185">RELATED LINKS</span></span>

[<span data-ttu-id="97a5b-186">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="97a5b-186">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="97a5b-187">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="97a5b-187">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="97a5b-188">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="97a5b-188">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="97a5b-189">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="97a5b-189">Remove-AzResource</span></span>](./Remove-AzResource.md)
