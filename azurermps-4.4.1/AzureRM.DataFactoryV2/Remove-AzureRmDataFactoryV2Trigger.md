---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 3a10820bb0e4ed8c2a9ddb95bc716753a4a96ca0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538216"
---
# <span data-ttu-id="4921a-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4921a-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="4921a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4921a-102">SYNOPSIS</span></span>
<span data-ttu-id="4921a-103">데이터 팩터리에 트리거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4921a-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4921a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4921a-104">SYNTAX</span></span>

### <span data-ttu-id="4921a-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4921a-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4921a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4921a-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4921a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4921a-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4921a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4921a-108">DESCRIPTION</span></span>
<span data-ttu-id="4921a-109">**AzureRmDataFactoryV2Trigger** cmdlet은 데이터 팩터리에 트리거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4921a-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="4921a-110">_Force_ 매개 변수를 지정 하면 cmdlet은 트리거를 제거 하기 전에 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4921a-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="4921a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4921a-111">EXAMPLES</span></span>

### <span data-ttu-id="4921a-112">예제 1: 트리거 제거</span><span class="sxs-lookup"><span data-stu-id="4921a-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="4921a-113">Data factory "WikiADF"에서 "ScheduledTrigger" 이라는 트리거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4921a-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="4921a-114">변수</span><span class="sxs-lookup"><span data-stu-id="4921a-114">PARAMETERS</span></span>

### <span data-ttu-id="4921a-115">-확인</span><span class="sxs-lookup"><span data-stu-id="4921a-115">-Confirm</span></span>
<span data-ttu-id="4921a-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4921a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4921a-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4921a-117">-DataFactoryName</span></span>
<span data-ttu-id="4921a-118">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4921a-118">The data factory name.</span></span>

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

### <span data-ttu-id="4921a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4921a-119">-Force</span></span>
<span data-ttu-id="4921a-120">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4921a-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4921a-121">-이름</span><span class="sxs-lookup"><span data-stu-id="4921a-121">-Name</span></span>
<span data-ttu-id="4921a-122">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4921a-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4921a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4921a-123">-ResourceGroupName</span></span>
<span data-ttu-id="4921a-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4921a-124">The resource group name.</span></span>

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

### <span data-ttu-id="4921a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4921a-125">-ResourceId</span></span>
<span data-ttu-id="4921a-126">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4921a-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4921a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4921a-127">-InputObject</span></span>
<span data-ttu-id="4921a-128">제거할 트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4921a-128">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="4921a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4921a-129">-WhatIf</span></span>
<span data-ttu-id="4921a-130">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4921a-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="4921a-131">입력</span><span class="sxs-lookup"><span data-stu-id="4921a-131">INPUTS</span></span>

### <span data-ttu-id="4921a-132">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="4921a-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="4921a-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4921a-133">System.String</span></span>


## <span data-ttu-id="4921a-134">출력</span><span class="sxs-lookup"><span data-stu-id="4921a-134">OUTPUTS</span></span>

### <span data-ttu-id="4921a-135">System. 개체</span><span class="sxs-lookup"><span data-stu-id="4921a-135">System.Object</span></span>

## <span data-ttu-id="4921a-136">상속자</span><span class="sxs-lookup"><span data-stu-id="4921a-136">NOTES</span></span>

## <span data-ttu-id="4921a-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4921a-137">RELATED LINKS</span></span>
[<span data-ttu-id="4921a-138">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4921a-138">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="4921a-139">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4921a-139">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="4921a-140">시작-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4921a-140">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="4921a-141">중지-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4921a-141">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

