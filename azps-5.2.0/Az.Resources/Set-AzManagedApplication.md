---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: 3d8445c78ae2f11fef734db0b24319b524f55704
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351758"
---
# <span data-ttu-id="8811c-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="8811c-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="8811c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8811c-102">SYNOPSIS</span></span>
<span data-ttu-id="8811c-103">관리되는 애플리케이션 업데이트</span><span class="sxs-lookup"><span data-stu-id="8811c-103">Updates managed application</span></span>

## <span data-ttu-id="8811c-104">구문</span><span class="sxs-lookup"><span data-stu-id="8811c-104">SYNTAX</span></span>

### <span data-ttu-id="8811c-105">SetByNameAndResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="8811c-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8811c-106">SetById</span><span class="sxs-lookup"><span data-stu-id="8811c-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8811c-107">설명</span><span class="sxs-lookup"><span data-stu-id="8811c-107">DESCRIPTION</span></span>
<span data-ttu-id="8811c-108">**Set-AzManagedApplication** cmdlet은 관리되는 애플리케이션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="8811c-109">예제</span><span class="sxs-lookup"><span data-stu-id="8811c-109">EXAMPLES</span></span>

### <span data-ttu-id="8811c-110">예제 1: 관리되는 애플리케이션 정의 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="8811c-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="8811c-111">이 명령은 관리되는 애플리케이션 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-111">This command updates the managed application description</span></span>

## <span data-ttu-id="8811c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8811c-112">PARAMETERS</span></span>

### <span data-ttu-id="8811c-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8811c-113">-ApiVersion</span></span>
<span data-ttu-id="8811c-114">설정되면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8811c-115">지정하지 않으면 API 버전이 사용 가능한 최신 버전으로 자동으로 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8811c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8811c-116">-DefaultProfile</span></span>
<span data-ttu-id="8811c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8811c-118">-Id</span><span class="sxs-lookup"><span data-stu-id="8811c-118">-Id</span></span>
<span data-ttu-id="8811c-119">구독을 포함하여 정식으로 관리되는 애플리케이션 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="8811c-120">예: /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8811c-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8811c-121">-Kind</span><span class="sxs-lookup"><span data-stu-id="8811c-121">-Kind</span></span>
<span data-ttu-id="8811c-122">관리되는 애플리케이션 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-122">The managed application kind.</span></span>
<span data-ttu-id="8811c-123">마켓플레이스 또는 servicecatalog 중 하나</span><span class="sxs-lookup"><span data-stu-id="8811c-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="8811c-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="8811c-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="8811c-125">관리되는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="8811c-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8811c-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="8811c-127">관리되는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-127">The managed resource group name.</span></span>

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

### <span data-ttu-id="8811c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="8811c-128">-Name</span></span>
<span data-ttu-id="8811c-129">관리되는 애플리케이션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-129">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8811c-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="8811c-130">-Parameter</span></span>
<span data-ttu-id="8811c-131">관리되는 애플리케이션에 대한 JSON 형식의 매개 변수 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="8811c-132">파일 이름에 대한 경로 또는 매개 변수를 포함하는 URI 또는 매개 변수를 문자열로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="8811c-133">-Plan</span><span class="sxs-lookup"><span data-stu-id="8811c-133">-Plan</span></span>
<span data-ttu-id="8811c-134">관리되는 애플리케이션 계획 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-134">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="8811c-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="8811c-135">-Pre</span></span>
<span data-ttu-id="8811c-136">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8811c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8811c-137">-ResourceGroupName</span></span>
<span data-ttu-id="8811c-138">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8811c-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="8811c-139">-Tag</span></span>
<span data-ttu-id="8811c-140">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="8811c-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8811c-141">-Confirm</span></span>
<span data-ttu-id="8811c-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8811c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8811c-143">-WhatIf</span></span>
<span data-ttu-id="8811c-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8811c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8811c-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8811c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8811c-146">CommonParameters</span></span>
<span data-ttu-id="8811c-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8811c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8811c-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8811c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8811c-149">입력</span><span class="sxs-lookup"><span data-stu-id="8811c-149">INPUTS</span></span>

### <span data-ttu-id="8811c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="8811c-150">System.String</span></span>

### <span data-ttu-id="8811c-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8811c-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8811c-152">출력</span><span class="sxs-lookup"><span data-stu-id="8811c-152">OUTPUTS</span></span>

### <span data-ttu-id="8811c-153">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="8811c-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8811c-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8811c-154">NOTES</span></span>

## <span data-ttu-id="8811c-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8811c-155">RELATED LINKS</span></span>
