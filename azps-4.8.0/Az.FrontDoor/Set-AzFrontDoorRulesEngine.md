---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoorRulesEngine.md
ms.openlocfilehash: cf98121f535f60c7d1ddc3b29e33f10fd8f29842
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214941"
---
# <span data-ttu-id="1143b-101">Set-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="1143b-101">Set-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="1143b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1143b-102">SYNOPSIS</span></span>
<span data-ttu-id="1143b-103">규칙 엔진을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1143b-103">Update a Rules Engine.</span></span>

## <span data-ttu-id="1143b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1143b-104">SYNTAX</span></span>

### <span data-ttu-id="1143b-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1143b-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1143b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1143b-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1143b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1143b-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoorRulesEngine -ResourceId <String> [-Rule <PSRulesEngineRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1143b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1143b-108">DESCRIPTION</span></span>
<span data-ttu-id="1143b-109">규칙 엔진을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1143b-109">Update a Rules Engine.</span></span>

## <span data-ttu-id="1143b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1143b-110">EXAMPLES</span></span>

### <span data-ttu-id="1143b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1143b-111">Example 1</span></span>
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

<span data-ttu-id="1143b-112">기존 규칙 엔진 구성을 가져오고 다른 규칙 엔진 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1143b-112">Get an existing rules engine configuration and add another rules engine rule to it.</span></span>

## <span data-ttu-id="1143b-113">변수</span><span class="sxs-lookup"><span data-stu-id="1143b-113">PARAMETERS</span></span>

### <span data-ttu-id="1143b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1143b-114">-DefaultProfile</span></span>
<span data-ttu-id="1143b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1143b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1143b-116">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="1143b-116">-FrontDoorName</span></span>
<span data-ttu-id="1143b-117">전방 문 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1143b-117">Front Door name.</span></span>

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

### <span data-ttu-id="1143b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1143b-118">-InputObject</span></span>
<span data-ttu-id="1143b-119">업데이트할 규칙 엔진 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1143b-119">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="1143b-120">-이름</span><span class="sxs-lookup"><span data-stu-id="1143b-120">-Name</span></span>
<span data-ttu-id="1143b-121">규칙 엔진 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1143b-121">Rules engine name.</span></span>

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

### <span data-ttu-id="1143b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1143b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1143b-123">앞 문이 생성 될 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1143b-123">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="1143b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1143b-124">-ResourceId</span></span>
<span data-ttu-id="1143b-125">업데이트할 규칙 엔진의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1143b-125">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="1143b-126">-규칙</span><span class="sxs-lookup"><span data-stu-id="1143b-126">-Rule</span></span>
<span data-ttu-id="1143b-127">특정 규칙 엔진 구성을 정의 하는 규칙 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1143b-127">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="1143b-128">-확인</span><span class="sxs-lookup"><span data-stu-id="1143b-128">-Confirm</span></span>
<span data-ttu-id="1143b-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1143b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1143b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1143b-130">-WhatIf</span></span>
<span data-ttu-id="1143b-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1143b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1143b-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1143b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1143b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1143b-133">CommonParameters</span></span>
<span data-ttu-id="1143b-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1143b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1143b-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1143b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1143b-136">입력</span><span class="sxs-lookup"><span data-stu-id="1143b-136">INPUTS</span></span>

### <span data-ttu-id="1143b-137">FrontDoor. a m/. Ps규칙 엔진</span><span class="sxs-lookup"><span data-stu-id="1143b-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="1143b-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1143b-138">System.String</span></span>

## <span data-ttu-id="1143b-139">출력</span><span class="sxs-lookup"><span data-stu-id="1143b-139">OUTPUTS</span></span>

### <span data-ttu-id="1143b-140">FrontDoor. a m/. Ps규칙 엔진</span><span class="sxs-lookup"><span data-stu-id="1143b-140">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="1143b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="1143b-141">NOTES</span></span>

## <span data-ttu-id="1143b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1143b-142">RELATED LINKS</span></span>
