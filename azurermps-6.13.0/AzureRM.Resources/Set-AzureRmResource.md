---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: e5346924b6d93148781d71c3a5493b7398c02e20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535631"
---
# <span data-ttu-id="ef0ae-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef0ae-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="ef0ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef0ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ef0ae-103">리소스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef0ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ef0ae-104">SYNTAX</span></span>

### <span data-ttu-id="ef0ae-105">ByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="ef0ae-105">ByResourceId (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef0ae-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ef0ae-106">ByInputObject</span></span>
```
Set-AzureRmResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef0ae-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="ef0ae-107">BySubscriptionLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef0ae-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="ef0ae-108">ByTenantLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef0ae-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ef0ae-109">DESCRIPTION</span></span>
<span data-ttu-id="ef0ae-110">**Set-AzureRmResource** cmdlet은 기존 Azure 리소스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-110">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="ef0ae-111">이름 및 형식 또는 ID를 기준으로 수정할 리소스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="ef0ae-112">예제의</span><span class="sxs-lookup"><span data-stu-id="ef0ae-112">EXAMPLES</span></span>

### <span data-ttu-id="ef0ae-113">예제 1: 리소스 수정</span><span class="sxs-lookup"><span data-stu-id="ef0ae-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzureRmResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="ef0ae-114">첫 번째 명령은 Get-AzureRmResource cmdlet을 사용 하 여 ContosoSite 이라는 리소스를 가져온 다음 $Resource 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-114">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="ef0ae-115">두 번째 명령은 $Resource의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="ef0ae-116">마지막 명령은 $Resource 일치 하도록 리소스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="ef0ae-117">예제 2: 지정 된 리소스 그룹의 모든 리소스 수정</span><span class="sxs-lookup"><span data-stu-id="ef0ae-117">Example 2: Modify all resources in a given resource group</span></span>
```
PS C:\> $Resource = Get-AzureRmResource -ResourceGroupName testrg
PS C:\> $Resource | ForEach-Object { $_.Tags.Add("testkey", "testval") }
PS C:\> $Resource | Set-AzureRmResource -Force

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

<span data-ttu-id="ef0ae-118">첫 번째 명령은 testrg 리소스 그룹의 리소스를 가져온 다음이를 $Resource 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="ef0ae-119">두 번째 명령은 리소스 그룹의 각 리소스에 대해 반복 하 고 새 태그를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="ef0ae-120">마지막 명령은 이러한 각 리소스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="ef0ae-121">변수</span><span class="sxs-lookup"><span data-stu-id="ef0ae-121">PARAMETERS</span></span>

### <span data-ttu-id="ef0ae-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ef0ae-122">-ApiVersion</span></span>
<span data-ttu-id="ef0ae-123">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ef0ae-124">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ef0ae-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef0ae-125">-AsJob</span></span>
<span data-ttu-id="ef0ae-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ef0ae-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef0ae-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef0ae-127">-DefaultProfile</span></span>
<span data-ttu-id="ef0ae-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ef0ae-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef0ae-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="ef0ae-129">-ExtensionResourceName</span></span>
<span data-ttu-id="ef0ae-130">리소스에 대 한 확장 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="ef0ae-131">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. 서버 이름 `/` 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="ef0ae-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="ef0ae-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="ef0ae-132">-ExtensionResourceType</span></span>
<span data-ttu-id="ef0ae-133">확장 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="ef0ae-134">예를 들어 확장 리소스가 데이터베이스인 경우 다음을 지정 합니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="ef0ae-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="ef0ae-135">-Force</span><span class="sxs-lookup"><span data-stu-id="ef0ae-135">-Force</span></span>
<span data-ttu-id="ef0ae-136">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ef0ae-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef0ae-137">-InputObject</span></span>
<span data-ttu-id="ef0ae-138">업데이트할 리소스의 개체 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-138">The object representation of the resource to update.</span></span>

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

