---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 0ccbabbb863b99aefd19b8f8a53257ac8c46faaa
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93711940"
---
# <span data-ttu-id="5aa0e-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="5aa0e-101">New-AzResource</span></span>

## <span data-ttu-id="5aa0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5aa0e-102">SYNOPSIS</span></span>
<span data-ttu-id="5aa0e-103">리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-103">Creates a resource.</span></span>

## <span data-ttu-id="5aa0e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5aa0e-104">SYNTAX</span></span>

### <span data-ttu-id="5aa0e-105">ByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="5aa0e-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5aa0e-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="5aa0e-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5aa0e-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="5aa0e-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5aa0e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5aa0e-108">DESCRIPTION</span></span>
<span data-ttu-id="5aa0e-109">**AzResource** cmdlet은 리소스 그룹에 웹 사이트, Azure sql 데이터베이스 서버 또는 Azure sql 데이터베이스 등의 azure 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="5aa0e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5aa0e-110">EXAMPLES</span></span>

### <span data-ttu-id="5aa0e-111">예제 1: 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="5aa0e-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="5aa0e-112">이 명령은 ResourceGroup11의 웹 사이트인 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="5aa0e-113">예제 2: splatting를 사용 하 여 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="5aa0e-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="5aa0e-114">이 명령은 ResourceGroup11의 웹 사이트인 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="5aa0e-115">변수</span><span class="sxs-lookup"><span data-stu-id="5aa0e-115">PARAMETERS</span></span>

### <span data-ttu-id="5aa0e-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5aa0e-116">-ApiVersion</span></span>
<span data-ttu-id="5aa0e-117">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="5aa0e-118">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5aa0e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5aa0e-119">-AsJob</span></span>
<span data-ttu-id="5aa0e-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5aa0e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5aa0e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aa0e-121">-DefaultProfile</span></span>
<span data-ttu-id="5aa0e-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5aa0e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5aa0e-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="5aa0e-123">-ExtensionResourceName</span></span>
<span data-ttu-id="5aa0e-124">리소스에 대 한 확장 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="5aa0e-125">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. 서버 이름 `/` 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="5aa0e-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="5aa0e-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="5aa0e-126">-ExtensionResourceType</span></span>
<span data-ttu-id="5aa0e-127">확장 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="5aa0e-128">예를 들어 확장 리소스가 데이터베이스인 경우 다음 형식을 지정 합니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="5aa0e-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="5aa0e-129">-Force</span><span class="sxs-lookup"><span data-stu-id="5aa0e-129">-Force</span></span>
<span data-ttu-id="5aa0e-130">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5aa0e-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="5aa0e-131">-IsFullObject</span></span>
<span data-ttu-id="5aa0e-132">*속성* 매개 변수에서 지정 하는 개체가 전체 개체 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="5aa0e-133">-종류</span><span class="sxs-lookup"><span data-stu-id="5aa0e-133">-Kind</span></span>
<span data-ttu-id="5aa0e-134">자원의 자원 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="5aa0e-135">-위치</span><span class="sxs-lookup"><span data-stu-id="5aa0e-135">-Location</span></span>
<span data-ttu-id="5aa0e-136">리소스의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="5aa0e-137">중앙 미국 또는 동남 아시아 등의 데이터 센터 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="5aa0e-138">해당 형식의 리소스를 지 원하는 위치에 리소스를 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="5aa0e-139">리소스 그룹에는 다른 위치의 리소스가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="5aa0e-140">각 리소스 형식을 지 원하는 위치를 확인 하려면 Get-AzLocation cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="5aa0e-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="5aa0e-141">-ODataQuery</span></span>
<span data-ttu-id="5aa0e-142">OData (Open Data Protocol) 스타일 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="5aa0e-143">이 cmdlet은이 값을 다른 모든 필터 외에도 요청에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="5aa0e-144">-계획</span><span class="sxs-lookup"><span data-stu-id="5aa0e-144">-Plan</span></span>
<span data-ttu-id="5aa0e-145">자원 계획 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="5aa0e-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="5aa0e-146">-Pre</span></span>
<span data-ttu-id="5aa0e-147">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5aa0e-148">-속성</span><span class="sxs-lookup"><span data-stu-id="5aa0e-148">-Properties</span></span>
<span data-ttu-id="5aa0e-149">리소스에 대 한 리소스 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="5aa0e-150">이 매개 변수를 사용 하 여 리소스 형식에 해당 하는 속성 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="5aa0e-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aa0e-151">-ResourceGroupName</span></span>
<span data-ttu-id="5aa0e-152">이 cmdlet이 리소스를 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="5aa0e-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5aa0e-153">-ResourceId</span></span>
<span data-ttu-id="5aa0e-154">구독을 포함 하 여 정규화 된 리소스 ID를 다음 예제와 같이 지정 합니다. `/subscriptions/` 구독 ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="5aa0e-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="5aa0e-155">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="5aa0e-155">-ResourceName</span></span>
<span data-ttu-id="5aa0e-156">리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-156">Specifies the name of the resource.</span></span> <span data-ttu-id="5aa0e-157">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="5aa0e-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="5aa0e-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5aa0e-158">-ResourceType</span></span>
<span data-ttu-id="5aa0e-159">리소스의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="5aa0e-160">예를 들어 데이터베이스의 경우 리소스 종류는 다음과 같습니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="5aa0e-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="5aa0e-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="5aa0e-161">-Sku</span></span>
<span data-ttu-id="5aa0e-162">Sku 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="5aa0e-163">태그</span><span class="sxs-lookup"><span data-stu-id="5aa0e-163">-Tag</span></span>
<span data-ttu-id="5aa0e-164">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5aa0e-165">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5aa0e-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5aa0e-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="5aa0e-166">-TenantLevel</span></span>
<span data-ttu-id="5aa0e-167">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="5aa0e-168">-확인</span><span class="sxs-lookup"><span data-stu-id="5aa0e-168">-Confirm</span></span>
<span data-ttu-id="5aa0e-169">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aa0e-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aa0e-170">-WhatIf</span></span>
<span data-ttu-id="5aa0e-171">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aa0e-172">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aa0e-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aa0e-173">CommonParameters</span></span>
<span data-ttu-id="5aa0e-174">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa0e-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aa0e-175">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aa0e-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aa0e-176">입력</span><span class="sxs-lookup"><span data-stu-id="5aa0e-176">INPUTS</span></span>

### <span data-ttu-id="5aa0e-177">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="5aa0e-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5aa0e-178">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5aa0e-178">System.String</span></span>

## <span data-ttu-id="5aa0e-179">출력</span><span class="sxs-lookup"><span data-stu-id="5aa0e-179">OUTPUTS</span></span>

### <span data-ttu-id="5aa0e-180">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="5aa0e-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5aa0e-181">상속자</span><span class="sxs-lookup"><span data-stu-id="5aa0e-181">NOTES</span></span>

## <span data-ttu-id="5aa0e-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5aa0e-182">RELATED LINKS</span></span>

[<span data-ttu-id="5aa0e-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="5aa0e-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="5aa0e-184">이동-AzResource</span><span class="sxs-lookup"><span data-stu-id="5aa0e-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="5aa0e-185">제거-AzResource</span><span class="sxs-lookup"><span data-stu-id="5aa0e-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="5aa0e-186">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="5aa0e-186">Set-AzResource</span></span>](./Set-AzResource.md)
