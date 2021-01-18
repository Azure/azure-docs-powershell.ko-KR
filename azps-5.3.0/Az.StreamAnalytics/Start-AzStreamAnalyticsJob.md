---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: 1194a730293d6f0f7b4aca58f508f808a2c6193e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494640"
---
# <span data-ttu-id="c1b93-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c1b93-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="c1b93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1b93-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b93-103">Stream Analytics 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b93-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="c1b93-104">구문</span><span class="sxs-lookup"><span data-stu-id="c1b93-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1b93-105">설명</span><span class="sxs-lookup"><span data-stu-id="c1b93-105">DESCRIPTION</span></span>
<span data-ttu-id="c1b93-106">**Start-AzStreamAnalyticsJob** cmdlet은 Azure에서 Stream Analytics 작업을 비동기적으로 배포하고 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b93-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="c1b93-107">예제</span><span class="sxs-lookup"><span data-stu-id="c1b93-107">EXAMPLES</span></span>

### <span data-ttu-id="c1b93-108">예제 1: Stream Analytics 작업 시작</span><span class="sxs-lookup"><span data-stu-id="c1b93-108">Example 1: Start a Stream Analytics job</span></span>
```powershell
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="c1b93-109">이 명령은 StreamingJob 작업을 시작하고 출력 이벤트 스트림이 타임스탬프 2014-07-03T01:00Z에서 시작된다고 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b93-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="c1b93-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1b93-110">PARAMETERS</span></span>

### <span data-ttu-id="c1b93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b93-111">-DefaultProfile</span></span>
<span data-ttu-id="c1b93-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1b93-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1b93-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c1b93-113">-Name</span></span>
<span data-ttu-id="c1b93-114">시작할 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b93-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

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

### <span data-ttu-id="c1b93-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="c1b93-115">-OutputStartMode</span></span>
<span data-ttu-id="c1b93-116">작업의 시작 모드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b93-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="c1b93-117">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="c1b93-117">Valid values are:</span></span> 
- <span data-ttu-id="c1b93-118">JobStartTime - 이 값은 작업이 시작되면 출력 이벤트 스트림의 시작 지점이 시작해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c1b93-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="c1b93-119">CustomTime - 이 값은 *OutputStartTime* 매개 변수에 지정된 사용자 지정 시간에서 출력 이벤트 스트림의 시작 지점이 시작될 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c1b93-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="c1b93-120">LastOutputEventTime - 이 값은 출력 이벤트 스트림의 시작 지점이 마지막 이벤트 출력 시간에서 시작해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c1b93-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="c1b93-121">속성이 없습니다. 기본값은 JobStartTime입니다.</span><span class="sxs-lookup"><span data-stu-id="c1b93-121">If the property is absent, the default is JobStartTime.</span></span>

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

### <span data-ttu-id="c1b93-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="c1b93-122">-OutputStartTime</span></span>
<span data-ttu-id="c1b93-123">출력 시작 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b93-123">Specifies the output start time.</span></span>
<span data-ttu-id="c1b93-124">이 값은 출력 이벤트 스트림의 시작점을 나타내는 ISO-8601 형식의 타임스탬프 또는 $Null 시작될 때마다 출력 이벤트 스트림이 시작된다고 나타내는 타임스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="c1b93-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="c1b93-125">*OutputStartMode가 CustomTime으로* 설정된 경우 이 속성에 값이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b93-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

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

### <span data-ttu-id="c1b93-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1b93-126">-ResourceGroupName</span></span>
<span data-ttu-id="c1b93-127">Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b93-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="c1b93-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b93-128">CommonParameters</span></span>
<span data-ttu-id="c1b93-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c1b93-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b93-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c1b93-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b93-131">입력</span><span class="sxs-lookup"><span data-stu-id="c1b93-131">INPUTS</span></span>

### <span data-ttu-id="c1b93-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c1b93-132">System.String</span></span>

### <span data-ttu-id="c1b93-133">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c1b93-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c1b93-134">출력</span><span class="sxs-lookup"><span data-stu-id="c1b93-134">OUTPUTS</span></span>

### <span data-ttu-id="c1b93-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1b93-135">System.Boolean</span></span>

## <span data-ttu-id="c1b93-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c1b93-136">NOTES</span></span>

## <span data-ttu-id="c1b93-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1b93-137">RELATED LINKS</span></span>

[<span data-ttu-id="c1b93-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c1b93-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="c1b93-139">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c1b93-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="c1b93-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c1b93-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="c1b93-141">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c1b93-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


