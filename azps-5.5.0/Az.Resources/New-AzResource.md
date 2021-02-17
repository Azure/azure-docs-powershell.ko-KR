---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 37561ecc57f5b729a33b2011c26a297bcb2bf52b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192737"
---
# <span data-ttu-id="94e7d-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="94e7d-101">New-AzResource</span></span>

## <span data-ttu-id="94e7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="94e7d-103">리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-103">Creates a resource.</span></span>

## <span data-ttu-id="94e7d-104">구문</span><span class="sxs-lookup"><span data-stu-id="94e7d-104">SYNTAX</span></span>

### <span data-ttu-id="94e7d-105">ByResourceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="94e7d-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94e7d-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="94e7d-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94e7d-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="94e7d-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94e7d-108">설명</span><span class="sxs-lookup"><span data-stu-id="94e7d-108">DESCRIPTION</span></span>
<span data-ttu-id="94e7d-109">**New-AzResource** cmdlet은 웹 사이트, Azure SQL Database 서버 또는 Azure SQL Database와 같은 Azure 리소스를 리소스 그룹에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="94e7d-110">예제</span><span class="sxs-lookup"><span data-stu-id="94e7d-110">EXAMPLES</span></span>

### <span data-ttu-id="94e7d-111">예제 1: 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="94e7d-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="94e7d-112">이 명령은 ResourceGroup11에서 웹 사이트인 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="94e7d-113">예제 2: 스플래팅을 사용하여 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="94e7d-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="94e7d-114">이 명령은 ResourceGroup11에서 웹 사이트인 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="94e7d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94e7d-115">PARAMETERS</span></span>

### <span data-ttu-id="94e7d-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="94e7d-116">-ApiVersion</span></span>
<span data-ttu-id="94e7d-117">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="94e7d-118">버전을 지정하지 않으면 이 cmdlet은 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="94e7d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94e7d-119">-AsJob</span></span>
<span data-ttu-id="94e7d-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="94e7d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94e7d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e7d-121">-DefaultProfile</span></span>
<span data-ttu-id="94e7d-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="94e7d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94e7d-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="94e7d-123">-ExtensionResourceName</span></span>
<span data-ttu-id="94e7d-124">리소스에 대한 확장 리소스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="94e7d-125">예를 들어 데이터베이스를 지정하려면 다음 형식을 사용합니다. 서버 이름 `/` 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="94e7d-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="94e7d-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="94e7d-126">-ExtensionResourceType</span></span>
<span data-ttu-id="94e7d-127">확장 리소스에 대한 리소스 종류를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="94e7d-128">예를 들어 확장 리소스가 데이터베이스인 경우 다음 형식을 지정합니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="94e7d-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="94e7d-129">-Force</span><span class="sxs-lookup"><span data-stu-id="94e7d-129">-Force</span></span>
<span data-ttu-id="94e7d-130">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="94e7d-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="94e7d-131">-IsFullObject</span></span>
<span data-ttu-id="94e7d-132">*Properties* 매개 변수가 지정하는 개체가 전체 개체임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="94e7d-133">-Kind</span><span class="sxs-lookup"><span data-stu-id="94e7d-133">-Kind</span></span>
<span data-ttu-id="94e7d-134">리소스에 대한 리소스 종류를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="94e7d-135">-Location</span><span class="sxs-lookup"><span data-stu-id="94e7d-135">-Location</span></span>
<span data-ttu-id="94e7d-136">리소스의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="94e7d-137">미국 중부 또는 동남 아시아와 같은 데이터 센터 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="94e7d-138">해당 유형의 리소스를 지원하는 모든 위치에 리소스를 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="94e7d-139">리소스 그룹에는 다른 위치의 리소스가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="94e7d-140">각 리소스 종류를 지원하는 위치를 결정하기 위해 Get-AzLocation cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="94e7d-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="94e7d-141">-ODataQuery</span></span>
<span data-ttu-id="94e7d-142">OData(Open Data Protocol) 스타일 필터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="94e7d-143">이 cmdlet은 다른 필터 외에도 요청에 이 값을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="94e7d-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="94e7d-144">-Plan</span></span>
<span data-ttu-id="94e7d-145">리소스 계획 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="94e7d-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="94e7d-146">-Pre</span></span>
<span data-ttu-id="94e7d-147">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="94e7d-148">-Properties</span><span class="sxs-lookup"><span data-stu-id="94e7d-148">-Properties</span></span>
<span data-ttu-id="94e7d-149">리소스에 대한 리소스 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="94e7d-150">이 매개 변수를 사용하여 리소스 종류에 특정된 속성 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="94e7d-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94e7d-151">-ResourceGroupName</span></span>
<span data-ttu-id="94e7d-152">이 cmdlet이 리소스를 만드는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="94e7d-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94e7d-153">-ResourceId</span></span>
<span data-ttu-id="94e7d-154">다음 예제와 같이 구독을 포함한 정식 리소스 `/subscriptions/` ID를 지정합니다.`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="94e7d-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="94e7d-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="94e7d-155">-ResourceName</span></span>
<span data-ttu-id="94e7d-156">리소스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-156">Specifies the name of the resource.</span></span> <span data-ttu-id="94e7d-157">예를 들어 데이터베이스를 지정하려면 다음 형식을 사용합니다. `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="94e7d-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="94e7d-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="94e7d-158">-ResourceType</span></span>
<span data-ttu-id="94e7d-159">리소스의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="94e7d-160">예를 들어 데이터베이스의 경우 리소스 종류는 다음과 같습니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="94e7d-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="94e7d-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="94e7d-161">-Sku</span></span>
<span data-ttu-id="94e7d-162">SKU 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="94e7d-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="94e7d-163">-Tag</span></span>
<span data-ttu-id="94e7d-164">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="94e7d-165">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="94e7d-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="94e7d-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="94e7d-166">-TenantLevel</span></span>
<span data-ttu-id="94e7d-167">이 cmdlet이 테넌트 수준에서 작동하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="94e7d-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94e7d-168">-Confirm</span></span>
<span data-ttu-id="94e7d-169">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94e7d-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94e7d-170">-WhatIf</span></span>
<span data-ttu-id="94e7d-171">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="94e7d-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94e7d-172">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94e7d-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e7d-173">CommonParameters</span></span>
<span data-ttu-id="94e7d-174">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="94e7d-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e7d-175">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="94e7d-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e7d-176">입력</span><span class="sxs-lookup"><span data-stu-id="94e7d-176">INPUTS</span></span>

### <span data-ttu-id="94e7d-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="94e7d-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="94e7d-178">System.String</span><span class="sxs-lookup"><span data-stu-id="94e7d-178">System.String</span></span>

## <span data-ttu-id="94e7d-179">출력</span><span class="sxs-lookup"><span data-stu-id="94e7d-179">OUTPUTS</span></span>

### <span data-ttu-id="94e7d-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="94e7d-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="94e7d-181">참고 사항</span><span class="sxs-lookup"><span data-stu-id="94e7d-181">NOTES</span></span>

## <span data-ttu-id="94e7d-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94e7d-182">RELATED LINKS</span></span>

[<span data-ttu-id="94e7d-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="94e7d-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="94e7d-184">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="94e7d-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="94e7d-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="94e7d-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="94e7d-186">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="94e7d-186">Set-AzResource</span></span>](./Set-AzResource.md)
