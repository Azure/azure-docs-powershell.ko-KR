---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/start-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 20bd934a35fdf0cf907e83f22c8148fdfe5425db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535048"
---
# <span data-ttu-id="82acf-101">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="82acf-101">Start-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="82acf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82acf-102">SYNOPSIS</span></span>
<span data-ttu-id="82acf-103">Stream Analytics 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="82acf-103">Starts a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82acf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="82acf-104">SYNTAX</span></span>

```
Start-AzureRmStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82acf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="82acf-105">DESCRIPTION</span></span>
<span data-ttu-id="82acf-106">**AzureRmStreamAnalyticsJob** Cmdlet은 Azure에서 Stream Analytics 작업을 비동기적으로 배포 하 고 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="82acf-106">The **Start-AzureRmStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="82acf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="82acf-107">EXAMPLES</span></span>

### <span data-ttu-id="82acf-108">예제 1: Stream Analytics 작업 시작</span><span class="sxs-lookup"><span data-stu-id="82acf-108">EXAMPLE 1: Start a Stream Analytics job</span></span>
```
PS C:\>Start-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="82acf-109">이 명령은 작업 StreamingJob을 시작 하 고 출력 이벤트 스트림이 timestamp 2014 년 1 ~ 7-03T01:00Z에 시작 되도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82acf-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="82acf-110">변수</span><span class="sxs-lookup"><span data-stu-id="82acf-110">PARAMETERS</span></span>

### <span data-ttu-id="82acf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82acf-111">-DefaultProfile</span></span>
<span data-ttu-id="82acf-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82acf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82acf-113">-이름</span><span class="sxs-lookup"><span data-stu-id="82acf-113">-Name</span></span>
<span data-ttu-id="82acf-114">시작할 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82acf-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82acf-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="82acf-115">-OutputStartMode</span></span>
<span data-ttu-id="82acf-116">작업의 시작 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82acf-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="82acf-117">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="82acf-117">Valid values are:</span></span> 
- <span data-ttu-id="82acf-118">JobStartTime-이 값은 작업이 시작 될 때 출력 이벤트 스트림의 시작 지점이 시작 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="82acf-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="82acf-119">CustomTime-이 값은 출력 이벤트 스트림의 시작 지점이 *OutputStartTime* 매개 변수에 지정 된 사용자 지정 시간에 시작 되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="82acf-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 <span data-ttu-id="82acf-120">--LastOutputEventTime-이 값은 출력 이벤트 스트림의 시작 지점이 마지막 이벤트 출력 시간에서 시작 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="82acf-120">-- LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="82acf-121">속성이 없으면 JobStartTime입니다.</span><span class="sxs-lookup"><span data-stu-id="82acf-121">If the property is absent, the default is JobStartTime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82acf-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="82acf-122">-OutputStartTime</span></span>
<span data-ttu-id="82acf-123">출력 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82acf-123">Specifies the output start time.</span></span>
<span data-ttu-id="82acf-124">이 값은 출력 이벤트 스트림의 시작 지점을 나타내는 ISO 8601 형식 지정 된 타임 스탬프 이거나, 스트리밍 작업이 시작 될 때마다 출력 이벤트 스트림이 시작 됨을 나타내는 $Null입니다.</span><span class="sxs-lookup"><span data-stu-id="82acf-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="82acf-125">*OutputStartMode* 가 customtime으로 설정 된 경우이 속성에 값이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="82acf-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82acf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82acf-126">-ResourceGroupName</span></span>
<span data-ttu-id="82acf-127">Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82acf-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82acf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82acf-128">CommonParameters</span></span>
<span data-ttu-id="82acf-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="82acf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82acf-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82acf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82acf-131">입력</span><span class="sxs-lookup"><span data-stu-id="82acf-131">INPUTS</span></span>

### <span data-ttu-id="82acf-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="82acf-132">System.String</span></span>

### <span data-ttu-id="82acf-133">시스템 Null 허용 ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="82acf-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="82acf-134">출력</span><span class="sxs-lookup"><span data-stu-id="82acf-134">OUTPUTS</span></span>

### <span data-ttu-id="82acf-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="82acf-135">System.Boolean</span></span>

## <span data-ttu-id="82acf-136">상속자</span><span class="sxs-lookup"><span data-stu-id="82acf-136">NOTES</span></span>

## <span data-ttu-id="82acf-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82acf-137">RELATED LINKS</span></span>

[<span data-ttu-id="82acf-138">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="82acf-138">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="82acf-139">새로운 AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="82acf-139">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="82acf-140">제거-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="82acf-140">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="82acf-141">중지-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="82acf-141">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


