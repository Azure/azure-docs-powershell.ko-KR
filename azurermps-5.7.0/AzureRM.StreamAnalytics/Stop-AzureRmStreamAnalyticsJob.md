---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/stop-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 13e977ebe4acdfb799d830620ce7963ad1066177
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524791"
---
# <span data-ttu-id="74b1e-101">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="74b1e-101">Stop-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="74b1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="74b1e-103">Stream Analytics 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="74b1e-103">Stops a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74b1e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="74b1e-104">SYNTAX</span></span>

```
Stop-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74b1e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="74b1e-105">DESCRIPTION</span></span>
<span data-ttu-id="74b1e-106">**AzureRmStreamAnalyticsJob** cmdlet은 비동기적으로 스트림 분석 작업을 중지 하 고 Azure에서 실행 되 던 리소스의 할당을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="74b1e-106">The **Stop-AzureRmStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="74b1e-107">작업 정의 및 메타 데이터는 Azure 포털 및 관리 Api를 통해 구독 내에서 계속 사용할 수 있으며,이에 따라 작업을 편집 하 고 다시 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74b1e-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="74b1e-108">중지 된 상태의 작업에 대해서는 요금이 부과 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74b1e-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="74b1e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="74b1e-109">EXAMPLES</span></span>

### <span data-ttu-id="74b1e-110">예제 1: 실행 중인 작업 중지</span><span class="sxs-lookup"><span data-stu-id="74b1e-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="74b1e-111">이 명령은 작업 StreamingJob을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="74b1e-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="74b1e-112">변수</span><span class="sxs-lookup"><span data-stu-id="74b1e-112">PARAMETERS</span></span>

### <span data-ttu-id="74b1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b1e-113">-DefaultProfile</span></span>
<span data-ttu-id="74b1e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="74b1e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74b1e-115">-이름</span><span class="sxs-lookup"><span data-stu-id="74b1e-115">-Name</span></span>
<span data-ttu-id="74b1e-116">중지할 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="74b1e-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b1e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b1e-117">-ResourceGroupName</span></span>
<span data-ttu-id="74b1e-118">Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="74b1e-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74b1e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b1e-119">CommonParameters</span></span>
<span data-ttu-id="74b1e-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="74b1e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b1e-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74b1e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b1e-122">입력</span><span class="sxs-lookup"><span data-stu-id="74b1e-122">INPUTS</span></span>

### <span data-ttu-id="74b1e-123">않아야</span><span class="sxs-lookup"><span data-stu-id="74b1e-123">None</span></span>
<span data-ttu-id="74b1e-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74b1e-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="74b1e-125">출력</span><span class="sxs-lookup"><span data-stu-id="74b1e-125">OUTPUTS</span></span>

### <span data-ttu-id="74b1e-126">System. 개체</span><span class="sxs-lookup"><span data-stu-id="74b1e-126">System.Object</span></span>

## <span data-ttu-id="74b1e-127">상속자</span><span class="sxs-lookup"><span data-stu-id="74b1e-127">NOTES</span></span>

## <span data-ttu-id="74b1e-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74b1e-128">RELATED LINKS</span></span>

[<span data-ttu-id="74b1e-129">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="74b1e-129">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="74b1e-130">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="74b1e-130">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="74b1e-131">새로운 AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="74b1e-131">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="74b1e-132">제거-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="74b1e-132">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="74b1e-133">시작-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="74b1e-133">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)


