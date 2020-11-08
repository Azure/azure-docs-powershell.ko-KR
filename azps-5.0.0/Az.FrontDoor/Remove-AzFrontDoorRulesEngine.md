---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: e0df270a2cfc409025434a4e9ca64a2234e6e7c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215440"
---
# <span data-ttu-id="9fbba-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="9fbba-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="9fbba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fbba-102">SYNOPSIS</span></span>
<span data-ttu-id="9fbba-103">전방 도어에서 규칙 엔진 제거</span><span class="sxs-lookup"><span data-stu-id="9fbba-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="9fbba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9fbba-104">SYNTAX</span></span>

### <span data-ttu-id="9fbba-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9fbba-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fbba-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fbba-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fbba-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fbba-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fbba-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9fbba-108">DESCRIPTION</span></span>
<span data-ttu-id="9fbba-109">전방 도어에서 규칙 엔진 제거</span><span class="sxs-lookup"><span data-stu-id="9fbba-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="9fbba-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9fbba-110">EXAMPLES</span></span>

### <span data-ttu-id="9fbba-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9fbba-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="9fbba-112">규칙 엔진 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbba-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="9fbba-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="9fbba-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="9fbba-114">존재 하지 않는 규칙 엔진 구성을 제거할 때 예상 되는 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="9fbba-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="9fbba-115">변수</span><span class="sxs-lookup"><span data-stu-id="9fbba-115">PARAMETERS</span></span>

### <span data-ttu-id="9fbba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fbba-116">-DefaultProfile</span></span>
<span data-ttu-id="9fbba-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9fbba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fbba-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="9fbba-118">-FrontDoorName</span></span>
<span data-ttu-id="9fbba-119">전방 문 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9fbba-119">Front Door name.</span></span>

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

### <span data-ttu-id="9fbba-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fbba-120">-InputObject</span></span>
<span data-ttu-id="9fbba-121">업데이트할 규칙 엔진 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9fbba-121">The Rules Engine object to update.</span></span>

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

### <span data-ttu-id="9fbba-122">-이름</span><span class="sxs-lookup"><span data-stu-id="9fbba-122">-Name</span></span>
<span data-ttu-id="9fbba-123">규칙 엔진 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9fbba-123">Rules engine name.</span></span>

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

### <span data-ttu-id="9fbba-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9fbba-124">-PassThru</span></span>
<span data-ttu-id="9fbba-125">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbba-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="9fbba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fbba-126">-ResourceGroupName</span></span>
<span data-ttu-id="9fbba-127">앞 문이 생성 될 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9fbba-127">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="9fbba-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fbba-128">-ResourceId</span></span>
<span data-ttu-id="9fbba-129">업데이트할 규칙 엔진의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="9fbba-129">Resource Id of the RulesEngine to update</span></span>

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

### <span data-ttu-id="9fbba-130">-확인</span><span class="sxs-lookup"><span data-stu-id="9fbba-130">-Confirm</span></span>
<span data-ttu-id="9fbba-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbba-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fbba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fbba-132">-WhatIf</span></span>
<span data-ttu-id="9fbba-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9fbba-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fbba-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9fbba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fbba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fbba-135">CommonParameters</span></span>
<span data-ttu-id="9fbba-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fbba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fbba-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9fbba-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fbba-138">입력</span><span class="sxs-lookup"><span data-stu-id="9fbba-138">INPUTS</span></span>

### <span data-ttu-id="9fbba-139">FrontDoor. a m/. Ps규칙 엔진</span><span class="sxs-lookup"><span data-stu-id="9fbba-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="9fbba-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9fbba-140">System.String</span></span>

## <span data-ttu-id="9fbba-141">출력</span><span class="sxs-lookup"><span data-stu-id="9fbba-141">OUTPUTS</span></span>

### <span data-ttu-id="9fbba-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9fbba-142">System.Boolean</span></span>

## <span data-ttu-id="9fbba-143">상속자</span><span class="sxs-lookup"><span data-stu-id="9fbba-143">NOTES</span></span>

## <span data-ttu-id="9fbba-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9fbba-144">RELATED LINKS</span></span>
