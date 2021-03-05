---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 457f5db18ba43d1fd598e255d9ca1fb2e62f3f3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986659"
---
# <span data-ttu-id="4590d-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="4590d-101">New-AzResource</span></span>

## <span data-ttu-id="4590d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4590d-102">SYNOPSIS</span></span>
<span data-ttu-id="4590d-103">리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-103">Creates a resource.</span></span>

## <span data-ttu-id="4590d-104">구문</span><span class="sxs-lookup"><span data-stu-id="4590d-104">SYNTAX</span></span>

### <span data-ttu-id="4590d-105">ByResourceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="4590d-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4590d-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="4590d-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4590d-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="4590d-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4590d-108">설명</span><span class="sxs-lookup"><span data-stu-id="4590d-108">DESCRIPTION</span></span>
<span data-ttu-id="4590d-109">**New-AzResource** cmdlet은 리소스 그룹에 웹 사이트, Azure SQL 데이터베이스 서버 또는 Azure SQL 데이터베이스와 같은 Azure 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="4590d-110">예제</span><span class="sxs-lookup"><span data-stu-id="4590d-110">EXAMPLES</span></span>

### <span data-ttu-id="4590d-111">예제 1: 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="4590d-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="4590d-112">이 명령은 ResourceGroup11의 웹 사이트인 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="4590d-113">예제 2: splatting을 사용하여 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="4590d-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US"
    Properties        = @{test = "test"}
    ResourceName      = "TestSite06"
    ResourceType      = "microsoft.web/sites"
    ResourceGroupName = "ResourceGroup11"
    Force             = $true
}

PS> New-AzResource @prop
```

<span data-ttu-id="4590d-114">이 명령은 ResourceGroup11의 웹 사이트인 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="4590d-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4590d-115">PARAMETERS</span></span>

### <span data-ttu-id="4590d-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4590d-116">-ApiVersion</span></span>
<span data-ttu-id="4590d-117">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="4590d-118">버전을 지정하지 않으면 이 cmdlet에서는 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4590d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4590d-119">-AsJob</span></span>
<span data-ttu-id="4590d-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4590d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4590d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4590d-121">-DefaultProfile</span></span>
<span data-ttu-id="4590d-122">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4590d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4590d-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="4590d-123">-ExtensionResourceName</span></span>
<span data-ttu-id="4590d-124">리소스에 대한 확장 리소스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="4590d-125">예를 들어 데이터베이스를 지정하려면 서버 이름 데이터베이스 이름 형식을 `/` 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="4590d-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="4590d-126">-ExtensionResourceType</span></span>
<span data-ttu-id="4590d-127">확장 리소스에 대한 리소스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="4590d-128">예를 들어 확장 리소스가 데이터베이스인 경우 다음 형식을 지정합니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="4590d-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="4590d-129">-Force</span><span class="sxs-lookup"><span data-stu-id="4590d-129">-Force</span></span>
<span data-ttu-id="4590d-130">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4590d-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="4590d-131">-IsFullObject</span></span>
<span data-ttu-id="4590d-132">속성 매개 변수가  지정하는 개체가 전체 개체인 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="4590d-133">-Kind</span><span class="sxs-lookup"><span data-stu-id="4590d-133">-Kind</span></span>
<span data-ttu-id="4590d-134">리소스에 대한 리소스 종류를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="4590d-135">-Location</span><span class="sxs-lookup"><span data-stu-id="4590d-135">-Location</span></span>
<span data-ttu-id="4590d-136">리소스의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="4590d-137">미국 중부 또는 동남 아시아와 같은 데이터 센터 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="4590d-138">해당 유형의 리소스를 지원하는 모든 위치에 리소스를 위치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="4590d-139">리소스 그룹에는 다른 위치의 리소스가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="4590d-140">각 리소스 유형을 지원하는 위치를 확인하기 위해 Get-AzLocation cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="4590d-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="4590d-141">-ODataQuery</span></span>
<span data-ttu-id="4590d-142">OData(Open Data Protocol) 스타일 필터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="4590d-143">이 cmdlet은 다른 필터 외에도 요청에 이 값을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="4590d-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="4590d-144">-Plan</span></span>
<span data-ttu-id="4590d-145">리소스 계획 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-145">A hash table that represents resource plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4590d-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="4590d-146">-Pre</span></span>
<span data-ttu-id="4590d-147">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4590d-148">-속성</span><span class="sxs-lookup"><span data-stu-id="4590d-148">-Properties</span></span>
<span data-ttu-id="4590d-149">리소스에 대한 리소스 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="4590d-150">이 매개 변수를 사용하여 리소스 유형에 특정 속성의 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4590d-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4590d-151">-ResourceGroupName</span></span>
<span data-ttu-id="4590d-152">이 cmdlet에서 리소스를 만드는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="4590d-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4590d-153">-ResourceId</span></span>
<span data-ttu-id="4590d-154">다음 예제와 같이 구독을 포함하여 완전히 자격을 갖춘 리소스 `/subscriptions/` ID를 지정합니다.`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="4590d-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="4590d-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4590d-155">-ResourceName</span></span>
<span data-ttu-id="4590d-156">리소스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-156">Specifies the name of the resource.</span></span> <span data-ttu-id="4590d-157">예를 들어 데이터베이스를 지정하려면 다음 형식을 사용합니다. `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="4590d-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="4590d-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4590d-158">-ResourceType</span></span>
<span data-ttu-id="4590d-159">리소스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="4590d-160">예를 들어 데이터베이스의 경우 리소스 유형은 다음과 같습니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="4590d-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="4590d-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="4590d-161">-Sku</span></span>
<span data-ttu-id="4590d-162">sku 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="4590d-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="4590d-163">-Tag</span></span>
<span data-ttu-id="4590d-164">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4590d-165">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="4590d-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4590d-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="4590d-166">-TenantLevel</span></span>
<span data-ttu-id="4590d-167">이 cmdlet이 테넌트 수준에서 작동하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="4590d-168">-확인</span><span class="sxs-lookup"><span data-stu-id="4590d-168">-Confirm</span></span>
<span data-ttu-id="4590d-169">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4590d-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4590d-170">-WhatIf</span></span>
<span data-ttu-id="4590d-171">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4590d-172">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4590d-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4590d-173">CommonParameters</span></span>
<span data-ttu-id="4590d-174">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4590d-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4590d-175">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4590d-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4590d-176">입력</span><span class="sxs-lookup"><span data-stu-id="4590d-176">INPUTS</span></span>

### <span data-ttu-id="4590d-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4590d-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4590d-178">System.String</span><span class="sxs-lookup"><span data-stu-id="4590d-178">System.String</span></span>

## <span data-ttu-id="4590d-179">출력</span><span class="sxs-lookup"><span data-stu-id="4590d-179">OUTPUTS</span></span>

### <span data-ttu-id="4590d-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="4590d-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4590d-181">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4590d-181">NOTES</span></span>

## <span data-ttu-id="4590d-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4590d-182">RELATED LINKS</span></span>

[<span data-ttu-id="4590d-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="4590d-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="4590d-184">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="4590d-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="4590d-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="4590d-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="4590d-186">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="4590d-186">Set-AzResource</span></span>](./Set-AzResource.md)
