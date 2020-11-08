---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217416"
---
# <span data-ttu-id="cbdaa-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="cbdaa-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="cbdaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbdaa-102">SYNOPSIS</span></span>
<span data-ttu-id="cbdaa-103">지정 된 앞면 도어에 대 한 새 규칙 엔진 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cbdaa-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="cbdaa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cbdaa-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cbdaa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cbdaa-105">DESCRIPTION</span></span>
<span data-ttu-id="cbdaa-106">지정 된 앞면 도어에 대 한 새 규칙 엔진 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cbdaa-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="cbdaa-107">Cmdlet "New-AzFrontDoorRulesEngineRule"를 사용 하 여이 cmdlet의 "-Rules" 매개 변수에 전달 하는 규칙 엔진 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cbdaa-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="cbdaa-108">예제의</span><span class="sxs-lookup"><span data-stu-id="cbdaa-108">EXAMPLES</span></span>

### <span data-ttu-id="cbdaa-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="cbdaa-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="cbdaa-110">지정 된 앞면 도어에 대 한 새 규칙 엔진 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cbdaa-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="cbdaa-111">변수</span><span class="sxs-lookup"><span data-stu-id="cbdaa-111">PARAMETERS</span></span>

### <span data-ttu-id="cbdaa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbdaa-112">-DefaultProfile</span></span>
<span data-ttu-id="cbdaa-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cbdaa-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbdaa-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="cbdaa-114">-FrontDoorName</span></span>
<span data-ttu-id="cbdaa-115">전방 문 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cbdaa-115">Front Door name.</span></span>

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

### <span data-ttu-id="cbdaa-116">-이름</span><span class="sxs-lookup"><span data-stu-id="cbdaa-116">-Name</span></span>
<span data-ttu-id="cbdaa-117">규칙 엔진 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cbdaa-117">Rules engine name.</span></span>

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

### <span data-ttu-id="cbdaa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbdaa-118">-ResourceGroupName</span></span>
<span data-ttu-id="cbdaa-119">앞 문이 생성 될 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cbdaa-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="cbdaa-120">-규칙</span><span class="sxs-lookup"><span data-stu-id="cbdaa-120">-Rule</span></span>
<span data-ttu-id="cbdaa-121">특정 규칙 엔진 구성을 정의 하는 규칙 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="cbdaa-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="cbdaa-122">-확인</span><span class="sxs-lookup"><span data-stu-id="cbdaa-122">-Confirm</span></span>
<span data-ttu-id="cbdaa-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdaa-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbdaa-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbdaa-124">-WhatIf</span></span>
<span data-ttu-id="cbdaa-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cbdaa-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbdaa-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbdaa-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbdaa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdaa-127">CommonParameters</span></span>
<span data-ttu-id="cbdaa-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbdaa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdaa-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cbdaa-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdaa-130">입력</span><span class="sxs-lookup"><span data-stu-id="cbdaa-130">INPUTS</span></span>

### <span data-ttu-id="cbdaa-131">않아야</span><span class="sxs-lookup"><span data-stu-id="cbdaa-131">None</span></span>

## <span data-ttu-id="cbdaa-132">출력</span><span class="sxs-lookup"><span data-stu-id="cbdaa-132">OUTPUTS</span></span>

### <span data-ttu-id="cbdaa-133">FrontDoor. a m/. Ps규칙 엔진</span><span class="sxs-lookup"><span data-stu-id="cbdaa-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="cbdaa-134">상속자</span><span class="sxs-lookup"><span data-stu-id="cbdaa-134">NOTES</span></span>

## <span data-ttu-id="cbdaa-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbdaa-135">RELATED LINKS</span></span>
