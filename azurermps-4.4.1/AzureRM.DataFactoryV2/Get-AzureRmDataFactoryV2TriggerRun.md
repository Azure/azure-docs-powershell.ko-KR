---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: d5ea2dee1f6023b9505c38a58d364b7aa92591db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704075"
---
# <span data-ttu-id="56f73-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="56f73-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="56f73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56f73-102">SYNOPSIS</span></span>
<span data-ttu-id="56f73-103">트리거 실행에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="56f73-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56f73-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56f73-104">SYNTAX</span></span>

### <span data-ttu-id="56f73-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="56f73-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="56f73-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="56f73-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="56f73-107">설명은</span><span class="sxs-lookup"><span data-stu-id="56f73-107">DESCRIPTION</span></span>
<span data-ttu-id="56f73-108">**AzureRmDataFactoryV2TriggerRun** 명령은 지정 된 시간에 지정한 트리거에 대 한 트리거 실행에 대 한 자세한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="56f73-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="56f73-109">예제의</span><span class="sxs-lookup"><span data-stu-id="56f73-109">EXAMPLES</span></span>

### <span data-ttu-id="56f73-110">예제 1: 트리거 실행에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="56f73-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded

```

<span data-ttu-id="56f73-111">이 명령은 "2017-09-01" 및 "2019-09-30" 간에 시작 된 팩토리 "WikiADF"의 "WikiTrigger"에 대 한 실행 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="56f73-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="56f73-112">변수</span><span class="sxs-lookup"><span data-stu-id="56f73-112">PARAMETERS</span></span>

### <span data-ttu-id="56f73-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="56f73-113">-DataFactory</span></span>
<span data-ttu-id="56f73-114">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="56f73-114">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56f73-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="56f73-115">-DataFactoryName</span></span>
<span data-ttu-id="56f73-116">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56f73-116">The data factory name.</span></span>

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

### <span data-ttu-id="56f73-117">-이름</span><span class="sxs-lookup"><span data-stu-id="56f73-117">-Name</span></span>
<span data-ttu-id="56f73-118">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56f73-118">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f73-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56f73-119">-ResourceGroupName</span></span>
<span data-ttu-id="56f73-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56f73-120">The resource group name.</span></span>

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

### <span data-ttu-id="56f73-121">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="56f73-121">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="56f73-122">트리거 실행이 ISO8601 format에서 실행 되기 시작 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="56f73-122">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f73-123">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="56f73-123">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="56f73-124">트리거 실행이 ISO8601 형식으로 실행 되기 시작 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="56f73-124">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="56f73-125">입력</span><span class="sxs-lookup"><span data-stu-id="56f73-125">INPUTS</span></span>

### <span data-ttu-id="56f73-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="56f73-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="56f73-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="56f73-127">System.String</span></span>


## <span data-ttu-id="56f73-128">출력</span><span class="sxs-lookup"><span data-stu-id="56f73-128">OUTPUTS</span></span>

### <span data-ttu-id="56f73-129">DataFactoryV2 ' 1 [[Microsoft Azure. PSTriggerRun, Microsoft Azure. DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="56f73-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="56f73-130">DataFactoryV2. PSTriggerRun/.</span><span class="sxs-lookup"><span data-stu-id="56f73-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>


## <span data-ttu-id="56f73-131">상속자</span><span class="sxs-lookup"><span data-stu-id="56f73-131">NOTES</span></span>

## <span data-ttu-id="56f73-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56f73-132">RELATED LINKS</span></span>
[<span data-ttu-id="56f73-133">시작-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="56f73-133">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="56f73-134">중지-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="56f73-134">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

