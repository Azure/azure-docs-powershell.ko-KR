---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365730"
---
# <span data-ttu-id="858f1-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="858f1-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="858f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="858f1-102">SYNOPSIS</span></span>
<span data-ttu-id="858f1-103">데이터 팩터리에서 트리거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="858f1-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="858f1-104">구문</span><span class="sxs-lookup"><span data-stu-id="858f1-104">SYNTAX</span></span>

### <span data-ttu-id="858f1-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="858f1-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="858f1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="858f1-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="858f1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="858f1-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="858f1-108">설명</span><span class="sxs-lookup"><span data-stu-id="858f1-108">DESCRIPTION</span></span>
<span data-ttu-id="858f1-109">**Remove-AzDataFactoryV2Trigger** cmdlet은 데이터 팩터리에서 트리거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="858f1-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="858f1-110">Force _매개_ 변수를 지정하면 트리거를 제거하기 전에 cmdlet이 프롬프트를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="858f1-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="858f1-111">예제</span><span class="sxs-lookup"><span data-stu-id="858f1-111">EXAMPLES</span></span>

### <span data-ttu-id="858f1-112">예제 1: 트리거 제거</span><span class="sxs-lookup"><span data-stu-id="858f1-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="858f1-113">데이터 팩터리 "WikiADF"에서 "ScheduledTrigger"라는 트리거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="858f1-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="858f1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="858f1-114">PARAMETERS</span></span>

### <span data-ttu-id="858f1-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="858f1-115">-DataFactoryName</span></span>
<span data-ttu-id="858f1-116">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="858f1-116">The data factory name.</span></span>

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

### <span data-ttu-id="858f1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858f1-117">-DefaultProfile</span></span>
<span data-ttu-id="858f1-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="858f1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="858f1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="858f1-119">-Force</span></span>
<span data-ttu-id="858f1-120">확인 메시지를 표시하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="858f1-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="858f1-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="858f1-121">-InputObject</span></span>
<span data-ttu-id="858f1-122">제거할 트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="858f1-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="858f1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="858f1-123">-Name</span></span>
<span data-ttu-id="858f1-124">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="858f1-124">The trigger name.</span></span>

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

### <span data-ttu-id="858f1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="858f1-125">-ResourceGroupName</span></span>
<span data-ttu-id="858f1-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="858f1-126">The resource group name.</span></span>

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

### <span data-ttu-id="858f1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="858f1-127">-ResourceId</span></span>
<span data-ttu-id="858f1-128">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="858f1-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="858f1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="858f1-129">-Confirm</span></span>
<span data-ttu-id="858f1-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="858f1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="858f1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="858f1-131">-WhatIf</span></span>
<span data-ttu-id="858f1-132">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="858f1-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="858f1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858f1-133">CommonParameters</span></span>
<span data-ttu-id="858f1-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="858f1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858f1-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="858f1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858f1-136">입력</span><span class="sxs-lookup"><span data-stu-id="858f1-136">INPUTS</span></span>

### <span data-ttu-id="858f1-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="858f1-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="858f1-138">System.String</span><span class="sxs-lookup"><span data-stu-id="858f1-138">System.String</span></span>

## <span data-ttu-id="858f1-139">출력</span><span class="sxs-lookup"><span data-stu-id="858f1-139">OUTPUTS</span></span>

### <span data-ttu-id="858f1-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="858f1-140">System.Boolean</span></span>

## <span data-ttu-id="858f1-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="858f1-141">NOTES</span></span>

## <span data-ttu-id="858f1-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="858f1-142">RELATED LINKS</span></span>

[<span data-ttu-id="858f1-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="858f1-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="858f1-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="858f1-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="858f1-145">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="858f1-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="858f1-146">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="858f1-146">Stop-AzDataFactoryV2Trigger</span></span>]()

