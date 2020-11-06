---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1D10C1EA-632A-4953-85B1-596A45C30B24
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 7b1130d222e36d53fbef1dcbb60f6d74615c5b11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530634"
---
# <span data-ttu-id="7709d-101">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7709d-101">Get-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="7709d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7709d-102">SYNOPSIS</span></span>
<span data-ttu-id="7709d-103">Stream Analytics 작업 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7709d-103">Gets Stream Analytics jobs information.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7709d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7709d-104">SYNTAX</span></span>

### <span data-ttu-id="7709d-105">지정 된 리소스 그룹의 stream analytics 개체의 경우</span><span class="sxs-lookup"><span data-stu-id="7709d-105">For stream analytics objects in the given resource group</span></span>
```
Get-AzureRmStreamAnalyticsJob [-ResourceGroupName] <String> [[-Name] <String>] [-NoExpand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7709d-106">지정 된 구독의 stream analytics 개체</span><span class="sxs-lookup"><span data-stu-id="7709d-106">For stream analytics objects in the given subscription</span></span>
```
Get-AzureRmStreamAnalyticsJob [-NoExpand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7709d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7709d-107">DESCRIPTION</span></span>
<span data-ttu-id="7709d-108">**AzureRmStreamAnalyticsJob** Cmdlet은 Azure 구독 또는 지정 된 리소스 그룹에 정의 된 모든 스트림 분석 작업을 나열 하거나 리소스 그룹 내의 특정 작업에 대 한 작업 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7709d-108">The **Get-AzureRmStreamAnalyticsJob** cmdlet lists all Stream Analytics jobs defined in the Azure subscription or specified resource group or gets job information about a specific job within a resource group.</span></span>

## <span data-ttu-id="7709d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7709d-109">EXAMPLES</span></span>

### <span data-ttu-id="7709d-110">예제 1: 구독의 모든 작업에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="7709d-110">EXAMPLE 1: Get information about all jobs in a subscription</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob
```

<span data-ttu-id="7709d-111">이 명령은 Azure 구독에서 모든 Stream Analytics 작업에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7709d-111">This command returns information about all the Stream Analytics jobs in the Azure subscription.</span></span>

### <span data-ttu-id="7709d-112">예제 2: 리소스 그룹의 모든 작업에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="7709d-112">EXAMPLE 2: Get information about all jobs in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US"
```

<span data-ttu-id="7709d-113">이 명령은 리소스 그룹 StreamAnalytics의 모든 Stream Analytics 작업에 대 한 정보를 반환 합니다 (기본값-서쪽-US).</span><span class="sxs-lookup"><span data-stu-id="7709d-113">This command returns information about all the Stream Analytics jobs in the resource group StreamAnalytics-Default-West-US.</span></span>

### <span data-ttu-id="7709d-114">예제 3: 리소스 그룹의 특정 작업에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="7709d-114">EXAMPLE 3: Get information about a specific job in a resource group</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="7709d-115">이 명령은 리소스 그룹 StreamAnalytics의 Stream Analytics 작업 StreamingJob에 대 한 정보를 반환 합니다-기본값-미국-US.</span><span class="sxs-lookup"><span data-stu-id="7709d-115">This command returns information about the Stream Analytics job StreamingJob in the resource group StreamAnalytics-Default-West-US.</span></span>

## <span data-ttu-id="7709d-116">변수</span><span class="sxs-lookup"><span data-stu-id="7709d-116">PARAMETERS</span></span>

### <span data-ttu-id="7709d-117">-이름</span><span class="sxs-lookup"><span data-stu-id="7709d-117">-Name</span></span>
<span data-ttu-id="7709d-118">검색할 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7709d-118">Specifies the name of the Azure Stream Analytics job to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: For stream analytics objects in the given resource group
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7709d-119">-NoExpand</span><span class="sxs-lookup"><span data-stu-id="7709d-119">-NoExpand</span></span>
<span data-ttu-id="7709d-120">Cmdlet이 Azure Stream Analytics 작업을 검색 하지만 입력, 출력 및 변환에 대 한 정보를 반환 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7709d-120">Indicates the cmdlet will retrieve the Azure Stream Analytics job, but not return information on its inputs, outputs, and transformation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7709d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7709d-121">-ResourceGroupName</span></span>
<span data-ttu-id="7709d-122">Azure Stream Analytics 작업이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7709d-122">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: For stream analytics objects in the given resource group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7709d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7709d-123">-DefaultProfile</span></span>
<span data-ttu-id="7709d-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7709d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7709d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7709d-125">CommonParameters</span></span>
<span data-ttu-id="7709d-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7709d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7709d-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7709d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7709d-128">입력</span><span class="sxs-lookup"><span data-stu-id="7709d-128">INPUTS</span></span>

## <span data-ttu-id="7709d-129">출력</span><span class="sxs-lookup"><span data-stu-id="7709d-129">OUTPUTS</span></span>

### <span data-ttu-id="7709d-130">System.webserver. List ' 1 [[Microsoft Azure.]. PSJob, Microsoft Azure. commands 분석]] Microsoft Azure. e. e. e. e. e t e 분석.</span><span class="sxs-lookup"><span data-stu-id="7709d-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob, Microsoft.Azure.Commands.StreamAnalytics]]            Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="7709d-131">상속자</span><span class="sxs-lookup"><span data-stu-id="7709d-131">NOTES</span></span>

## <span data-ttu-id="7709d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7709d-132">RELATED LINKS</span></span>

[<span data-ttu-id="7709d-133">새로운 AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7709d-133">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="7709d-134">제거-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7709d-134">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="7709d-135">시작-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7709d-135">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="7709d-136">중지-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7709d-136">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


