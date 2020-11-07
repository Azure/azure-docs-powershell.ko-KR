---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: cbe72ac0c1b62a11b48113bd9043118f3750f37b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704121"
---
# <span data-ttu-id="4cf9e-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="4cf9e-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="4cf9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cf9e-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf9e-103">리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cf9e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4cf9e-104">SYNTAX</span></span>

### <span data-ttu-id="4cf9e-105">ByResourceId (기본값)</span><span class="sxs-lookup"><span data-stu-id="4cf9e-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cf9e-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="4cf9e-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4cf9e-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="4cf9e-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cf9e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4cf9e-108">DESCRIPTION</span></span>
<span data-ttu-id="4cf9e-109">**AzureRmResource** Cmdlet은 Azure 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="4cf9e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4cf9e-110">EXAMPLES</span></span>

### <span data-ttu-id="4cf9e-111">예제 1: 웹 사이트 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="4cf9e-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="4cf9e-112">이 명령은 ContosoSite 이라는 웹 사이트 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="4cf9e-113">이 예제에서는 구독 ID에 대 한 자리 표시자 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="4cf9e-114">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="4cf9e-115">따라서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4cf9e-116">변수</span><span class="sxs-lookup"><span data-stu-id="4cf9e-116">PARAMETERS</span></span>

### <span data-ttu-id="4cf9e-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4cf9e-117">-ApiVersion</span></span>
<span data-ttu-id="4cf9e-118">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4cf9e-119">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4cf9e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4cf9e-120">-AsJob</span></span>
<span data-ttu-id="4cf9e-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4cf9e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4cf9e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf9e-122">-DefaultProfile</span></span>
<span data-ttu-id="4cf9e-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4cf9e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cf9e-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="4cf9e-124">-ExtensionResourceName</span></span>
<span data-ttu-id="4cf9e-125">이 cmdlet이 제거 하는 리소스의 확장 리소스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="4cf9e-126">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. 서버 이름 `/` 데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="4cf9e-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="4cf9e-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="4cf9e-127">-ExtensionResourceType</span></span>
<span data-ttu-id="4cf9e-128">확장 리소스의 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="4cf9e-129">자원에 대 한 확장 리소스 종류를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="4cf9e-130">예를 들면 다음과 같습니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="4cf9e-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="4cf9e-131">-Force</span><span class="sxs-lookup"><span data-stu-id="4cf9e-131">-Force</span></span>
<span data-ttu-id="4cf9e-132">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4cf9e-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="4cf9e-133">-ODataQuery</span></span>
<span data-ttu-id="4cf9e-134">OData (Open Data Protocol) 스타일 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="4cf9e-135">이 cmdlet은이 값을 다른 모든 필터 외에도 요청에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="4cf9e-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="4cf9e-136">-Pre</span></span>
<span data-ttu-id="4cf9e-137">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4cf9e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cf9e-138">-ResourceGroupName</span></span>
<span data-ttu-id="4cf9e-139">이 cmdlet이 리소스를 제거할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="4cf9e-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cf9e-140">-ResourceId</span></span>
<span data-ttu-id="4cf9e-141">이 cmdlet이 제거 하는 리소스의 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="4cf9e-142">ID에는 다음 예제와 같이 구독이 포함 됩니다. `/subscriptions/` 구독 ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="4cf9e-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="4cf9e-143">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="4cf9e-143">-ResourceName</span></span>
<span data-ttu-id="4cf9e-144">이 cmdlet이 제거 하는 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="4cf9e-145">예를 들어 데이터베이스를 지정 하려면 다음 형식을 사용 합니다. `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="4cf9e-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="4cf9e-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4cf9e-146">-ResourceType</span></span>
<span data-ttu-id="4cf9e-147">이 cmdlet이 제거 하는 리소스의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="4cf9e-148">예를 들어 데이터베이스의 경우 리소스 종류는 다음과 같습니다. `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="4cf9e-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="4cf9e-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="4cf9e-149">-TenantLevel</span></span>
<span data-ttu-id="4cf9e-150">이 cmdlet이 테 넌 트 수준에서 작동 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="4cf9e-151">-확인</span><span class="sxs-lookup"><span data-stu-id="4cf9e-151">-Confirm</span></span>
<span data-ttu-id="4cf9e-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cf9e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cf9e-153">-WhatIf</span></span>
<span data-ttu-id="4cf9e-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cf9e-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cf9e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf9e-156">CommonParameters</span></span>
<span data-ttu-id="4cf9e-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf9e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf9e-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cf9e-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf9e-159">입력</span><span class="sxs-lookup"><span data-stu-id="4cf9e-159">INPUTS</span></span>

### <span data-ttu-id="4cf9e-160">않아야</span><span class="sxs-lookup"><span data-stu-id="4cf9e-160">None</span></span>

## <span data-ttu-id="4cf9e-161">출력</span><span class="sxs-lookup"><span data-stu-id="4cf9e-161">OUTPUTS</span></span>

### <span data-ttu-id="4cf9e-162">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="4cf9e-162">System.Boolean</span></span>

## <span data-ttu-id="4cf9e-163">상속자</span><span class="sxs-lookup"><span data-stu-id="4cf9e-163">NOTES</span></span>

## <span data-ttu-id="4cf9e-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cf9e-164">RELATED LINKS</span></span>

[<span data-ttu-id="4cf9e-165">찾기-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="4cf9e-165">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="4cf9e-166">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="4cf9e-166">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="4cf9e-167">이동-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="4cf9e-167">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="4cf9e-168">새로운 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="4cf9e-168">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="4cf9e-169">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="4cf9e-169">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


