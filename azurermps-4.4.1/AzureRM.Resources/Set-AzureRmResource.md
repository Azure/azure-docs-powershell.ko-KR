---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: d3e7a1e947eb03c52c2cd8e032a359eb7765be03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710952"
---
# <span data-ttu-id="667e2-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="667e2-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="667e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="667e2-102">SYNOPSIS</span></span>
<span data-ttu-id="667e2-103">리소스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="667e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="667e2-104">SYNTAX</span></span>

### <span data-ttu-id="667e2-105">리소스 Id입니다. (기본값)</span><span class="sxs-lookup"><span data-stu-id="667e2-105">The resource Id. (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="667e2-106">구독 수준에 있는 리소스</span><span class="sxs-lookup"><span data-stu-id="667e2-106">Resource that resides at the subscription level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667e2-107">테 넌 트 수준에 있는 리소스</span><span class="sxs-lookup"><span data-stu-id="667e2-107">Resource that resides at the tenant level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="667e2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="667e2-108">DESCRIPTION</span></span>
<span data-ttu-id="667e2-109">**Set-AzureRmResource** cmdlet은 기존 Azure 리소스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="667e2-110">이름 및 형식 또는 ID를 기준으로 수정할 리소스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="667e2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="667e2-111">EXAMPLES</span></span>

### <span data-ttu-id="667e2-112">예제 1: 리소스 수정</span><span class="sxs-lookup"><span data-stu-id="667e2-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="667e2-113">첫 번째 명령은 Get-AzureRmResource cmdlet을 사용 하 여 ContosoSite 이라는 리소스를 가져온 다음 $Resource 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="667e2-114">두 번째 명령은 $Resource의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="667e2-115">마지막 명령은 $Resource 일치 하도록 리소스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="667e2-116">변수</span><span class="sxs-lookup"><span data-stu-id="667e2-116">PARAMETERS</span></span>

### <span data-ttu-id="667e2-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="667e2-117">-ApiVersion</span></span>
<span data-ttu-id="667e2-118">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="667e2-119">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="667e2-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="667e2-120">-ExtensionResourceName</span></span>
<span data-ttu-id="667e2-121">리소스에 대 한 확장 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-121">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="667e2-122">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-122">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="667e2-123">서버 이름 `/` 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="667e2-123">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667e2-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="667e2-124">-ExtensionResourceType</span></span>
<span data-ttu-id="667e2-125">확장 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="667e2-126">예를 들어 확장 리소스가 데이터베이스인 경우 다음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-126">For instance, if the extension resource is a database specify the following:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667e2-127">-Force</span><span class="sxs-lookup"><span data-stu-id="667e2-127">-Force</span></span>
<span data-ttu-id="667e2-128">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="667e2-129">-종류</span><span class="sxs-lookup"><span data-stu-id="667e2-129">-Kind</span></span>
<span data-ttu-id="667e2-130">자원의 자원 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-130">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="667e2-131">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="667e2-131">-ODataQuery</span></span>
<span data-ttu-id="667e2-132">OData (Open Data Protocol) 스타일 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-132">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="667e2-133">이 cmdlet은이 값을 다른 모든 필터 외에도 요청에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-133">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="667e2-134">-계획</span><span class="sxs-lookup"><span data-stu-id="667e2-134">-Plan</span></span>
<span data-ttu-id="667e2-135">리소스에 대 한 리소스 계획 속성을 해시 테이블로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-135">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="667e2-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="667e2-136">-Pre</span></span>
<span data-ttu-id="667e2-137">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="667e2-138">-속성</span><span class="sxs-lookup"><span data-stu-id="667e2-138">-Properties</span></span>
<span data-ttu-id="667e2-139">리소스에 대 한 리소스 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-139">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="667e2-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="667e2-140">-ResourceGroupName</span></span>
<span data-ttu-id="667e2-141">이 cmdlet이 리소스를 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-141">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667e2-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="667e2-142">-ResourceId</span></span>
<span data-ttu-id="667e2-143">다음 예제와 같이 구독을 포함 하 여 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-143">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="667e2-144">`/subscriptions/`구독 ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="667e2-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667e2-145">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="667e2-145">-ResourceName</span></span>
<span data-ttu-id="667e2-146">리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-146">Specifies the name of the resource.</span></span>
<span data-ttu-id="667e2-147">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-147">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667e2-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="667e2-148">-ResourceType</span></span>
<span data-ttu-id="667e2-149">리소스의 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-149">Specifies the type of the resource.</span></span>
<span data-ttu-id="667e2-150">예를 들어 데이터베이스의 경우 리소스 종류는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-150">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="667e2-151">-Sku</span><span class="sxs-lookup"><span data-stu-id="667e2-151">-Sku</span></span>
<span data-ttu-id="667e2-152">리소스의 SKU 개체를 해시 테이블로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-152">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="667e2-153">태그</span><span class="sxs-lookup"><span data-stu-id="667e2-153">-Tag</span></span>
<span data-ttu-id="667e2-154">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="667e2-155">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="667e2-155">For example:</span></span>

<span data-ttu-id="667e2-156">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="667e2-156">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="667e2-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="667e2-157">-TenantLevel</span></span>
<span data-ttu-id="667e2-158">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-158">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667e2-159">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="667e2-159">-UsePatchSemantics</span></span>
<span data-ttu-id="667e2-160">HTTP를 사용 하지 않고이 cmdlet이 HTTP 패치를 사용 하 여 개체를 업데이트 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-160">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="667e2-161">-확인</span><span class="sxs-lookup"><span data-stu-id="667e2-161">-Confirm</span></span>
<span data-ttu-id="667e2-162">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="667e2-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="667e2-163">-WhatIf</span></span>
<span data-ttu-id="667e2-164">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="667e2-165">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="667e2-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667e2-166">-DefaultProfile</span></span>
<span data-ttu-id="667e2-167">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="667e2-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667e2-168">CommonParameters</span></span>
<span data-ttu-id="667e2-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="667e2-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667e2-170">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="667e2-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667e2-171">입력</span><span class="sxs-lookup"><span data-stu-id="667e2-171">INPUTS</span></span>

## <span data-ttu-id="667e2-172">출력</span><span class="sxs-lookup"><span data-stu-id="667e2-172">OUTPUTS</span></span>

### <span data-ttu-id="667e2-173">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="667e2-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="667e2-174">상속자</span><span class="sxs-lookup"><span data-stu-id="667e2-174">NOTES</span></span>

## <span data-ttu-id="667e2-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="667e2-175">RELATED LINKS</span></span>

[<span data-ttu-id="667e2-176">찾기-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="667e2-176">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="667e2-177">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="667e2-177">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="667e2-178">이동-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="667e2-178">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="667e2-179">새로운 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="667e2-179">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="667e2-180">제거-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="667e2-180">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
