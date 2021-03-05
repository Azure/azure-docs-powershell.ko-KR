---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 7356f6f0235f73207582303b46459d28dffbe6fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964880"
---
# <span data-ttu-id="8e1f7-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8e1f7-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="8e1f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e1f7-102">SYNOPSIS</span></span>
<span data-ttu-id="8e1f7-103">데이터 팩터리에서 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="8e1f7-104">구문</span><span class="sxs-lookup"><span data-stu-id="8e1f7-104">SYNTAX</span></span>

### <span data-ttu-id="8e1f7-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="8e1f7-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e1f7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8e1f7-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e1f7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e1f7-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e1f7-108">설명</span><span class="sxs-lookup"><span data-stu-id="8e1f7-108">DESCRIPTION</span></span>
<span data-ttu-id="8e1f7-109">**Stop-AzDataFactoryV2Trigger** cmdlet은 데이터 팩터리에서 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="8e1f7-110">트리거가 '시작' 상태인 경우 cmdlet은 트리거를 중지하고 더 이상 파이프라인을 호출하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="8e1f7-111">트리거가 이미 '중지됨' 상태인 경우 이 cmdlet은 영향을주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="8e1f7-112">Force 매개 변수를 지정하면 트리거를 중지하기 전에 cmdlet에 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="8e1f7-113">예제</span><span class="sxs-lookup"><span data-stu-id="8e1f7-113">EXAMPLES</span></span>

### <span data-ttu-id="8e1f7-114">예제 1: 트리거 중지</span><span class="sxs-lookup"><span data-stu-id="8e1f7-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="8e1f7-115">데이터 팩터리 "WikiADF"에서 "ScheduledTrigger"라는 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="8e1f7-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8e1f7-116">PARAMETERS</span></span>

### <span data-ttu-id="8e1f7-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8e1f7-117">-DataFactoryName</span></span>
<span data-ttu-id="8e1f7-118">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-118">The data factory name.</span></span>

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

### <span data-ttu-id="8e1f7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e1f7-119">-DefaultProfile</span></span>
<span data-ttu-id="8e1f7-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e1f7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8e1f7-121">-Force</span></span>
<span data-ttu-id="8e1f7-122">확인을 요청하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="8e1f7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e1f7-123">-InputObject</span></span>
<span data-ttu-id="8e1f7-124">시작할 개체를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="8e1f7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8e1f7-125">-Name</span></span>
<span data-ttu-id="8e1f7-126">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-126">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e1f7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e1f7-127">-ResourceGroupName</span></span>
<span data-ttu-id="8e1f7-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-128">The resource group name.</span></span>

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

### <span data-ttu-id="8e1f7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e1f7-129">-ResourceId</span></span>
<span data-ttu-id="8e1f7-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8e1f7-131">-확인</span><span class="sxs-lookup"><span data-stu-id="8e1f7-131">-Confirm</span></span>
<span data-ttu-id="8e1f7-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e1f7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e1f7-133">-WhatIf</span></span>
<span data-ttu-id="8e1f7-134">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="8e1f7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e1f7-135">CommonParameters</span></span>
<span data-ttu-id="8e1f7-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e1f7-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8e1f7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e1f7-138">입력</span><span class="sxs-lookup"><span data-stu-id="8e1f7-138">INPUTS</span></span>

### <span data-ttu-id="8e1f7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8e1f7-139">System.String</span></span>

### <span data-ttu-id="8e1f7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="8e1f7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="8e1f7-141">출력</span><span class="sxs-lookup"><span data-stu-id="8e1f7-141">OUTPUTS</span></span>

### <span data-ttu-id="8e1f7-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="8e1f7-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="8e1f7-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8e1f7-143">NOTES</span></span>

## <span data-ttu-id="8e1f7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e1f7-144">RELATED LINKS</span></span>

[<span data-ttu-id="8e1f7-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8e1f7-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8e1f7-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8e1f7-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8e1f7-147">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8e1f7-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8e1f7-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8e1f7-148">Remove-AzDataFactoryV2Trigger</span></span>]()
