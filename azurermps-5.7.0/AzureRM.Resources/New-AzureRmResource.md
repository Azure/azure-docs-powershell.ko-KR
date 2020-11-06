---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: c7a98f6fba2c690fb296c42f4f6eca902d7678bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528837"
---
# <span data-ttu-id="e5919-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e5919-101">New-AzureRmResource</span></span>

## <span data-ttu-id="e5919-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5919-102">SYNOPSIS</span></span>
<span data-ttu-id="e5919-103">리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5919-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5919-104">SYNTAX</span></span>

### <span data-ttu-id="e5919-105">ByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="e5919-105">ByResourceId (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5919-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e5919-106">BySubscriptionLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5919-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="e5919-107">ByTenantLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5919-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e5919-108">DESCRIPTION</span></span>
<span data-ttu-id="e5919-109">**AzureRmResource** cmdlet은 리소스 그룹에 웹 사이트, Azure sql 데이터베이스 서버 또는 Azure sql 데이터베이스 등의 azure 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="e5919-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e5919-110">EXAMPLES</span></span>

### <span data-ttu-id="e5919-111">예제 1: 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="e5919-111">Example 1: Create a resource</span></span>
```
PS> New-AzureRmResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="e5919-112">이 명령은 ResourceGroup11의 웹 사이트인 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="e5919-113">예제 2: splatting를 사용 하 여 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="e5919-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US" 
    Properties        = @{test = "test"} 
    ResourceName      = "TestSite06" 
    ResourceType      = "microsoft.web/sites" 
    ResourceGroupName = "ResourceGroup11" 
    Force             = $true
}

PS> New-AzureRmResource @prop
```

<span data-ttu-id="e5919-114">이 명령은 ResourceGroup11의 웹 사이트인 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="e5919-115">변수</span><span class="sxs-lookup"><span data-stu-id="e5919-115">PARAMETERS</span></span>

### <span data-ttu-id="e5919-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e5919-116">-ApiVersion</span></span>
<span data-ttu-id="e5919-117">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="e5919-118">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5919-119">-AsJob</span></span>
<span data-ttu-id="e5919-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e5919-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5919-121">-DefaultProfile</span></span>
<span data-ttu-id="e5919-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e5919-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="e5919-123">-ExtensionResourceName</span></span>
<span data-ttu-id="e5919-124">리소스에 대 한 확장 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="e5919-125">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-125">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="e5919-126">서버 이름 `/` 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="e5919-126">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="e5919-127">-ExtensionResourceType</span></span>
<span data-ttu-id="e5919-128">확장 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="e5919-129">예를 들어 확장 리소스가 데이터베이스인 경우 다음 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-129">For instance, if the extension resource is a database, specify the following type:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-130">-Force</span><span class="sxs-lookup"><span data-stu-id="e5919-130">-Force</span></span>
<span data-ttu-id="e5919-131">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-132">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="e5919-132">-IsFullObject</span></span>
<span data-ttu-id="e5919-133">*속성* 매개 변수에서 지정 하는 개체가 전체 개체 임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-133">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-134">-종류</span><span class="sxs-lookup"><span data-stu-id="e5919-134">-Kind</span></span>
<span data-ttu-id="e5919-135">자원의 자원 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-135">Specifies the resource kind for the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-136">-위치</span><span class="sxs-lookup"><span data-stu-id="e5919-136">-Location</span></span>
<span data-ttu-id="e5919-137">리소스의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-137">Specifies the location of the resource.</span></span>
<span data-ttu-id="e5919-138">중앙 미국 또는 동남 아시아 등의 데이터 센터 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-138">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="e5919-139">해당 형식의 리소스를 지 원하는 위치에 리소스를 배치할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-139">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="e5919-140">리소스 그룹에는 다른 위치의 리소스가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-140">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="e5919-141">각 리소스 형식을 지 원하는 위치를 확인 하려면 Get-AzureLocation cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-141">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-142">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="e5919-142">-ODataQuery</span></span>
<span data-ttu-id="e5919-143">OData (Open Data Protocol) 스타일 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-143">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="e5919-144">이 cmdlet은이 값을 다른 모든 필터 외에도 요청에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-144">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-145">-계획</span><span class="sxs-lookup"><span data-stu-id="e5919-145">-Plan</span></span>
<span data-ttu-id="e5919-146">자원 계획 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-146">A hash table that represents resource plan properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="e5919-147">-Pre</span></span>
<span data-ttu-id="e5919-148">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-149">-속성</span><span class="sxs-lookup"><span data-stu-id="e5919-149">-Properties</span></span>
<span data-ttu-id="e5919-150">리소스에 대 한 리소스 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-150">Specifies resource properties for the resource.</span></span> <span data-ttu-id="e5919-151">이 매개 변수를 사용 하 여 리소스 형식에 해당 하는 속성 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-151">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5919-152">-ResourceGroupName</span></span>
<span data-ttu-id="e5919-153">이 cmdlet이 리소스를 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-153">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5919-154">-ResourceId</span></span>
<span data-ttu-id="e5919-155">다음 예제와 같이 구독을 포함 하 여 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-155">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="e5919-156">`/subscriptions/`구독 ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e5919-156">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-157">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="e5919-157">-ResourceName</span></span>
<span data-ttu-id="e5919-158">리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-158">Specifies the name of the resource.</span></span> <span data-ttu-id="e5919-159">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-159">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-160">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e5919-160">-ResourceType</span></span>
<span data-ttu-id="e5919-161">리소스의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-161">Specifies the type of the resource.</span></span>
<span data-ttu-id="e5919-162">예를 들어 데이터베이스의 경우 리소스 종류는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-162">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-163">-Sku</span><span class="sxs-lookup"><span data-stu-id="e5919-163">-Sku</span></span>
<span data-ttu-id="e5919-164">Sku 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-164">A hash table that represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-165">태그</span><span class="sxs-lookup"><span data-stu-id="e5919-165">-Tag</span></span>
<span data-ttu-id="e5919-166">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-166">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e5919-167">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="e5919-167">For example:</span></span>

<span data-ttu-id="e5919-168">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e5919-168">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-169">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="e5919-169">-TenantLevel</span></span>
<span data-ttu-id="e5919-170">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-170">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-171">-확인</span><span class="sxs-lookup"><span data-stu-id="e5919-171">-Confirm</span></span>
<span data-ttu-id="e5919-172">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5919-173">-WhatIf</span></span>
<span data-ttu-id="e5919-174">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5919-175">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5919-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5919-176">CommonParameters</span></span>
<span data-ttu-id="e5919-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5919-178">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5919-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5919-179">입력</span><span class="sxs-lookup"><span data-stu-id="e5919-179">INPUTS</span></span>

### <span data-ttu-id="e5919-180">않아야</span><span class="sxs-lookup"><span data-stu-id="e5919-180">None</span></span>
<span data-ttu-id="e5919-181">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5919-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5919-182">출력</span><span class="sxs-lookup"><span data-stu-id="e5919-182">OUTPUTS</span></span>

### <span data-ttu-id="e5919-183">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="e5919-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e5919-184">상속자</span><span class="sxs-lookup"><span data-stu-id="e5919-184">NOTES</span></span>

## <span data-ttu-id="e5919-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5919-185">RELATED LINKS</span></span>

[<span data-ttu-id="e5919-186">찾기-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e5919-186">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="e5919-187">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e5919-187">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="e5919-188">이동-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e5919-188">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="e5919-189">제거-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e5919-189">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="e5919-190">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e5919-190">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
