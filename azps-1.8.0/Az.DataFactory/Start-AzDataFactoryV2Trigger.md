---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 988f63d9f894de95c4206dc05bcda66e68f3c4ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701110"
---
# <span data-ttu-id="635c6-101">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="635c6-101">Start-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="635c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="635c6-102">SYNOPSIS</span></span>
<span data-ttu-id="635c6-103">데이터 팩터리에 트리거를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="635c6-103">Starts a trigger in a data factory.</span></span>

## <span data-ttu-id="635c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="635c6-104">SYNTAX</span></span>

### <span data-ttu-id="635c6-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="635c6-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="635c6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="635c6-106">ByInputObject</span></span>
```
Start-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="635c6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="635c6-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="635c6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="635c6-108">DESCRIPTION</span></span>
<span data-ttu-id="635c6-109">**AzDataFactoryV2Trigger** cmdlet은 데이터 팩터리에 트리거를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="635c6-109">The **Start-AzDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="635c6-110">트리거가 ' 중지 됨 ' 상태인 경우 cmdlet은 트리거를 시작 하 고 결과적으로 해당 정의에 따라 파이프라인을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="635c6-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="635c6-111">트리거가 이미 ' 시작 됨 ' 상태에 있는 경우에는이 cmdlet이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="635c6-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="635c6-112">Force 매개 변수를 지정 하면 cmdlet이 트리거를 시작 하기 전에 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="635c6-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="635c6-113">예제의</span><span class="sxs-lookup"><span data-stu-id="635c6-113">EXAMPLES</span></span>

### <span data-ttu-id="635c6-114">예제 1: 트리거 시작</span><span class="sxs-lookup"><span data-stu-id="635c6-114">Example 1: Start a trigger</span></span>
```
Start-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="635c6-115">Data factory "WikiADF"에서 "ScheduledTrigger" 이라는 트리거를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="635c6-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="635c6-116">변수</span><span class="sxs-lookup"><span data-stu-id="635c6-116">PARAMETERS</span></span>

### <span data-ttu-id="635c6-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="635c6-117">-DataFactoryName</span></span>
<span data-ttu-id="635c6-118">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="635c6-118">The data factory name.</span></span>

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

### <span data-ttu-id="635c6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="635c6-119">-DefaultProfile</span></span>
<span data-ttu-id="635c6-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="635c6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="635c6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="635c6-121">-Force</span></span>
<span data-ttu-id="635c6-122">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="635c6-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="635c6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="635c6-123">-InputObject</span></span>
<span data-ttu-id="635c6-124">시작할 트리거 개체.</span><span class="sxs-lookup"><span data-stu-id="635c6-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="635c6-125">-이름</span><span class="sxs-lookup"><span data-stu-id="635c6-125">-Name</span></span>
<span data-ttu-id="635c6-126">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="635c6-126">The trigger name.</span></span>

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

### <span data-ttu-id="635c6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="635c6-127">-ResourceGroupName</span></span>
<span data-ttu-id="635c6-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="635c6-128">The resource group name.</span></span>

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

### <span data-ttu-id="635c6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="635c6-129">-ResourceId</span></span>
<span data-ttu-id="635c6-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="635c6-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="635c6-131">-확인</span><span class="sxs-lookup"><span data-stu-id="635c6-131">-Confirm</span></span>
<span data-ttu-id="635c6-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="635c6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="635c6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="635c6-133">-WhatIf</span></span>
<span data-ttu-id="635c6-134">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="635c6-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="635c6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="635c6-135">CommonParameters</span></span>
<span data-ttu-id="635c6-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="635c6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="635c6-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="635c6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="635c6-138">입력</span><span class="sxs-lookup"><span data-stu-id="635c6-138">INPUTS</span></span>

### <span data-ttu-id="635c6-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="635c6-139">System.String</span></span>

### <span data-ttu-id="635c6-140">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="635c6-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="635c6-141">출력</span><span class="sxs-lookup"><span data-stu-id="635c6-141">OUTPUTS</span></span>

### <span data-ttu-id="635c6-142">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="635c6-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="635c6-143">상속자</span><span class="sxs-lookup"><span data-stu-id="635c6-143">NOTES</span></span>

## <span data-ttu-id="635c6-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="635c6-144">RELATED LINKS</span></span>

[<span data-ttu-id="635c6-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="635c6-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="635c6-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="635c6-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="635c6-147">중지-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="635c6-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="635c6-148">제거-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="635c6-148">Remove-AzDataFactoryV2Trigger</span></span>]()