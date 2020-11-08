---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 0c4f351ca224991862e6b050462270fd64fd2a33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056059"
---
# <span data-ttu-id="53157-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="53157-101">New-AzResource</span></span>

## <span data-ttu-id="53157-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53157-102">SYNOPSIS</span></span>
<span data-ttu-id="53157-103">리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53157-103">Creates a resource.</span></span>

## <span data-ttu-id="53157-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53157-104">SYNTAX</span></span>

### <span data-ttu-id="53157-105">ByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="53157-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53157-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="53157-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53157-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="53157-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53157-108">설명은</span><span class="sxs-lookup"><span data-stu-id="53157-108">DESCRIPTION</span></span>
<span data-ttu-id="53157-109">**AzResource** cmdlet은 리소스 그룹에 웹 사이트, Azure sql 데이터베이스 서버 또는 Azure sql 데이터베이스 등의 azure 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53157-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="53157-110">예제의</span><span class="sxs-lookup"><span data-stu-id="53157-110">EXAMPLES</span></span>

### <span data-ttu-id="53157-111">예제 1: 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="53157-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="53157-112">이 명령은 ResourceGroup11의 웹 사이트인 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53157-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="53157-113">예제 2: splatting를 사용 하 여 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="53157-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="53157-114">이 명령은 ResourceGroup11의 웹 사이트인 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53157-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="53157-115">변수</span><span class="sxs-lookup"><span data-stu-id="53157-115">PARAMETERS</span></span>

### <span data-ttu-id="53157-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="53157-116">-ApiVersion</span></span>
<span data-ttu-id="53157-117">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="53157-118">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="53157-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53157-119">-AsJob</span></span>
<span data-ttu-id="53157-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="53157-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53157-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53157-121">-DefaultProfile</span></span>
<span data-ttu-id="53157-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="53157-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53157-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="53157-123">-ExtensionResourceName</span></span>
<span data-ttu-id="53157-124">리소스에 대 한 확장 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="53157-125">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. 서버 이름 `/` 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="53157-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="53157-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="53157-126">-ExtensionResourceType</span></span>
<span data-ttu-id="53157-127">확장 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="53157-128">예를 들어 확장 리소스가 데이터베이스인 경우 다음 형식을 지정 합니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="53157-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="53157-129">-Force</span><span class="sxs-lookup"><span data-stu-id="53157-129">-Force</span></span>
<span data-ttu-id="53157-130">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="53157-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="53157-131">-IsFullObject</span></span>
<span data-ttu-id="53157-132">*속성* 매개 변수에서 지정 하는 개체가 전체 개체 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="53157-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="53157-133">-종류</span><span class="sxs-lookup"><span data-stu-id="53157-133">-Kind</span></span>
<span data-ttu-id="53157-134">자원의 자원 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="53157-135">-위치</span><span class="sxs-lookup"><span data-stu-id="53157-135">-Location</span></span>
<span data-ttu-id="53157-136">리소스의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="53157-137">중앙 미국 또는 동남 아시아 등의 데이터 센터 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="53157-138">해당 형식의 리소스를 지 원하는 위치에 리소스를 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53157-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="53157-139">리소스 그룹에는 다른 위치의 리소스가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53157-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="53157-140">각 리소스 형식을 지 원하는 위치를 확인 하려면 Get-AzLocation cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="53157-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="53157-141">-ODataQuery</span></span>
<span data-ttu-id="53157-142">OData (Open Data Protocol) 스타일 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="53157-143">이 cmdlet은이 값을 다른 모든 필터 외에도 요청에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="53157-144">-계획</span><span class="sxs-lookup"><span data-stu-id="53157-144">-Plan</span></span>
<span data-ttu-id="53157-145">자원 계획 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="53157-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="53157-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="53157-146">-Pre</span></span>
<span data-ttu-id="53157-147">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="53157-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="53157-148">-속성</span><span class="sxs-lookup"><span data-stu-id="53157-148">-Properties</span></span>
<span data-ttu-id="53157-149">리소스에 대 한 리소스 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="53157-150">이 매개 변수를 사용 하 여 리소스 형식에 해당 하는 속성 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="53157-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53157-151">-ResourceGroupName</span></span>
<span data-ttu-id="53157-152">이 cmdlet이 리소스를 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="53157-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53157-153">-ResourceId</span></span>
<span data-ttu-id="53157-154">구독을 포함 하 여 정규화 된 리소스 ID를 다음 예제와 같이 지정 합니다. `/subscriptions/` 구독 ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="53157-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="53157-155">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="53157-155">-ResourceName</span></span>
<span data-ttu-id="53157-156">리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-156">Specifies the name of the resource.</span></span> <span data-ttu-id="53157-157">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="53157-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="53157-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="53157-158">-ResourceType</span></span>
<span data-ttu-id="53157-159">리소스의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="53157-160">예를 들어 데이터베이스의 경우 리소스 종류는 다음과 같습니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="53157-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="53157-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="53157-161">-Sku</span></span>
<span data-ttu-id="53157-162">Sku 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="53157-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="53157-163">태그</span><span class="sxs-lookup"><span data-stu-id="53157-163">-Tag</span></span>
<span data-ttu-id="53157-164">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="53157-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="53157-165">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="53157-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="53157-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="53157-166">-TenantLevel</span></span>
<span data-ttu-id="53157-167">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="53157-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="53157-168">-확인</span><span class="sxs-lookup"><span data-stu-id="53157-168">-Confirm</span></span>
<span data-ttu-id="53157-169">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53157-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53157-170">-WhatIf</span></span>
<span data-ttu-id="53157-171">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="53157-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53157-172">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53157-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53157-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53157-173">CommonParameters</span></span>
<span data-ttu-id="53157-174">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53157-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53157-175">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53157-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53157-176">입력</span><span class="sxs-lookup"><span data-stu-id="53157-176">INPUTS</span></span>

### <span data-ttu-id="53157-177">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="53157-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="53157-178">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="53157-178">System.String</span></span>

## <span data-ttu-id="53157-179">출력</span><span class="sxs-lookup"><span data-stu-id="53157-179">OUTPUTS</span></span>

### <span data-ttu-id="53157-180">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="53157-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="53157-181">상속자</span><span class="sxs-lookup"><span data-stu-id="53157-181">NOTES</span></span>

## <span data-ttu-id="53157-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53157-182">RELATED LINKS</span></span>

[<span data-ttu-id="53157-183">찾기-AzResource</span><span class="sxs-lookup"><span data-stu-id="53157-183">Find-AzResource</span></span>](./Find-AzResource.md)

[<span data-ttu-id="53157-184">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="53157-184">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="53157-185">이동-AzResource</span><span class="sxs-lookup"><span data-stu-id="53157-185">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="53157-186">제거-AzResource</span><span class="sxs-lookup"><span data-stu-id="53157-186">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="53157-187">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="53157-187">Set-AzResource</span></span>](./Set-AzResource.md)
