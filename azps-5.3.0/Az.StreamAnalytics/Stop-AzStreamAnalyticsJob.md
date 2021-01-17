---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 90721eff72d24bbbb27f526e50bcc294ef7ce14a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384252"
---
# <span data-ttu-id="e36aa-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e36aa-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="e36aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e36aa-102">SYNOPSIS</span></span>
<span data-ttu-id="e36aa-103">Stream Analytics 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="e36aa-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="e36aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="e36aa-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e36aa-105">설명</span><span class="sxs-lookup"><span data-stu-id="e36aa-105">DESCRIPTION</span></span>
<span data-ttu-id="e36aa-106">**Stop-AzStreamAnalyticsJob** cmdlet은 Stream Analytics 작업이 Azure에서 실행되지 못하게 비동기적으로 중지하고 사용 중이던 리소스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e36aa-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="e36aa-107">작업 정의 및 메타데이터는 작업을 편집하고 다시 시작할 수 있도록 Azure Portal 및 관리 API를 통해 구독 내에서 계속 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e36aa-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="e36aa-108">중지됨 상태의 작업 요금은 청구되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e36aa-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="e36aa-109">예제</span><span class="sxs-lookup"><span data-stu-id="e36aa-109">EXAMPLES</span></span>

### <span data-ttu-id="e36aa-110">예제 1: 실행 중인 작업 중지</span><span class="sxs-lookup"><span data-stu-id="e36aa-110">Example 1: Stop a running job</span></span>
```powershell
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="e36aa-111">이 명령은 StreamingJob 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="e36aa-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="e36aa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e36aa-112">PARAMETERS</span></span>

### <span data-ttu-id="e36aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e36aa-113">-DefaultProfile</span></span>
<span data-ttu-id="e36aa-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e36aa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e36aa-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e36aa-115">-Name</span></span>
<span data-ttu-id="e36aa-116">중지할 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e36aa-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="e36aa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e36aa-117">-ResourceGroupName</span></span>
<span data-ttu-id="e36aa-118">Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e36aa-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="e36aa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36aa-119">CommonParameters</span></span>
<span data-ttu-id="e36aa-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e36aa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36aa-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e36aa-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36aa-122">입력</span><span class="sxs-lookup"><span data-stu-id="e36aa-122">INPUTS</span></span>

### <span data-ttu-id="e36aa-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e36aa-123">System.String</span></span>

## <span data-ttu-id="e36aa-124">출력</span><span class="sxs-lookup"><span data-stu-id="e36aa-124">OUTPUTS</span></span>

### <span data-ttu-id="e36aa-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e36aa-125">System.Boolean</span></span>

## <span data-ttu-id="e36aa-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e36aa-126">NOTES</span></span>

## <span data-ttu-id="e36aa-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e36aa-127">RELATED LINKS</span></span>

[<span data-ttu-id="e36aa-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e36aa-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="e36aa-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e36aa-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="e36aa-130">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e36aa-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="e36aa-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e36aa-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="e36aa-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e36aa-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


