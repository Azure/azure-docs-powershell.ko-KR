---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: a2bf5146958e10dc60c656f08a329d2ec01d1eeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528729"
---
# <span data-ttu-id="931fd-101">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="931fd-101">Get-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="931fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="931fd-102">SYNOPSIS</span></span>
<span data-ttu-id="931fd-103">Stream Analytics 작업 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="931fd-103">Gets Stream Analytics jobs information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="931fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="931fd-104">SYNTAX</span></span>

### <span data-ttu-id="931fd-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="931fd-105">ByResourceGroup</span></span>
```
Get-AzureRmStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="931fd-106">BySubscription</span><span class="sxs-lookup"><span data-stu-id="931fd-106">BySubscription</span></span>
```
Get-AzureRmStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="931fd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="931fd-107">DESCRIPTION</span></span>
<span data-ttu-id="931fd-108">**AzureRmStreamAnalyticsJob** Cmdlet은 Azure 구독 또는 지정 된 리소스 그룹에 정의 된 모든 스트림 분석 작업을 나열 하거나 리소스 그룹 내의 특정 작업에 대 한 작업 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="931fd-108">The **Get-AzureRmStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="931fd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="931fd-109">EXAMPLES</span></span>

### <span data-ttu-id="931fd-110">예제 1: 구독의 모든 작업에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="931fd-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob
```

<span data-ttu-id="931fd-111">이 명령은 Azure 구독에서 모든 Stream Analytics 작업에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="931fd-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="931fd-112">예제 2: 리소스 그룹의 모든 작업에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="931fd-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="931fd-113">이 명령은 리소스 그룹 StreamAnalytics의 모든 Stream Analytics 작업에 대 한 정보를 반환 합니다 (기본값-서쪽-US).</span><span class="sxs-lookup"><span data-stu-id="931fd-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="931fd-114">예제 3: 리소스 그룹의 특정 작업에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="931fd-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="931fd-115">이 명령은 리소스 그룹 StreamAnalytics의 Stream Analytics 작업 StreamingJob에 대 한 정보를 반환 합니다-기본값-미국-US.</span><span class="sxs-lookup"><span data-stu-id="931fd-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="931fd-116">변수</span><span class="sxs-lookup"><span data-stu-id="931fd-116">PARAMETERS</span></span>

### <span data-ttu-id="931fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="931fd-117">-DefaultProfile</span></span>
<span data-ttu-id="931fd-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="931fd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="931fd-119">-이름</span><span class="sxs-lookup"><span data-stu-id="931fd-119">-Name</span></span>
<span data-ttu-id="931fd-120">검색할 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="931fd-120">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="931fd-121">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="931fd-121">-NoExpand</span></span>
<span data-ttu-id="931fd-122">Cmdlet이 Azure Stream Analytics 작업을 검색 하지만 입력, 출력 및 변환에 대 한 정보를 반환 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="931fd-122">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="931fd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="931fd-123">-ResourceGroupName</span></span>
<span data-ttu-id="931fd-124">Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="931fd-124">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="931fd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="931fd-125">CommonParameters</span></span>
<span data-ttu-id="931fd-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="931fd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="931fd-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="931fd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="931fd-128">입력</span><span class="sxs-lookup"><span data-stu-id="931fd-128">INPUTS</span></span>

### <span data-ttu-id="931fd-129">않아야</span><span class="sxs-lookup"><span data-stu-id="931fd-129">None</span></span>
<span data-ttu-id="931fd-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="931fd-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="931fd-131">출력</span><span class="sxs-lookup"><span data-stu-id="931fd-131">OUTPUTS</span></span>

### <span data-ttu-id="931fd-132">System.webserver. List ' 1 [[Microsoft Azure.]. PSJob, Microsoft Azure. commands 분석]] Microsoft Azure. e. e. e. e. e t e 분석.</span><span class="sxs-lookup"><span data-stu-id="931fd-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="931fd-133">상속자</span><span class="sxs-lookup"><span data-stu-id="931fd-133">NOTES</span></span>

## <span data-ttu-id="931fd-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="931fd-134">RELATED LINKS</span></span>

[<span data-ttu-id="931fd-135">새로운 AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="931fd-135">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="931fd-136">제거-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="931fd-136">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="931fd-137">시작-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="931fd-137">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="931fd-138">중지-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="931fd-138">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


