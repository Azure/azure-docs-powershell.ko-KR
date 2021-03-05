---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: 6d2dd13f08fd9e621f30f586e7c46c828387e31e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963771"
---
# <span data-ttu-id="a32ee-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="a32ee-101">Remove-AzResource</span></span>

## <span data-ttu-id="a32ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a32ee-102">SYNOPSIS</span></span>
<span data-ttu-id="a32ee-103">리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-103">Removes a resource.</span></span>

## <span data-ttu-id="a32ee-104">구문</span><span class="sxs-lookup"><span data-stu-id="a32ee-104">SYNTAX</span></span>

### <span data-ttu-id="a32ee-105">ByResourceId(기본값)</span><span class="sxs-lookup"><span data-stu-id="a32ee-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a32ee-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="a32ee-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a32ee-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="a32ee-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a32ee-108">설명</span><span class="sxs-lookup"><span data-stu-id="a32ee-108">DESCRIPTION</span></span>
<span data-ttu-id="a32ee-109">**Remove-AzResource** cmdlet은 Azure 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="a32ee-110">예제</span><span class="sxs-lookup"><span data-stu-id="a32ee-110">EXAMPLES</span></span>

### <span data-ttu-id="a32ee-111">예제 1: 웹 사이트 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="a32ee-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="a32ee-112">이 명령은 ContosoSite라는 웹 사이트 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="a32ee-113">이 예제에서는 구독 ID에 대해 자리 1개 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="a32ee-114">명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="a32ee-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a32ee-115">따라서 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a32ee-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a32ee-116">PARAMETERS</span></span>

### <span data-ttu-id="a32ee-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a32ee-117">-ApiVersion</span></span>
<span data-ttu-id="a32ee-118">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a32ee-119">버전을 지정하지 않으면 이 cmdlet에서는 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a32ee-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a32ee-120">-AsJob</span></span>
<span data-ttu-id="a32ee-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a32ee-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a32ee-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a32ee-122">-DefaultProfile</span></span>
<span data-ttu-id="a32ee-123">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a32ee-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a32ee-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="a32ee-124">-ExtensionResourceName</span></span>
<span data-ttu-id="a32ee-125">이 cmdlet이 제거한 리소스의 확장 리소스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="a32ee-126">예를 들어 데이터베이스를 지정하려면 서버 이름 데이터베이스 이름 형식을 `/` 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="a32ee-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="a32ee-127">-ExtensionResourceType</span></span>
<span data-ttu-id="a32ee-128">확장 리소스에 대한 리소스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="a32ee-129">리소스에 대한 확장 리소스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="a32ee-130">예를 들어: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="a32ee-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="a32ee-131">-Force</span><span class="sxs-lookup"><span data-stu-id="a32ee-131">-Force</span></span>
<span data-ttu-id="a32ee-132">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a32ee-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="a32ee-133">-ODataQuery</span></span>
<span data-ttu-id="a32ee-134">OData(Open Data Protocol) 스타일 필터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="a32ee-135">이 cmdlet은 다른 필터 외에도 요청에 이 값을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="a32ee-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="a32ee-136">-Pre</span></span>
<span data-ttu-id="a32ee-137">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a32ee-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a32ee-138">-ResourceGroupName</span></span>
<span data-ttu-id="a32ee-139">이 cmdlet에서 리소스를 제거하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="a32ee-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a32ee-140">-ResourceId</span></span>
<span data-ttu-id="a32ee-141">이 cmdlet이 제거한 리소스의 완전히 자격을 갖춘 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="a32ee-142">ID에는 다음 예제와 같이 `/subscriptions/` 구독이 포함됩니다.`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a32ee-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a32ee-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a32ee-143">-ResourceName</span></span>
<span data-ttu-id="a32ee-144">이 cmdlet에서 제거한 리소스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="a32ee-145">예를 들어 데이터베이스를 지정하려면 다음 형식을 사용합니다. `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a32ee-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a32ee-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a32ee-146">-ResourceType</span></span>
<span data-ttu-id="a32ee-147">이 cmdlet에서 제거하는 리소스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="a32ee-148">예를 들어 데이터베이스의 경우 리소스 유형은 다음과 같습니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="a32ee-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="a32ee-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a32ee-149">-TenantLevel</span></span>
<span data-ttu-id="a32ee-150">이 cmdlet이 테넌트 수준에서 작동하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="a32ee-151">-확인</span><span class="sxs-lookup"><span data-stu-id="a32ee-151">-Confirm</span></span>
<span data-ttu-id="a32ee-152">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a32ee-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a32ee-153">-WhatIf</span></span>
<span data-ttu-id="a32ee-154">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a32ee-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a32ee-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a32ee-156">CommonParameters</span></span>
<span data-ttu-id="a32ee-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a32ee-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a32ee-158">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a32ee-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a32ee-159">입력</span><span class="sxs-lookup"><span data-stu-id="a32ee-159">INPUTS</span></span>

### <span data-ttu-id="a32ee-160">System.String</span><span class="sxs-lookup"><span data-stu-id="a32ee-160">System.String</span></span>

## <span data-ttu-id="a32ee-161">출력</span><span class="sxs-lookup"><span data-stu-id="a32ee-161">OUTPUTS</span></span>

### <span data-ttu-id="a32ee-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a32ee-162">System.Boolean</span></span>

## <span data-ttu-id="a32ee-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a32ee-163">NOTES</span></span>

## <span data-ttu-id="a32ee-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a32ee-164">RELATED LINKS</span></span>

[<span data-ttu-id="a32ee-165">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="a32ee-165">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="a32ee-166">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="a32ee-166">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="a32ee-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="a32ee-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="a32ee-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="a32ee-168">Set-AzResource</span></span>](./Set-AzResource.md)


