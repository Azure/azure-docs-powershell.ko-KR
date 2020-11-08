---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879394"
---
# <span data-ttu-id="fc16f-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fc16f-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="fc16f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc16f-102">SYNOPSIS</span></span>
<span data-ttu-id="fc16f-103">데이터 팩터리에 트리거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc16f-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="fc16f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc16f-104">SYNTAX</span></span>

### <span data-ttu-id="fc16f-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="fc16f-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc16f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fc16f-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc16f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fc16f-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc16f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fc16f-108">DESCRIPTION</span></span>
<span data-ttu-id="fc16f-109">**AzDataFactoryV2Trigger** cmdlet은 데이터 팩터리에 트리거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc16f-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="fc16f-110">_Force_ 매개 변수를 지정 하면 cmdlet은 트리거를 제거 하기 전에 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc16f-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="fc16f-111">예제의</span><span class="sxs-lookup"><span data-stu-id="fc16f-111">EXAMPLES</span></span>

### <span data-ttu-id="fc16f-112">예제 1: 트리거 제거</span><span class="sxs-lookup"><span data-stu-id="fc16f-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="fc16f-113">Data factory "WikiADF"에서 "ScheduledTrigger" 이라는 트리거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc16f-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="fc16f-114">변수</span><span class="sxs-lookup"><span data-stu-id="fc16f-114">PARAMETERS</span></span>

### <span data-ttu-id="fc16f-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fc16f-115">-DataFactoryName</span></span>
<span data-ttu-id="fc16f-116">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc16f-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc16f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc16f-117">-DefaultProfile</span></span>
<span data-ttu-id="fc16f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc16f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc16f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fc16f-119">-Force</span></span>
<span data-ttu-id="fc16f-120">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc16f-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fc16f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc16f-121">-InputObject</span></span>
<span data-ttu-id="fc16f-122">제거할 트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fc16f-122">The Trigger object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc16f-123">-이름</span><span class="sxs-lookup"><span data-stu-id="fc16f-123">-Name</span></span>
<span data-ttu-id="fc16f-124">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc16f-124">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc16f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc16f-125">-ResourceGroupName</span></span>
<span data-ttu-id="fc16f-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc16f-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc16f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc16f-127">-ResourceId</span></span>
<span data-ttu-id="fc16f-128">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fc16f-128">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc16f-129">-확인</span><span class="sxs-lookup"><span data-stu-id="fc16f-129">-Confirm</span></span>
<span data-ttu-id="fc16f-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc16f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc16f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc16f-131">-WhatIf</span></span>
<span data-ttu-id="fc16f-132">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc16f-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="fc16f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc16f-133">CommonParameters</span></span>
<span data-ttu-id="fc16f-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc16f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc16f-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc16f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc16f-136">입력</span><span class="sxs-lookup"><span data-stu-id="fc16f-136">INPUTS</span></span>

### <span data-ttu-id="fc16f-137">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="fc16f-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="fc16f-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fc16f-138">System.String</span></span>

## <span data-ttu-id="fc16f-139">출력</span><span class="sxs-lookup"><span data-stu-id="fc16f-139">OUTPUTS</span></span>

### <span data-ttu-id="fc16f-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="fc16f-140">System.Boolean</span></span>

## <span data-ttu-id="fc16f-141">상속자</span><span class="sxs-lookup"><span data-stu-id="fc16f-141">NOTES</span></span>

## <span data-ttu-id="fc16f-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc16f-142">RELATED LINKS</span></span>

[<span data-ttu-id="fc16f-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fc16f-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="fc16f-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fc16f-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="fc16f-145">시작-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fc16f-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="fc16f-146">중지-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fc16f-146">Stop-AzDataFactoryV2Trigger</span></span>]()
