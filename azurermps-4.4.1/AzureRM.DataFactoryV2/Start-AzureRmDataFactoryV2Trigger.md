---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 610aabd21fa1a3e7ae19430c4ce5d79d89f7ab3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538199"
---
# <span data-ttu-id="00f69-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="00f69-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="00f69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00f69-102">SYNOPSIS</span></span>

<span data-ttu-id="00f69-103">데이터 팩터리에 트리거를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="00f69-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00f69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00f69-104">SYNTAX</span></span>

### <span data-ttu-id="00f69-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="00f69-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="00f69-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="00f69-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="00f69-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="00f69-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="00f69-108">설명은</span><span class="sxs-lookup"><span data-stu-id="00f69-108">DESCRIPTION</span></span>

<span data-ttu-id="00f69-109">**AzureRmDataFactoryV2Trigger** cmdlet은 데이터 팩터리에 트리거를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="00f69-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="00f69-110">트리거가 ' 중지 됨 ' 상태인 경우 cmdlet은 트리거를 시작 하 고 결과적으로 해당 정의에 따라 파이프라인을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="00f69-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="00f69-111">트리거가 이미 ' 시작 됨 ' 상태에 있는 경우에는이 cmdlet이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00f69-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="00f69-112">Force 매개 변수를 지정 하면 cmdlet이 트리거를 시작 하기 전에 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00f69-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>


## <span data-ttu-id="00f69-113">예제의</span><span class="sxs-lookup"><span data-stu-id="00f69-113">EXAMPLES</span></span>

### <span data-ttu-id="00f69-114">예제 1: 트리거 시작</span><span class="sxs-lookup"><span data-stu-id="00f69-114">Example 1: Start a trigger</span></span>

```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="00f69-115">Data factory "WikiADF"에서 "ScheduledTrigger" 이라는 트리거를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="00f69-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>


## <span data-ttu-id="00f69-116">변수</span><span class="sxs-lookup"><span data-stu-id="00f69-116">PARAMETERS</span></span>

### <span data-ttu-id="00f69-117">-확인</span><span class="sxs-lookup"><span data-stu-id="00f69-117">-Confirm</span></span>
<span data-ttu-id="00f69-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="00f69-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f69-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="00f69-119">-DataFactoryName</span></span>
<span data-ttu-id="00f69-120">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00f69-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00f69-121">-Force</span><span class="sxs-lookup"><span data-stu-id="00f69-121">-Force</span></span>
<span data-ttu-id="00f69-122">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="00f69-122">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00f69-123">-이름</span><span class="sxs-lookup"><span data-stu-id="00f69-123">-Name</span></span>
<span data-ttu-id="00f69-124">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00f69-124">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00f69-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f69-125">-ResourceGroupName</span></span>
<span data-ttu-id="00f69-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00f69-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00f69-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00f69-127">-ResourceId</span></span>
<span data-ttu-id="00f69-128">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="00f69-128">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00f69-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00f69-129">-InputObject</span></span>
<span data-ttu-id="00f69-130">시작할 트리거 개체.</span><span class="sxs-lookup"><span data-stu-id="00f69-130">Trigger object to start.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00f69-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00f69-131">-WhatIf</span></span>
<span data-ttu-id="00f69-132">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="00f69-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="00f69-133">입력</span><span class="sxs-lookup"><span data-stu-id="00f69-133">INPUTS</span></span>

### <span data-ttu-id="00f69-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="00f69-134">System.String</span></span>
<span data-ttu-id="00f69-135">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="00f69-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="00f69-136">출력</span><span class="sxs-lookup"><span data-stu-id="00f69-136">OUTPUTS</span></span>

### <span data-ttu-id="00f69-137">DataFactoryV2 ' 1 [[Microsoft Azure. PSTrigger, Microsoft Azure. DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="00f69-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="00f69-138">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="00f69-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="00f69-139">상속자</span><span class="sxs-lookup"><span data-stu-id="00f69-139">NOTES</span></span>

## <span data-ttu-id="00f69-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00f69-140">RELATED LINKS</span></span>
[<span data-ttu-id="00f69-141">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="00f69-141">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="00f69-142">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="00f69-142">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="00f69-143">중지-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="00f69-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="00f69-144">제거-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="00f69-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
