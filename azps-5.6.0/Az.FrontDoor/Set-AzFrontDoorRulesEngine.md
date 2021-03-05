---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/set-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 7f24d7a7fc027e8d4411b12a3f04d24121af5354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969136"
---
# <span data-ttu-id="a2f0d-101">Set-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="a2f0d-101">Set-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="a2f0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="a2f0d-103">규칙 엔진을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-103">Update a Rules Engine.</span></span>

## <span data-ttu-id="a2f0d-104">구문</span><span class="sxs-lookup"><span data-stu-id="a2f0d-104">SYNTAX</span></span>

### <span data-ttu-id="a2f0d-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a2f0d-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2f0d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2f0d-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2f0d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2f0d-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceId <String> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2f0d-108">설명</span><span class="sxs-lookup"><span data-stu-id="a2f0d-108">DESCRIPTION</span></span>
<span data-ttu-id="a2f0d-109">규칙 엔진을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-109">Update a Rules Engine.</span></span>

## <span data-ttu-id="a2f0d-110">예제</span><span class="sxs-lookup"><span data-stu-id="a2f0d-110">EXAMPLES</span></span>

### <span data-ttu-id="a2f0d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a2f0d-111">Example 1</span></span>
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

<span data-ttu-id="a2f0d-112">기존 규칙 엔진 구성을 얻고 다른 규칙 엔진 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-112">Get an existing rules engine configuration and add another rules engine rule to it.</span></span>

## <span data-ttu-id="a2f0d-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a2f0d-113">PARAMETERS</span></span>

### <span data-ttu-id="a2f0d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2f0d-114">-DefaultProfile</span></span>
<span data-ttu-id="a2f0d-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2f0d-116">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="a2f0d-116">-FrontDoorName</span></span>
<span data-ttu-id="a2f0d-117">프런트 도어 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-117">Front Door name.</span></span>

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

### <span data-ttu-id="a2f0d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2f0d-118">-InputObject</span></span>
<span data-ttu-id="a2f0d-119">업데이트할 규칙 엔진 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-119">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="a2f0d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a2f0d-120">-Name</span></span>
<span data-ttu-id="a2f0d-121">규칙 엔진 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-121">Rules engine name.</span></span>

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

### <span data-ttu-id="a2f0d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2f0d-122">-ResourceGroupName</span></span>
<span data-ttu-id="a2f0d-123">Front Door에서 만들 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-123">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="a2f0d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2f0d-124">-ResourceId</span></span>
<span data-ttu-id="a2f0d-125">업데이트할 RulesEngine의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="a2f0d-125">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="a2f0d-126">-Rule</span><span class="sxs-lookup"><span data-stu-id="a2f0d-126">-Rule</span></span>
<span data-ttu-id="a2f0d-127">특정 규칙 엔진 구성을 정의하는 규칙 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-127">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="a2f0d-128">-확인</span><span class="sxs-lookup"><span data-stu-id="a2f0d-128">-Confirm</span></span>
<span data-ttu-id="a2f0d-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2f0d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2f0d-130">-WhatIf</span></span>
<span data-ttu-id="a2f0d-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2f0d-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2f0d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2f0d-133">CommonParameters</span></span>
<span data-ttu-id="a2f0d-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a2f0d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2f0d-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2f0d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2f0d-136">입력</span><span class="sxs-lookup"><span data-stu-id="a2f0d-136">INPUTS</span></span>

### <span data-ttu-id="a2f0d-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="a2f0d-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="a2f0d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a2f0d-138">System.String</span></span>

## <span data-ttu-id="a2f0d-139">출력</span><span class="sxs-lookup"><span data-stu-id="a2f0d-139">OUTPUTS</span></span>

### <span data-ttu-id="a2f0d-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="a2f0d-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="a2f0d-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a2f0d-141">NOTES</span></span>

## <span data-ttu-id="a2f0d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2f0d-142">RELATED LINKS</span></span>
