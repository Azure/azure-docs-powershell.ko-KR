---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/stop-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: d4ec2865f0a0efcc4a306d0614df1c27adddc5b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535043"
---
# <span data-ttu-id="b1d4e-101">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b1d4e-101">Stop-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="b1d4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="b1d4e-103">Stream Analytics 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-103">Stops a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1d4e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1d4e-104">SYNTAX</span></span>

```
Stop-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1d4e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b1d4e-105">DESCRIPTION</span></span>
<span data-ttu-id="b1d4e-106">**AzureRmStreamAnalyticsJob** cmdlet은 비동기적으로 스트림 분석 작업을 중지 하 고 Azure에서 실행 되 던 리소스의 할당을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-106">The **Stop-AzureRmStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="b1d4e-107">작업 정의 및 메타 데이터는 Azure 포털 및 관리 Api를 통해 구독 내에서 계속 사용할 수 있으며,이에 따라 작업을 편집 하 고 다시 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="b1d4e-108">중지 된 상태의 작업에 대해서는 요금이 부과 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="b1d4e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b1d4e-109">EXAMPLES</span></span>

### <span data-ttu-id="b1d4e-110">예제 1: 실행 중인 작업 중지</span><span class="sxs-lookup"><span data-stu-id="b1d4e-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="b1d4e-111">이 명령은 작업 StreamingJob을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="b1d4e-112">변수</span><span class="sxs-lookup"><span data-stu-id="b1d4e-112">PARAMETERS</span></span>

### <span data-ttu-id="b1d4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1d4e-113">-DefaultProfile</span></span>
<span data-ttu-id="b1d4e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1d4e-115">-이름</span><span class="sxs-lookup"><span data-stu-id="b1d4e-115">-Name</span></span>
<span data-ttu-id="b1d4e-116">중지할 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="b1d4e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1d4e-117">-ResourceGroupName</span></span>
<span data-ttu-id="b1d4e-118">Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="b1d4e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1d4e-119">CommonParameters</span></span>
<span data-ttu-id="b1d4e-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1d4e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1d4e-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1d4e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1d4e-122">입력</span><span class="sxs-lookup"><span data-stu-id="b1d4e-122">INPUTS</span></span>

### <span data-ttu-id="b1d4e-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b1d4e-123">System.String</span></span>

## <span data-ttu-id="b1d4e-124">출력</span><span class="sxs-lookup"><span data-stu-id="b1d4e-124">OUTPUTS</span></span>

### <span data-ttu-id="b1d4e-125">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b1d4e-125">System.Boolean</span></span>

## <span data-ttu-id="b1d4e-126">상속자</span><span class="sxs-lookup"><span data-stu-id="b1d4e-126">NOTES</span></span>

## <span data-ttu-id="b1d4e-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1d4e-127">RELATED LINKS</span></span>

[<span data-ttu-id="b1d4e-128">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b1d4e-128">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="b1d4e-129">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b1d4e-129">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="b1d4e-130">새로운 AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b1d4e-130">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="b1d4e-131">제거-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b1d4e-131">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="b1d4e-132">시작-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b1d4e-132">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)


