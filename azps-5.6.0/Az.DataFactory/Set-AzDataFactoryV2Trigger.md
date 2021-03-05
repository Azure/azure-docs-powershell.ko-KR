---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Trigger.md
ms.openlocfilehash: b0058f21f472f14e97898ea81636fa000034bed5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006928"
---
# <span data-ttu-id="10e70-101">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="10e70-101">Set-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="10e70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10e70-102">SYNOPSIS</span></span>
<span data-ttu-id="10e70-103">데이터 팩터리에서 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-103">Creates a trigger in a data factory.</span></span>

## <span data-ttu-id="10e70-104">구문</span><span class="sxs-lookup"><span data-stu-id="10e70-104">SYNTAX</span></span>

### <span data-ttu-id="10e70-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="10e70-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10e70-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="10e70-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10e70-107">설명</span><span class="sxs-lookup"><span data-stu-id="10e70-107">DESCRIPTION</span></span>
<span data-ttu-id="10e70-108">**Set-AzDataFactoryV2Trigger** cmdlet은 데이터 팩터리에서 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-108">The **Set-AzDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="10e70-109">이미 존재하는 트리거의 이름을 지정하면 cmdlet에서 트리거를 바꾸기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="10e70-110">Force 매개 _변수를 지정하는_ 경우 cmdlet은 확인을 요청하지 않고 기존 트리거를 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="10e70-111">트리거는 '중지됨' 상태로 생성됩니다. 즉, 트리거가 참조하는 파이프라인을 즉시 호출하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="10e70-112">예제</span><span class="sxs-lookup"><span data-stu-id="10e70-112">EXAMPLES</span></span>

### <span data-ttu-id="10e70-113">예제 1: 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="10e70-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="10e70-114">데이터 팩터리 "WikiADF"에서 "ScheduledTrigger"라는 새 트리거를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="10e70-115">트리거는 '중지됨' 상태로 생성됩니다. 즉, 즉시 시작되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="10e70-116">cmdlet을 사용하여 트리거를 `Start-AzDataFactoryV2Trigger` 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-116">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="10e70-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="10e70-117">PARAMETERS</span></span>

### <span data-ttu-id="10e70-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="10e70-118">-DataFactoryName</span></span>
<span data-ttu-id="10e70-119">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-119">The data factory name.</span></span>

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

### <span data-ttu-id="10e70-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e70-120">-DefaultProfile</span></span>
<span data-ttu-id="10e70-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10e70-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="10e70-122">-DefinitionFile</span></span>
<span data-ttu-id="10e70-123">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10e70-124">-Force</span><span class="sxs-lookup"><span data-stu-id="10e70-124">-Force</span></span>
<span data-ttu-id="10e70-125">확인을 요청하지 않고 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="10e70-126">-Name</span><span class="sxs-lookup"><span data-stu-id="10e70-126">-Name</span></span>
<span data-ttu-id="10e70-127">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-127">The trigger name.</span></span>

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

### <span data-ttu-id="10e70-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10e70-128">-ResourceGroupName</span></span>
<span data-ttu-id="10e70-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-129">The resource group name.</span></span>

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

### <span data-ttu-id="10e70-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10e70-130">-ResourceId</span></span>
<span data-ttu-id="10e70-131">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="10e70-132">-확인</span><span class="sxs-lookup"><span data-stu-id="10e70-132">-Confirm</span></span>
<span data-ttu-id="10e70-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10e70-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10e70-134">-WhatIf</span></span>
<span data-ttu-id="10e70-135">cmdlet이 실행되지만 cmdlet을 실행하지 않는 경우 발생하는 것을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="10e70-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e70-136">CommonParameters</span></span>
<span data-ttu-id="10e70-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="10e70-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e70-138">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="10e70-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e70-139">입력</span><span class="sxs-lookup"><span data-stu-id="10e70-139">INPUTS</span></span>

### <span data-ttu-id="10e70-140">System.String</span><span class="sxs-lookup"><span data-stu-id="10e70-140">System.String</span></span>

## <span data-ttu-id="10e70-141">출력</span><span class="sxs-lookup"><span data-stu-id="10e70-141">OUTPUTS</span></span>

### <span data-ttu-id="10e70-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="10e70-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="10e70-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="10e70-143">NOTES</span></span>

## <span data-ttu-id="10e70-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10e70-144">RELATED LINKS</span></span>

[<span data-ttu-id="10e70-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="10e70-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="10e70-146">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="10e70-146">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="10e70-147">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="10e70-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="10e70-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="10e70-148">Remove-AzDataFactoryV2Trigger</span></span>]()
