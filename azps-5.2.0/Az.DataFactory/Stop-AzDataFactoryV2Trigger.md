---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 80e9ed345b9d1b80dd75be2036826559ac3bbb9a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358324"
---
# <span data-ttu-id="48a36-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="48a36-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="48a36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48a36-102">SYNOPSIS</span></span>
<span data-ttu-id="48a36-103">데이터 팩터리에서 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="48a36-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="48a36-104">구문</span><span class="sxs-lookup"><span data-stu-id="48a36-104">SYNTAX</span></span>

### <span data-ttu-id="48a36-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="48a36-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48a36-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="48a36-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48a36-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="48a36-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48a36-108">설명</span><span class="sxs-lookup"><span data-stu-id="48a36-108">DESCRIPTION</span></span>
<span data-ttu-id="48a36-109">**Stop-AzDataFactoryV2Trigger** cmdlet은 데이터 팩터리에서 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="48a36-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="48a36-110">트리거가 '시작' 상태이면 cmdlet은 트리거를 중지하고 더 이상 파이프라인을 호출하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="48a36-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="48a36-111">트리거가 이미 '중지됨' 상태인 경우 이 cmdlet은 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="48a36-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="48a36-112">Force 매개 변수를 지정하면 트리거를 중지하기 전에 cmdlet이 프롬프트를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="48a36-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="48a36-113">예제</span><span class="sxs-lookup"><span data-stu-id="48a36-113">EXAMPLES</span></span>

### <span data-ttu-id="48a36-114">예제 1: 트리거 중지</span><span class="sxs-lookup"><span data-stu-id="48a36-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="48a36-115">데이터 팩터리 "WikiADF"에서 "ScheduledTrigger"라는 트리거를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="48a36-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="48a36-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48a36-116">PARAMETERS</span></span>

### <span data-ttu-id="48a36-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="48a36-117">-DataFactoryName</span></span>
<span data-ttu-id="48a36-118">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48a36-118">The data factory name.</span></span>

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

### <span data-ttu-id="48a36-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48a36-119">-DefaultProfile</span></span>
<span data-ttu-id="48a36-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="48a36-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48a36-121">-Force</span><span class="sxs-lookup"><span data-stu-id="48a36-121">-Force</span></span>
<span data-ttu-id="48a36-122">확인 메시지를 표시하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="48a36-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="48a36-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48a36-123">-InputObject</span></span>
<span data-ttu-id="48a36-124">시작할 개체를 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="48a36-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="48a36-125">-Name</span><span class="sxs-lookup"><span data-stu-id="48a36-125">-Name</span></span>
<span data-ttu-id="48a36-126">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48a36-126">The trigger name.</span></span>

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

### <span data-ttu-id="48a36-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48a36-127">-ResourceGroupName</span></span>
<span data-ttu-id="48a36-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48a36-128">The resource group name.</span></span>

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

### <span data-ttu-id="48a36-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48a36-129">-ResourceId</span></span>
<span data-ttu-id="48a36-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="48a36-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="48a36-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48a36-131">-Confirm</span></span>
<span data-ttu-id="48a36-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="48a36-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48a36-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48a36-133">-WhatIf</span></span>
<span data-ttu-id="48a36-134">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="48a36-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="48a36-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48a36-135">CommonParameters</span></span>
<span data-ttu-id="48a36-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="48a36-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48a36-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="48a36-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48a36-138">입력</span><span class="sxs-lookup"><span data-stu-id="48a36-138">INPUTS</span></span>

### <span data-ttu-id="48a36-139">System.String</span><span class="sxs-lookup"><span data-stu-id="48a36-139">System.String</span></span>

### <span data-ttu-id="48a36-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="48a36-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="48a36-141">출력</span><span class="sxs-lookup"><span data-stu-id="48a36-141">OUTPUTS</span></span>

### <span data-ttu-id="48a36-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="48a36-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="48a36-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="48a36-143">NOTES</span></span>

## <span data-ttu-id="48a36-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48a36-144">RELATED LINKS</span></span>

[<span data-ttu-id="48a36-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="48a36-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="48a36-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="48a36-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="48a36-147">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="48a36-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="48a36-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="48a36-148">Remove-AzDataFactoryV2Trigger</span></span>]()