---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 3f98ff38d5e74b7b167dc3a168a1cc05a42a7a23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697041"
---
# <span data-ttu-id="b130b-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="b130b-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="b130b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b130b-102">SYNOPSIS</span></span>
<span data-ttu-id="b130b-103">트리거 실행에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b130b-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="b130b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b130b-104">SYNTAX</span></span>

### <span data-ttu-id="b130b-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b130b-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b130b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b130b-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b130b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b130b-107">DESCRIPTION</span></span>
<span data-ttu-id="b130b-108">**AzDataFactoryV2TriggerRun** 명령은 지정 된 시간에 지정한 트리거에 대 한 트리거 실행에 대 한 자세한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b130b-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="b130b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b130b-109">EXAMPLES</span></span>

### <span data-ttu-id="b130b-110">예제 1: 트리거 실행에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="b130b-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="b130b-111">이 명령은 "2017-09-01" 및 "2019-09-30" 간에 시작 된 팩토리 "WikiADF"의 "WikiTrigger"에 대 한 실행 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b130b-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="b130b-112">변수</span><span class="sxs-lookup"><span data-stu-id="b130b-112">PARAMETERS</span></span>

### <span data-ttu-id="b130b-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b130b-113">-DataFactory</span></span>
<span data-ttu-id="b130b-114">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b130b-114">The data factory object.</span></span>

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

### <span data-ttu-id="b130b-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b130b-115">-DataFactoryName</span></span>
<span data-ttu-id="b130b-116">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b130b-116">The data factory name.</span></span>

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

### <span data-ttu-id="b130b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b130b-117">-DefaultProfile</span></span>
<span data-ttu-id="b130b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b130b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b130b-119">-이름</span><span class="sxs-lookup"><span data-stu-id="b130b-119">-Name</span></span>
<span data-ttu-id="b130b-120">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b130b-120">The trigger name.</span></span>

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

### <span data-ttu-id="b130b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b130b-121">-ResourceGroupName</span></span>
<span data-ttu-id="b130b-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b130b-122">The resource group name.</span></span>

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

### <span data-ttu-id="b130b-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="b130b-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="b130b-124">트리거 실행이 ISO8601 format에서 실행 되기 시작 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="b130b-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="b130b-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="b130b-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="b130b-126">트리거 실행이 ISO8601 형식으로 실행 되기 시작 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="b130b-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="b130b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b130b-127">CommonParameters</span></span>
<span data-ttu-id="b130b-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b130b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b130b-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b130b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b130b-130">입력</span><span class="sxs-lookup"><span data-stu-id="b130b-130">INPUTS</span></span>

### <span data-ttu-id="b130b-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b130b-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="b130b-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b130b-132">System.String</span></span>

## <span data-ttu-id="b130b-133">출력</span><span class="sxs-lookup"><span data-stu-id="b130b-133">OUTPUTS</span></span>

### <span data-ttu-id="b130b-134">DataFactoryV2. PSTriggerRun/.</span><span class="sxs-lookup"><span data-stu-id="b130b-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="b130b-135">상속자</span><span class="sxs-lookup"><span data-stu-id="b130b-135">NOTES</span></span>

## <span data-ttu-id="b130b-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b130b-136">RELATED LINKS</span></span>

[<span data-ttu-id="b130b-137">시작-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b130b-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="b130b-138">중지-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="b130b-138">Stop-AzDataFactoryV2Trigger</span></span>]()

