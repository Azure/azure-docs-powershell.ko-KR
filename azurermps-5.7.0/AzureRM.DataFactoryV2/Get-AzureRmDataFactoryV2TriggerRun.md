---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
ms.openlocfilehash: 9c6ff7cc27261b6345a7ac8d68b68f095206ff9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536027"
---
# <span data-ttu-id="2c635-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="2c635-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="2c635-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c635-102">SYNOPSIS</span></span>
<span data-ttu-id="2c635-103">트리거 실행에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c635-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c635-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c635-104">SYNTAX</span></span>

### <span data-ttu-id="2c635-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="2c635-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c635-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2c635-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c635-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2c635-107">DESCRIPTION</span></span>
<span data-ttu-id="2c635-108">**AzureRmDataFactoryV2TriggerRun** 명령은 지정 된 시간에 지정한 트리거에 대 한 트리거 실행에 대 한 자세한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c635-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="2c635-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2c635-109">EXAMPLES</span></span>

### <span data-ttu-id="2c635-110">예제 1: 트리거 실행에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="2c635-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="2c635-111">이 명령은 "2017-09-01" 및 "2019-09-30" 간에 시작 된 팩토리 "WikiADF"의 "WikiTrigger"에 대 한 실행 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c635-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="2c635-112">변수</span><span class="sxs-lookup"><span data-stu-id="2c635-112">PARAMETERS</span></span>

### <span data-ttu-id="2c635-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c635-113">-DataFactory</span></span>
<span data-ttu-id="2c635-114">Data factory 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2c635-114">The data factory object.</span></span>

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

### <span data-ttu-id="2c635-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2c635-115">-DataFactoryName</span></span>
<span data-ttu-id="2c635-116">Data factory 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c635-116">The data factory name.</span></span>

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

### <span data-ttu-id="2c635-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c635-117">-DefaultProfile</span></span>
<span data-ttu-id="2c635-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c635-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c635-119">-이름</span><span class="sxs-lookup"><span data-stu-id="2c635-119">-Name</span></span>
<span data-ttu-id="2c635-120">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c635-120">The trigger name.</span></span>

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

### <span data-ttu-id="2c635-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c635-121">-ResourceGroupName</span></span>
<span data-ttu-id="2c635-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c635-122">The resource group name.</span></span>

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

### <span data-ttu-id="2c635-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="2c635-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="2c635-124">트리거 실행이 ISO8601 format에서 실행 되기 시작 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="2c635-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="2c635-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="2c635-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="2c635-126">트리거 실행이 ISO8601 형식으로 실행 되기 시작 하는 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="2c635-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="2c635-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c635-127">CommonParameters</span></span>
<span data-ttu-id="2c635-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c635-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c635-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c635-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c635-130">입력</span><span class="sxs-lookup"><span data-stu-id="2c635-130">INPUTS</span></span>

### <span data-ttu-id="2c635-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2c635-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="2c635-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2c635-132">System.String</span></span>

## <span data-ttu-id="2c635-133">출력</span><span class="sxs-lookup"><span data-stu-id="2c635-133">OUTPUTS</span></span>

### <span data-ttu-id="2c635-134">DataFactoryV2 ' 1 [[Microsoft Azure. PSTriggerRun, Microsoft Azure. DataFactoryV2, Version = 0.1.9.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2c635-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="2c635-135">DataFactoryV2. PSTriggerRun/.</span><span class="sxs-lookup"><span data-stu-id="2c635-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="2c635-136">상속자</span><span class="sxs-lookup"><span data-stu-id="2c635-136">NOTES</span></span>

## <span data-ttu-id="2c635-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c635-137">RELATED LINKS</span></span>

[<span data-ttu-id="2c635-138">시작-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2c635-138">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="2c635-139">중지-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="2c635-139">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

