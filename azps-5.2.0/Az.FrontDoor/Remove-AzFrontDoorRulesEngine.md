---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: e0df270a2cfc409025434a4e9ca64a2234e6e7c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371372"
---
# <span data-ttu-id="4e681-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="4e681-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="4e681-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e681-102">SYNOPSIS</span></span>
<span data-ttu-id="4e681-103">Front Door에서 규칙 엔진 제거</span><span class="sxs-lookup"><span data-stu-id="4e681-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="4e681-104">구문</span><span class="sxs-lookup"><span data-stu-id="4e681-104">SYNTAX</span></span>

### <span data-ttu-id="4e681-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4e681-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e681-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e681-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e681-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e681-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e681-108">설명</span><span class="sxs-lookup"><span data-stu-id="4e681-108">DESCRIPTION</span></span>
<span data-ttu-id="4e681-109">Front Door에서 규칙 엔진 제거</span><span class="sxs-lookup"><span data-stu-id="4e681-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="4e681-110">예제</span><span class="sxs-lookup"><span data-stu-id="4e681-110">EXAMPLES</span></span>

### <span data-ttu-id="4e681-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4e681-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="4e681-112">규칙 엔진 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4e681-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="4e681-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="4e681-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="4e681-114">없는 규칙 엔진 구성을 제거할 때 예상되는 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="4e681-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="4e681-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e681-115">PARAMETERS</span></span>

### <span data-ttu-id="4e681-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e681-116">-DefaultProfile</span></span>
<span data-ttu-id="4e681-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4e681-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e681-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="4e681-118">-FrontDoorName</span></span>
<span data-ttu-id="4e681-119">Front Door 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e681-119">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e681-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e681-120">-InputObject</span></span>
<span data-ttu-id="4e681-121">업데이트할 규칙 엔진 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4e681-121">The Rules Engine object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e681-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4e681-122">-Name</span></span>
<span data-ttu-id="4e681-123">규칙 엔진 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e681-123">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e681-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e681-124">-PassThru</span></span>
<span data-ttu-id="4e681-125">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="4e681-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="4e681-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e681-126">-ResourceGroupName</span></span>
<span data-ttu-id="4e681-127">Front Door를 만들 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e681-127">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e681-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e681-128">-ResourceId</span></span>
<span data-ttu-id="4e681-129">업데이트할 RulesEngine의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="4e681-129">Resource Id of the RulesEngine to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e681-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e681-130">-Confirm</span></span>
<span data-ttu-id="4e681-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e681-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e681-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e681-132">-WhatIf</span></span>
<span data-ttu-id="4e681-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4e681-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e681-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e681-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e681-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e681-135">CommonParameters</span></span>
<span data-ttu-id="4e681-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4e681-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e681-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4e681-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e681-138">입력</span><span class="sxs-lookup"><span data-stu-id="4e681-138">INPUTS</span></span>

### <span data-ttu-id="4e681-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="4e681-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="4e681-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4e681-140">System.String</span></span>

## <span data-ttu-id="4e681-141">출력</span><span class="sxs-lookup"><span data-stu-id="4e681-141">OUTPUTS</span></span>

### <span data-ttu-id="4e681-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4e681-142">System.Boolean</span></span>

## <span data-ttu-id="4e681-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4e681-143">NOTES</span></span>

## <span data-ttu-id="4e681-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e681-144">RELATED LINKS</span></span>
