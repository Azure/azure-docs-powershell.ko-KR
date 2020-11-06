---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8bf4a713784b367363e4f1f9167cfb144d06c0d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538203"
---
# <span data-ttu-id="fa69e-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fa69e-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="fa69e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa69e-102">SYNOPSIS</span></span>
<span data-ttu-id="fa69e-103">데이터 팩터리에 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa69e-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa69e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fa69e-104">SYNTAX</span></span>

### <span data-ttu-id="fa69e-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="fa69e-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fa69e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fa69e-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="fa69e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fa69e-107">DESCRIPTION</span></span>

<span data-ttu-id="fa69e-108">**AzureRmDataFactoryV2Trigger** cmdlet은 데이터 팩터리에 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa69e-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="fa69e-109">이미 존재 하는 트리거의 이름을 지정 하면 cmdlet에서 트리거를 바꾸기 전에 확인을 요청 하는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa69e-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="fa69e-110">_Force_ 매개 변수를 지정 하면 cmdlet은 확인 메시지를 표시 하지 않고 기존 트리거를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="fa69e-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="fa69e-111">트리거는 ' 중지 됨 ' 상태에서 만들어지고,이는 자신이 참조 하는 파이프라인 호출을 즉시 시작 하지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="fa69e-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="fa69e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="fa69e-112">EXAMPLES</span></span>

### <span data-ttu-id="fa69e-113">예제 1: 트리거 만들기</span><span class="sxs-lookup"><span data-stu-id="fa69e-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

```

<span data-ttu-id="fa69e-114">"WikiADF" 데이터 팩터리에 "ScheduledTrigger" 라는 새 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa69e-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="fa69e-115">트리거가 ' 중지 됨 ' 상태에 만들어지고,이는 즉시 시작 되지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="fa69e-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="fa69e-116">트리거는 cmdlet을 사용 하 여 시작할 수 있습니다 `Start-AzureRmDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="fa69e-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="fa69e-117">변수</span><span class="sxs-lookup"><span data-stu-id="fa69e-117">PARAMETERS</span></span>

### <span data-ttu-id="fa69e-118">-확인</span><span class="sxs-lookup"><span data-stu-id="fa69e-118">-Confirm</span></span>
<span data-ttu-id="fa69e-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa69e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa69e-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fa69e-120">-DataFactoryName</span></span>
<span data-ttu-id="fa69e-121">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fa69e-121">The data factory name.</span></span>

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

### <span data-ttu-id="fa69e-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="fa69e-122">-DefinitionFile</span></span>
<span data-ttu-id="fa69e-123">JSON 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="fa69e-123">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa69e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="fa69e-124">-Force</span></span>
<span data-ttu-id="fa69e-125">확인 메시지를 표시 하지 않고 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa69e-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fa69e-126">-이름</span><span class="sxs-lookup"><span data-stu-id="fa69e-126">-Name</span></span>
<span data-ttu-id="fa69e-127">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fa69e-127">The trigger name.</span></span>

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

### <span data-ttu-id="fa69e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa69e-128">-ResourceGroupName</span></span>
<span data-ttu-id="fa69e-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fa69e-129">The resource group name.</span></span>

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

### <span data-ttu-id="fa69e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa69e-130">-ResourceId</span></span>
<span data-ttu-id="fa69e-131">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fa69e-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fa69e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa69e-132">-WhatIf</span></span>
<span data-ttu-id="fa69e-133">Cmdlet이 실행 되지만 cmdlet을 실행 하지 않는 경우의 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fa69e-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="fa69e-134">입력</span><span class="sxs-lookup"><span data-stu-id="fa69e-134">INPUTS</span></span>

### <span data-ttu-id="fa69e-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fa69e-135">System.String</span></span>


## <span data-ttu-id="fa69e-136">출력</span><span class="sxs-lookup"><span data-stu-id="fa69e-136">OUTPUTS</span></span>

### <span data-ttu-id="fa69e-137">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="fa69e-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="fa69e-138">상속자</span><span class="sxs-lookup"><span data-stu-id="fa69e-138">NOTES</span></span>

## <span data-ttu-id="fa69e-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa69e-139">RELATED LINKS</span></span>
[<span data-ttu-id="fa69e-140">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fa69e-140">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="fa69e-141">시작-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fa69e-141">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="fa69e-142">중지-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fa69e-142">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="fa69e-143">제거-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="fa69e-143">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
