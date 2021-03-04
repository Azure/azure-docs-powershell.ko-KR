---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 2a13466b792426cdf06b7c52a8067f3adf5b787d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993146"
---
# <span data-ttu-id="03193-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="03193-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="03193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03193-102">SYNOPSIS</span></span>
<span data-ttu-id="03193-103">Stream Analytics 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="03193-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="03193-104">구문</span><span class="sxs-lookup"><span data-stu-id="03193-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03193-105">설명</span><span class="sxs-lookup"><span data-stu-id="03193-105">DESCRIPTION</span></span>
<span data-ttu-id="03193-106">**Stop-AzStreamAnalyticsJob** cmdlet은 Stream Analytics 작업이 Azure에서 실행되지 못하게 비동기적으로 중지하고 사용 중인 리소스를 딜로케이트합니다.</span><span class="sxs-lookup"><span data-stu-id="03193-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="03193-107">작업 정의 및 메타데이터는 Azure Portal 및 Management API를 통해 구독 내에서 계속 사용할 수 있으며, 이렇게 하여 작업을 편집하고 다시 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03193-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="03193-108">중지 상태의 작업 요금이 청구되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03193-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="03193-109">예제</span><span class="sxs-lookup"><span data-stu-id="03193-109">EXAMPLES</span></span>

### <span data-ttu-id="03193-110">예제 1: 실행 중인 작업 중지</span><span class="sxs-lookup"><span data-stu-id="03193-110">Example 1: Stop a running job</span></span>
```powershell
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="03193-111">이 명령은 StreamingJob 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="03193-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="03193-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="03193-112">PARAMETERS</span></span>

### <span data-ttu-id="03193-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03193-113">-DefaultProfile</span></span>
<span data-ttu-id="03193-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03193-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03193-115">-Name</span><span class="sxs-lookup"><span data-stu-id="03193-115">-Name</span></span>
<span data-ttu-id="03193-116">중지할 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03193-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="03193-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03193-117">-ResourceGroupName</span></span>
<span data-ttu-id="03193-118">Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03193-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="03193-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03193-119">CommonParameters</span></span>
<span data-ttu-id="03193-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03193-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03193-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03193-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03193-122">입력</span><span class="sxs-lookup"><span data-stu-id="03193-122">INPUTS</span></span>

### <span data-ttu-id="03193-123">System.String</span><span class="sxs-lookup"><span data-stu-id="03193-123">System.String</span></span>

## <span data-ttu-id="03193-124">출력</span><span class="sxs-lookup"><span data-stu-id="03193-124">OUTPUTS</span></span>

### <span data-ttu-id="03193-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03193-125">System.Boolean</span></span>

## <span data-ttu-id="03193-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="03193-126">NOTES</span></span>

## <span data-ttu-id="03193-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03193-127">RELATED LINKS</span></span>

[<span data-ttu-id="03193-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="03193-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="03193-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="03193-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="03193-130">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="03193-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="03193-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="03193-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="03193-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="03193-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


