---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
ms.openlocfilehash: cf98121f535f60c7d1ddc3b29e33f10fd8f29842
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209456"
---
# <span data-ttu-id="3d1bb-101">Set-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="3d1bb-101">Set-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="3d1bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d1bb-102">SYNOPSIS</span></span>
<span data-ttu-id="3d1bb-103">규칙 엔진을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1bb-103">Update a Rules Engine.</span></span>

## <span data-ttu-id="3d1bb-104">구문</span><span class="sxs-lookup"><span data-stu-id="3d1bb-104">SYNTAX</span></span>

### <span data-ttu-id="3d1bb-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3d1bb-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d1bb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d1bb-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d1bb-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d1bb-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceId <String> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d1bb-108">설명</span><span class="sxs-lookup"><span data-stu-id="3d1bb-108">DESCRIPTION</span></span>
<span data-ttu-id="3d1bb-109">규칙 엔진을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1bb-109">Update a Rules Engine.</span></span>

## <span data-ttu-id="3d1bb-110">예제</span><span class="sxs-lookup"><span data-stu-id="3d1bb-110">EXAMPLES</span></span>

### <span data-ttu-id="3d1bb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3d1bb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}

PS C:\> $rulesEngineRule2 = New-AzFrontDoorRulesEngineRuleObject -Name rules2 -Priority 3 -Action $rulesEngineAction
PS C:\AFD\azure-powershell\artifacts\Debug\Az.FrontDoor> Set-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1, $rulesEngineRule2

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1, rules2}
```

<span data-ttu-id="3d1bb-112">기존 규칙 엔진 구성을 얻고 여기에 다른 규칙 엔진 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1bb-112">Get an existing rules engine configuration and add another rules engine rule to it.</span></span>

## <span data-ttu-id="3d1bb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d1bb-113">PARAMETERS</span></span>

### <span data-ttu-id="3d1bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d1bb-114">-DefaultProfile</span></span>
<span data-ttu-id="3d1bb-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d1bb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d1bb-116">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="3d1bb-116">-FrontDoorName</span></span>
<span data-ttu-id="3d1bb-117">Front Door 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d1bb-117">Front Door name.</span></span>

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

### <span data-ttu-id="3d1bb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d1bb-118">-InputObject</span></span>
<span data-ttu-id="3d1bb-119">업데이트할 규칙 엔진 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3d1bb-119">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="3d1bb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3d1bb-120">-Name</span></span>
<span data-ttu-id="3d1bb-121">규칙 엔진 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d1bb-121">Rules engine name.</span></span>

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

### <span data-ttu-id="3d1bb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d1bb-122">-ResourceGroupName</span></span>
<span data-ttu-id="3d1bb-123">Front Door를 만들 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d1bb-123">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="3d1bb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d1bb-124">-ResourceId</span></span>
<span data-ttu-id="3d1bb-125">업데이트할 RulesEngine의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="3d1bb-125">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="3d1bb-126">-Rule</span><span class="sxs-lookup"><span data-stu-id="3d1bb-126">-Rule</span></span>
<span data-ttu-id="3d1bb-127">특정 규칙 엔진 구성을 정의하는 규칙 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3d1bb-127">A list of rules that define a particular Rules Engine Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d1bb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d1bb-128">-Confirm</span></span>
<span data-ttu-id="3d1bb-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d1bb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d1bb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d1bb-130">-WhatIf</span></span>
<span data-ttu-id="3d1bb-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3d1bb-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d1bb-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d1bb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d1bb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d1bb-133">CommonParameters</span></span>
<span data-ttu-id="3d1bb-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3d1bb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d1bb-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d1bb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d1bb-136">입력</span><span class="sxs-lookup"><span data-stu-id="3d1bb-136">INPUTS</span></span>

### <span data-ttu-id="3d1bb-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="3d1bb-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="3d1bb-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3d1bb-138">System.String</span></span>

## <span data-ttu-id="3d1bb-139">출력</span><span class="sxs-lookup"><span data-stu-id="3d1bb-139">OUTPUTS</span></span>

### <span data-ttu-id="3d1bb-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="3d1bb-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="3d1bb-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3d1bb-141">NOTES</span></span>

## <span data-ttu-id="3d1bb-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d1bb-142">RELATED LINKS</span></span>
