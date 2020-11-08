---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Trigger.md
ms.openlocfilehash: d5426decba60df0e18e331c01481ae4f99d5c27c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204065"
---
# <span data-ttu-id="b738c-101">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b738c-101">Remove-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="b738c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b738c-102">SYNOPSIS</span></span>
<span data-ttu-id="b738c-103">데이터 팩터리에 트리거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b738c-103">Removes a trigger from a data factory.</span></span>

## <span data-ttu-id="b738c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b738c-104">SYNTAX</span></span>

### <span data-ttu-id="b738c-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b738c-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b738c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b738c-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b738c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b738c-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b738c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b738c-108">DESCRIPTION</span></span>
<span data-ttu-id="b738c-109">**AzDataFactoryV2Trigger** cmdlet은 데이터 팩터리에 트리거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b738c-109">The **Remove-AzDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="b738c-110">_Force_ 매개 변수를 지정 하면 cmdlet은 트리거를 제거 하기 전에 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b738c-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="b738c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b738c-111">EXAMPLES</span></span>

### <span data-ttu-id="b738c-112">예제 1: 트리거 제거</span><span class="sxs-lookup"><span data-stu-id="b738c-112">Example 1: Remove a trigger</span></span>
```
Remove-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="b738c-113">Data factory "WikiADF"에서 "ScheduledTrigger" 이라는 트리거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b738c-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="b738c-114">변수</span><span class="sxs-lookup"><span data-stu-id="b738c-114">PARAMETERS</span></span>

### <span data-ttu-id="b738c-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b738c-115">-DataFactoryName</span></span>
<span data-ttu-id="b738c-116">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b738c-116">The data factory name.</span></span>

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

### <span data-ttu-id="b738c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b738c-117">-DefaultProfile</span></span>
<span data-ttu-id="b738c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b738c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b738c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b738c-119">-Force</span></span>
<span data-ttu-id="b738c-120">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b738c-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b738c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b738c-121">-InputObject</span></span>
<span data-ttu-id="b738c-122">제거할 트리거 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b738c-122">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="b738c-123">-이름</span><span class="sxs-lookup"><span data-stu-id="b738c-123">-Name</span></span>
<span data-ttu-id="b738c-124">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b738c-124">The trigger name.</span></span>

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

### <span data-ttu-id="b738c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b738c-125">-ResourceGroupName</span></span>
<span data-ttu-id="b738c-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b738c-126">The resource group name.</span></span>

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

### <span data-ttu-id="b738c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b738c-127">-ResourceId</span></span>
<span data-ttu-id="b738c-128">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b738c-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b738c-129">-확인</span><span class="sxs-lookup"><span data-stu-id="b738c-129">-Confirm</span></span>
<span data-ttu-id="b738c-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b738c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b738c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b738c-131">-WhatIf</span></span>
<span data-ttu-id="b738c-132">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b738c-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b738c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b738c-133">CommonParameters</span></span>
<span data-ttu-id="b738c-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b738c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b738c-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b738c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b738c-136">입력</span><span class="sxs-lookup"><span data-stu-id="b738c-136">INPUTS</span></span>

### <span data-ttu-id="b738c-137">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="b738c-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

### <span data-ttu-id="b738c-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b738c-138">System.String</span></span>

## <span data-ttu-id="b738c-139">출력</span><span class="sxs-lookup"><span data-stu-id="b738c-139">OUTPUTS</span></span>

### <span data-ttu-id="b738c-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b738c-140">System.Boolean</span></span>

## <span data-ttu-id="b738c-141">상속자</span><span class="sxs-lookup"><span data-stu-id="b738c-141">NOTES</span></span>

## <span data-ttu-id="b738c-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b738c-142">RELATED LINKS</span></span>

[<span data-ttu-id="b738c-143">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b738c-143">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b738c-144">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b738c-144">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b738c-145">시작-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b738c-145">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b738c-146">중지-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b738c-146">Stop-AzDataFactoryV2Trigger</span></span>]()

