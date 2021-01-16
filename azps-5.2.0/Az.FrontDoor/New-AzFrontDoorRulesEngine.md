---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348873"
---
# <span data-ttu-id="2660c-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="2660c-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="2660c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2660c-102">SYNOPSIS</span></span>
<span data-ttu-id="2660c-103">지정된 Front Door에 대한 새 규칙 엔진 구성을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="2660c-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="2660c-104">구문</span><span class="sxs-lookup"><span data-stu-id="2660c-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2660c-105">설명</span><span class="sxs-lookup"><span data-stu-id="2660c-105">DESCRIPTION</span></span>
<span data-ttu-id="2660c-106">지정된 Front Door에 대한 새 규칙 엔진 구성을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="2660c-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="2660c-107">cmdlet "New-AzFrontDoorRulesEngineRule"을 사용하여 이 cmdlet의 "-Rules" 매개 변수에 전달하는 규칙 엔진 규칙을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2660c-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="2660c-108">예제</span><span class="sxs-lookup"><span data-stu-id="2660c-108">EXAMPLES</span></span>

### <span data-ttu-id="2660c-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="2660c-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="2660c-110">지정된 Front Door에 대한 새 규칙 엔진 구성을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="2660c-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="2660c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2660c-111">PARAMETERS</span></span>

### <span data-ttu-id="2660c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2660c-112">-DefaultProfile</span></span>
<span data-ttu-id="2660c-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2660c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2660c-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="2660c-114">-FrontDoorName</span></span>
<span data-ttu-id="2660c-115">Front Door 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2660c-115">Front Door name.</span></span>

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

### <span data-ttu-id="2660c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2660c-116">-Name</span></span>
<span data-ttu-id="2660c-117">규칙 엔진 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2660c-117">Rules engine name.</span></span>

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

### <span data-ttu-id="2660c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2660c-118">-ResourceGroupName</span></span>
<span data-ttu-id="2660c-119">Front Door를 만들 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2660c-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="2660c-120">-Rule</span><span class="sxs-lookup"><span data-stu-id="2660c-120">-Rule</span></span>
<span data-ttu-id="2660c-121">특정 규칙 엔진 구성을 정의하는 규칙 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2660c-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

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

### <span data-ttu-id="2660c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2660c-122">-Confirm</span></span>
<span data-ttu-id="2660c-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2660c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2660c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2660c-124">-WhatIf</span></span>
<span data-ttu-id="2660c-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2660c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2660c-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2660c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2660c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2660c-127">CommonParameters</span></span>
<span data-ttu-id="2660c-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2660c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2660c-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2660c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2660c-130">입력</span><span class="sxs-lookup"><span data-stu-id="2660c-130">INPUTS</span></span>

### <span data-ttu-id="2660c-131">없음</span><span class="sxs-lookup"><span data-stu-id="2660c-131">None</span></span>

## <span data-ttu-id="2660c-132">출력</span><span class="sxs-lookup"><span data-stu-id="2660c-132">OUTPUTS</span></span>

### <span data-ttu-id="2660c-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="2660c-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="2660c-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2660c-134">NOTES</span></span>

## <span data-ttu-id="2660c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2660c-135">RELATED LINKS</span></span>