### <span data-ttu-id="ef0ae-139">-종류</span><span class="sxs-lookup"><span data-stu-id="ef0ae-139">-Kind</span></span>
<span data-ttu-id="ef0ae-140">자원의 자원 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-140">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="ef0ae-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ef0ae-141">-ODataQuery</span></span>
<span data-ttu-id="ef0ae-142">OData (Open Data Protocol) 스타일 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="ef0ae-143">이 cmdlet은이 값을 다른 모든 필터 외에도 요청에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="ef0ae-144">-계획</span><span class="sxs-lookup"><span data-stu-id="ef0ae-144">-Plan</span></span>
<span data-ttu-id="ef0ae-145">리소스에 대 한 리소스 계획 속성을 해시 테이블로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="ef0ae-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="ef0ae-146">-Pre</span></span>
<span data-ttu-id="ef0ae-147">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ef0ae-148">-속성</span><span class="sxs-lookup"><span data-stu-id="ef0ae-148">-Properties</span></span>
<span data-ttu-id="ef0ae-149">리소스에 대 한 리소스 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-149">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="ef0ae-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef0ae-150">-ResourceGroupName</span></span>
<span data-ttu-id="ef0ae-151">이 cmdlet이 리소스를 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="ef0ae-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef0ae-152">-ResourceId</span></span>
<span data-ttu-id="ef0ae-153">구독을 포함 하 여 정규화 된 리소스 ID를 다음 예제와 같이 지정 합니다. `/subscriptions/` 구독 ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="ef0ae-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="ef0ae-154">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="ef0ae-154">-ResourceName</span></span>
<span data-ttu-id="ef0ae-155">리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="ef0ae-156">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="ef0ae-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="ef0ae-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ef0ae-157">-ResourceType</span></span>
<span data-ttu-id="ef0ae-158">리소스의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="ef0ae-159">예를 들어 데이터베이스의 경우 리소스 종류는 다음과 같습니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="ef0ae-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="ef0ae-160">-Sku</span><span class="sxs-lookup"><span data-stu-id="ef0ae-160">-Sku</span></span>
<span data-ttu-id="ef0ae-161">리소스의 SKU 개체를 해시 테이블로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-161">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="ef0ae-162">태그</span><span class="sxs-lookup"><span data-stu-id="ef0ae-162">-Tag</span></span>
<span data-ttu-id="ef0ae-163">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ef0ae-164">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ef0ae-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ef0ae-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="ef0ae-165">-TenantLevel</span></span>
<span data-ttu-id="ef0ae-166">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-166">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="ef0ae-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="ef0ae-167">-UsePatchSemantics</span></span>
<span data-ttu-id="ef0ae-168">HTTP를 사용 하지 않고이 cmdlet이 HTTP 패치를 사용 하 여 개체를 업데이트 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="ef0ae-169">-확인</span><span class="sxs-lookup"><span data-stu-id="ef0ae-169">-Confirm</span></span>
<span data-ttu-id="ef0ae-170">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef0ae-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef0ae-171">-WhatIf</span></span>
<span data-ttu-id="ef0ae-172">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef0ae-173">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef0ae-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef0ae-174">CommonParameters</span></span>
<span data-ttu-id="ef0ae-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef0ae-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef0ae-176">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef0ae-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef0ae-177">입력</span><span class="sxs-lookup"><span data-stu-id="ef0ae-177">INPUTS</span></span>

### <span data-ttu-id="ef0ae-178">않아야</span><span class="sxs-lookup"><span data-stu-id="ef0ae-178">None</span></span>

## <span data-ttu-id="ef0ae-179">출력</span><span class="sxs-lookup"><span data-stu-id="ef0ae-179">OUTPUTS</span></span>

### <span data-ttu-id="ef0ae-180">Microsoft. Azure. a \* PSResource</span><span class="sxs-lookup"><span data-stu-id="ef0ae-180">Microsoft.Azure.Commands.ResourceManager.Models.PSResource</span></span>

## <span data-ttu-id="ef0ae-181">상속자</span><span class="sxs-lookup"><span data-stu-id="ef0ae-181">NOTES</span></span>

## <span data-ttu-id="ef0ae-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef0ae-182">RELATED LINKS</span></span>

[<span data-ttu-id="ef0ae-183">찾기-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef0ae-183">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="ef0ae-184">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef0ae-184">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="ef0ae-185">이동-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef0ae-185">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="ef0ae-186">새로운 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef0ae-186">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="ef0ae-187">제거-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ef0ae-187">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
