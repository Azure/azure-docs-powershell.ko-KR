---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 8e4f547d615a88957ffbf133dd725e2453ef7a11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703385"
---
# <span data-ttu-id="61a2d-101">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="61a2d-101">Stop-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="61a2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="61a2d-103">데이터 팩터리에 트리거를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a2d-103">Stops a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61a2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="61a2d-104">SYNTAX</span></span>

### <span data-ttu-id="61a2d-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="61a2d-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61a2d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="61a2d-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61a2d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="61a2d-107">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61a2d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="61a2d-108">DESCRIPTION</span></span>
<span data-ttu-id="61a2d-109">**AzureRmDataFactoryV2Trigger** cmdlet은 데이터 팩터리에 트리거를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a2d-109">The **Stop-AzureRmDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="61a2d-110">트리거가 ' 시작 됨 ' 상태인 경우 cmdlet은 트리거를 중지 하 고 더 이상 파이프라인을 호출 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61a2d-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="61a2d-111">트리거가 이미 ' 중지 됨 ' 상태인 경우에는이 cmdlet이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61a2d-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="61a2d-112">Force 매개 변수를 지정 하면 cmdlet은 트리거를 중지 하기 전에 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61a2d-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="61a2d-113">예제의</span><span class="sxs-lookup"><span data-stu-id="61a2d-113">EXAMPLES</span></span>

### <span data-ttu-id="61a2d-114">예제 1: 트리거 중지</span><span class="sxs-lookup"><span data-stu-id="61a2d-114">Example 1: Stop a trigger</span></span>
```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="61a2d-115">Data factory "WikiADF"에서 "ScheduledTrigger" 이라는 트리거를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a2d-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="61a2d-116">변수</span><span class="sxs-lookup"><span data-stu-id="61a2d-116">PARAMETERS</span></span>

### <span data-ttu-id="61a2d-117">-확인</span><span class="sxs-lookup"><span data-stu-id="61a2d-117">-Confirm</span></span>
<span data-ttu-id="61a2d-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a2d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61a2d-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="61a2d-119">-DataFactoryName</span></span>
<span data-ttu-id="61a2d-120">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61a2d-120">The data factory name.</span></span>

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

### <span data-ttu-id="61a2d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="61a2d-121">-Force</span></span>
<span data-ttu-id="61a2d-122">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a2d-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="61a2d-123">-이름</span><span class="sxs-lookup"><span data-stu-id="61a2d-123">-Name</span></span>
<span data-ttu-id="61a2d-124">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61a2d-124">The trigger name.</span></span>

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

### <span data-ttu-id="61a2d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61a2d-125">-ResourceGroupName</span></span>
<span data-ttu-id="61a2d-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61a2d-126">The resource group name.</span></span>

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

### <span data-ttu-id="61a2d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61a2d-127">-ResourceId</span></span>
<span data-ttu-id="61a2d-128">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="61a2d-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="61a2d-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61a2d-129">-InputObject</span></span>
<span data-ttu-id="61a2d-130">시작할 트리거 개체.</span><span class="sxs-lookup"><span data-stu-id="61a2d-130">Trigger object to start.</span></span>

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

### <span data-ttu-id="61a2d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61a2d-131">-WhatIf</span></span>
<span data-ttu-id="61a2d-132">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="61a2d-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="61a2d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a2d-133">-DefaultProfile</span></span>
<span data-ttu-id="61a2d-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="61a2d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a2d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a2d-135">CommonParameters</span></span>
<span data-ttu-id="61a2d-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="61a2d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a2d-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61a2d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a2d-138">입력</span><span class="sxs-lookup"><span data-stu-id="61a2d-138">INPUTS</span></span>

### <span data-ttu-id="61a2d-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="61a2d-139">System.String</span></span>
<span data-ttu-id="61a2d-140">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="61a2d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="61a2d-141">출력</span><span class="sxs-lookup"><span data-stu-id="61a2d-141">OUTPUTS</span></span>

### <span data-ttu-id="61a2d-142">DataFactoryV2 ' 1 [[Microsoft Azure. PSTrigger, Microsoft Azure. DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="61a2d-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="61a2d-143">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="61a2d-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="61a2d-144">상속자</span><span class="sxs-lookup"><span data-stu-id="61a2d-144">NOTES</span></span>

## <span data-ttu-id="61a2d-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61a2d-145">RELATED LINKS</span></span>

[<span data-ttu-id="61a2d-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="61a2d-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="61a2d-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="61a2d-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="61a2d-148">시작-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="61a2d-148">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="61a2d-149">제거-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="61a2d-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
