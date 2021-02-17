---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 5844863cf56008d5d73fae7eef644dfd8e27c239
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198841"
---
# <span data-ttu-id="2a8c9-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="2a8c9-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="2a8c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a8c9-102">SYNOPSIS</span></span>
<span data-ttu-id="2a8c9-103">트리거 실행에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="2a8c9-104">구문</span><span class="sxs-lookup"><span data-stu-id="2a8c9-104">SYNTAX</span></span>

### <span data-ttu-id="2a8c9-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="2a8c9-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a8c9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2a8c9-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a8c9-107">설명</span><span class="sxs-lookup"><span data-stu-id="2a8c9-107">DESCRIPTION</span></span>
<span data-ttu-id="2a8c9-108">**Get-AzDataFactoryV2TriggerRun** 명령은 지정된 시간 프레임에서 지정된 트리거에 대한 트리거 실행에 대한 자세한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="2a8c9-109">예제</span><span class="sxs-lookup"><span data-stu-id="2a8c9-109">EXAMPLES</span></span>

### <span data-ttu-id="2a8c9-110">예제 1: 트리거 실행에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="2a8c9-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded
```

<span data-ttu-id="2a8c9-111">이 명령은 "2017-09-01"과 "2019-09-30" 사이에 시작된 팩터리 "WikiADF"의 "WikiTrigger"에 대한 실행에 대한 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="2a8c9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a8c9-112">PARAMETERS</span></span>

### <span data-ttu-id="2a8c9-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2a8c9-113">-DataFactory</span></span>
<span data-ttu-id="2a8c9-114">데이터 팩터리 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-114">The data factory object.</span></span>

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

### <span data-ttu-id="2a8c9-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2a8c9-115">-DataFactoryName</span></span>
<span data-ttu-id="2a8c9-116">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-116">The data factory name.</span></span>

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

### <span data-ttu-id="2a8c9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a8c9-117">-DefaultProfile</span></span>
<span data-ttu-id="2a8c9-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a8c9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2a8c9-119">-Name</span></span>
<span data-ttu-id="2a8c9-120">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-120">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a8c9-121">-ResourceGroupName</span></span>
<span data-ttu-id="2a8c9-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-122">The resource group name.</span></span>

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

### <span data-ttu-id="2a8c9-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="2a8c9-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="2a8c9-124">트리거 실행이 ISO8601 형식으로 실행하기 시작한 시간 또는 그 이후의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c9-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="2a8c9-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="2a8c9-126">트리거 실행이 ISO8601 형식으로 실행되기 시작한 시간 또는 이전 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a8c9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a8c9-127">CommonParameters</span></span>
<span data-ttu-id="2a8c9-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a8c9-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2a8c9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a8c9-130">입력</span><span class="sxs-lookup"><span data-stu-id="2a8c9-130">INPUTS</span></span>

### <span data-ttu-id="2a8c9-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2a8c9-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="2a8c9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2a8c9-132">System.String</span></span>

## <span data-ttu-id="2a8c9-133">출력</span><span class="sxs-lookup"><span data-stu-id="2a8c9-133">OUTPUTS</span></span>

### <span data-ttu-id="2a8c9-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="2a8c9-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="2a8c9-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2a8c9-135">NOTES</span></span>

## <span data-ttu-id="2a8c9-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a8c9-136">RELATED LINKS</span></span>

[<span data-ttu-id="2a8c9-137">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2a8c9-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2a8c9-138">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2a8c9-138">Stop-AzDataFactoryV2Trigger</span></span>]()

