---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 06ff54b8f5a247f3035d0eda0be5c474f9a9576b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349106"
---
# <span data-ttu-id="5298c-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="5298c-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="5298c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5298c-102">SYNOPSIS</span></span>
<span data-ttu-id="5298c-103">Azure 관리되는 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="5298c-104">구문</span><span class="sxs-lookup"><span data-stu-id="5298c-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5298c-105">설명</span><span class="sxs-lookup"><span data-stu-id="5298c-105">DESCRIPTION</span></span>
<span data-ttu-id="5298c-106">**New-AzManagedApplication** cmdlet은 Azure 관리되는 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="5298c-107">예제</span><span class="sxs-lookup"><span data-stu-id="5298c-107">EXAMPLES</span></span>

### <span data-ttu-id="5298c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5298c-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="5298c-109">이 명령은 관리되는 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-109">This command creates a managed application</span></span>

## <span data-ttu-id="5298c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5298c-110">PARAMETERS</span></span>

### <span data-ttu-id="5298c-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5298c-111">-ApiVersion</span></span>
<span data-ttu-id="5298c-112">설정되면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="5298c-113">지정하지 않으면 API 버전이 사용 가능한 최신 버전으로 자동으로 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="5298c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5298c-114">-DefaultProfile</span></span>
<span data-ttu-id="5298c-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5298c-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="5298c-116">-Kind</span></span>
<span data-ttu-id="5298c-117">관리되는 애플리케이션 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-117">The managed application kind.</span></span>
<span data-ttu-id="5298c-118">마켓플레이스 또는 servicecatalog 중 하나</span><span class="sxs-lookup"><span data-stu-id="5298c-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5298c-119">-Location</span><span class="sxs-lookup"><span data-stu-id="5298c-119">-Location</span></span>
<span data-ttu-id="5298c-120">리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-120">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5298c-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="5298c-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="5298c-122">관리되는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="5298c-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5298c-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="5298c-124">관리되는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-124">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5298c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5298c-125">-Name</span></span>
<span data-ttu-id="5298c-126">관리되는 애플리케이션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5298c-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="5298c-127">-Parameter</span></span>
<span data-ttu-id="5298c-128">관리되는 애플리케이션에 대한 JSON 형식의 매개 변수 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="5298c-129">파일 이름에 대한 경로 또는 매개 변수를 포함하는 URI 또는 매개 변수를 문자열로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="5298c-130">-Plan</span><span class="sxs-lookup"><span data-stu-id="5298c-130">-Plan</span></span>
<span data-ttu-id="5298c-131">관리되는 애플리케이션 계획 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="5298c-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="5298c-132">-Pre</span></span>
<span data-ttu-id="5298c-133">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5298c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5298c-134">-ResourceGroupName</span></span>
<span data-ttu-id="5298c-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5298c-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="5298c-136">-Tag</span></span>
<span data-ttu-id="5298c-137">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="5298c-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5298c-138">-Confirm</span></span>
<span data-ttu-id="5298c-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5298c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5298c-140">-WhatIf</span></span>
<span data-ttu-id="5298c-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5298c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5298c-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5298c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5298c-143">CommonParameters</span></span>
<span data-ttu-id="5298c-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5298c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5298c-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5298c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5298c-146">입력</span><span class="sxs-lookup"><span data-stu-id="5298c-146">INPUTS</span></span>

### <span data-ttu-id="5298c-147">System.String</span><span class="sxs-lookup"><span data-stu-id="5298c-147">System.String</span></span>

### <span data-ttu-id="5298c-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5298c-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5298c-149">출력</span><span class="sxs-lookup"><span data-stu-id="5298c-149">OUTPUTS</span></span>

### <span data-ttu-id="5298c-150">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="5298c-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5298c-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5298c-151">NOTES</span></span>

## <span data-ttu-id="5298c-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5298c-152">RELATED LINKS</span></span>
