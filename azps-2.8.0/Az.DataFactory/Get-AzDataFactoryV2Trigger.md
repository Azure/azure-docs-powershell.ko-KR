---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Trigger.md
ms.openlocfilehash: e5afbdd389d1ee9e1b74895743ed47ceed0b4ae9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697046"
---
# <span data-ttu-id="4c3a6-101">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4c3a6-101">Get-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="4c3a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c3a6-102">SYNOPSIS</span></span>
<span data-ttu-id="4c3a6-103">Data factory의 트리거에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-103">Gets information about triggers in a data factory.</span></span>

## <span data-ttu-id="4c3a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4c3a6-104">SYNTAX</span></span>

### <span data-ttu-id="4c3a6-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4c3a6-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c3a6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4c3a6-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Trigger [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c3a6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4c3a6-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Trigger [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c3a6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4c3a6-108">DESCRIPTION</span></span>
<span data-ttu-id="4c3a6-109">**AzDataFactoryV2Trigger** cmdlet은 data factory의 트리거에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-109">The **Get-AzDataFactoryV2Trigger** cmdlet gets information about triggers in a data factory.</span></span> <span data-ttu-id="4c3a6-110">트리거의 이름을 지정 하는 경우 cmdlet은 해당 트리거에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-110">If you specify the name of a trigger, the cmdlet gets information about that trigger.</span></span> <span data-ttu-id="4c3a6-111">이름을 지정 하지 않으면 cmdlet은 data factory의 모든 트리거에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-111">If you do not specify a name, the cmdlet gets information about all triggers in the data factory.</span></span>

## <span data-ttu-id="4c3a6-112">예제의</span><span class="sxs-lookup"><span data-stu-id="4c3a6-112">EXAMPLES</span></span>

### <span data-ttu-id="4c3a6-113">예제 1: 특정 트리거에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="4c3a6-113">Example 1: Get information about a specific trigger</span></span>
```
PS C:\> Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped

    TriggerName       : ScheduledTrigger2
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="4c3a6-114">Data factory "WikiADF"에서 생성 된 모든 트리거의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-114">Gets a list of all triggers that have been created in the data factory "WikiADF".</span></span>

### <span data-ttu-id="4c3a6-115">예제 2: 모든 트리거에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="4c3a6-115">Example 2: Get information about all triggers</span></span>
```
Get-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="4c3a6-116">"WikiADF" 데이터 팩터리에 "ScheduledTrigger" 라는 단일 트리거를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-116">Gets a single trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="4c3a6-117">변수</span><span class="sxs-lookup"><span data-stu-id="4c3a6-117">PARAMETERS</span></span>

### <span data-ttu-id="4c3a6-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4c3a6-118">-DataFactory</span></span>
<span data-ttu-id="4c3a6-119">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-119">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c3a6-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4c3a6-120">-DataFactoryName</span></span>
<span data-ttu-id="4c3a6-121">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-121">The data factory name.</span></span>

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

### <span data-ttu-id="4c3a6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c3a6-122">-DefaultProfile</span></span>
<span data-ttu-id="4c3a6-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c3a6-124">-이름</span><span class="sxs-lookup"><span data-stu-id="4c3a6-124">-Name</span></span>
<span data-ttu-id="4c3a6-125">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c3a6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c3a6-126">-ResourceGroupName</span></span>
<span data-ttu-id="4c3a6-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-127">The resource group name.</span></span>

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

### <span data-ttu-id="4c3a6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c3a6-128">-ResourceId</span></span>
<span data-ttu-id="4c3a6-129">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4c3a6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c3a6-130">CommonParameters</span></span>
<span data-ttu-id="4c3a6-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c3a6-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c3a6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c3a6-133">입력</span><span class="sxs-lookup"><span data-stu-id="4c3a6-133">INPUTS</span></span>

### <span data-ttu-id="4c3a6-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4c3a6-134">System.String</span></span>

### <span data-ttu-id="4c3a6-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4c3a6-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="4c3a6-136">출력</span><span class="sxs-lookup"><span data-stu-id="4c3a6-136">OUTPUTS</span></span>

### <span data-ttu-id="4c3a6-137">DataFactoryV2. PSTrigger/.</span><span class="sxs-lookup"><span data-stu-id="4c3a6-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="4c3a6-138">상속자</span><span class="sxs-lookup"><span data-stu-id="4c3a6-138">NOTES</span></span>

## <span data-ttu-id="4c3a6-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c3a6-139">RELATED LINKS</span></span>

[<span data-ttu-id="4c3a6-140">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4c3a6-140">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="4c3a6-141">시작-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4c3a6-141">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="4c3a6-142">중지-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4c3a6-142">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="4c3a6-143">제거-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="4c3a6-143">Remove-AzDataFactoryV2Trigger</span></span>]()