---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: ceedee89473385202037cfedb23e4373995b6f98
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043106"
---
# <span data-ttu-id="5dd95-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5dd95-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="5dd95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dd95-102">SYNOPSIS</span></span>
<span data-ttu-id="5dd95-103">Stream Analytics 작업에서 함수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dd95-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="5dd95-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5dd95-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dd95-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5dd95-105">DESCRIPTION</span></span>
<span data-ttu-id="5dd95-106">**AzStreamAnalyticsFunction** Cmdlet은 Azure Stream Analytics 작업에 정의 된 함수의 목록이 나 특정 함수에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dd95-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="5dd95-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5dd95-107">EXAMPLES</span></span>

### <span data-ttu-id="5dd95-108">예제 1: 모든 Stream Analytics 함수 가져오기</span><span class="sxs-lookup"><span data-stu-id="5dd95-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="5dd95-109">이 명령은 StreamJob22 이라는 작업에 정의 된 함수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dd95-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="5dd95-110">예제 2: 특정 Stream Analytics 함수 가져오기</span><span class="sxs-lookup"><span data-stu-id="5dd95-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="5dd95-111">이 명령은 StreamJob22 이라는 작업에 정의 된 ScoreTweet 이라는 함수에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dd95-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="5dd95-112">변수</span><span class="sxs-lookup"><span data-stu-id="5dd95-112">PARAMETERS</span></span>

### <span data-ttu-id="5dd95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dd95-113">-DefaultProfile</span></span>
<span data-ttu-id="5dd95-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5dd95-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dd95-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="5dd95-115">-JobName</span></span>
<span data-ttu-id="5dd95-116">함수가 속한 Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dd95-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="5dd95-117">이 cmdlet은이 매개 변수에서 지정 하는 작업에 대 한 함수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dd95-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="5dd95-118">-이름</span><span class="sxs-lookup"><span data-stu-id="5dd95-118">-Name</span></span>
<span data-ttu-id="5dd95-119">이 cmdlet이 가져오는 Stream Analytics 함수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dd95-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5dd95-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dd95-120">-ResourceGroupName</span></span>
<span data-ttu-id="5dd95-121">스트림 분석 함수가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dd95-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="5dd95-122">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 대 한 함수를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5dd95-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5dd95-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dd95-123">CommonParameters</span></span>
<span data-ttu-id="5dd95-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dd95-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dd95-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dd95-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dd95-126">입력</span><span class="sxs-lookup"><span data-stu-id="5dd95-126">INPUTS</span></span>

### <span data-ttu-id="5dd95-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5dd95-127">System.String</span></span>

## <span data-ttu-id="5dd95-128">출력</span><span class="sxs-lookup"><span data-stu-id="5dd95-128">OUTPUTS</span></span>

### <span data-ttu-id="5dd95-129">Microsoft. i. a i m/. a i m/. i m a 함수</span><span class="sxs-lookup"><span data-stu-id="5dd95-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="5dd95-130">상속자</span><span class="sxs-lookup"><span data-stu-id="5dd95-130">NOTES</span></span>

## <span data-ttu-id="5dd95-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5dd95-131">RELATED LINKS</span></span>

[<span data-ttu-id="5dd95-132">새로운 AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5dd95-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="5dd95-133">제거-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5dd95-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="5dd95-134">테스트-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="5dd95-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


