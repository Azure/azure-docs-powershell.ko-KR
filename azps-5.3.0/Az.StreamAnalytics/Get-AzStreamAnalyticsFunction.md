---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 7F08A880-1FC5-4542-8AB8-927BB999A552
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsFunction.md
ms.openlocfilehash: ceedee89473385202037cfedb23e4373995b6f98
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384364"
---
# <span data-ttu-id="6ca6c-101">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6ca6c-101">Get-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="6ca6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ca6c-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca6c-103">Stream Analytics 작업에서 함수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ca6c-103">Gets functions in a Stream Analytics job.</span></span>

## <span data-ttu-id="6ca6c-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ca6c-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ca6c-105">설명</span><span class="sxs-lookup"><span data-stu-id="6ca6c-105">DESCRIPTION</span></span>
<span data-ttu-id="6ca6c-106">**Get-AzStreamAnalyticsFunction** cmdlet은 Azure Stream Analytics 작업에서 정의된 함수 목록 또는 특정 함수에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ca6c-106">The **Get-AzStreamAnalyticsFunction** cmdlet gets a list of the functions that are defined in an Azure Stream Analytics job or information about a specific function.</span></span>

## <span data-ttu-id="6ca6c-107">예제</span><span class="sxs-lookup"><span data-stu-id="6ca6c-107">EXAMPLES</span></span>

### <span data-ttu-id="6ca6c-108">예제 1: 모든 Stream Analytics 함수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ca6c-108">Example 1: Get all Stream Analytics functions</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22"
```

<span data-ttu-id="6ca6c-109">이 명령은 StreamJob22라는 작업에서 정의된 함수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ca6c-109">This command gets the functions defined on the job named StreamJob22.</span></span>

### <span data-ttu-id="6ca6c-110">예제 2: 특정 Stream Analytics 함수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ca6c-110">Example 2: Get a specific Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="6ca6c-111">이 명령은 StreamJob22라는 작업에서 정의된 ScoreTweet이라는 함수에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ca6c-111">This command gets information about the function named ScoreTweet defined on the job named StreamJob22.</span></span>

## <span data-ttu-id="6ca6c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ca6c-112">PARAMETERS</span></span>

### <span data-ttu-id="6ca6c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca6c-113">-DefaultProfile</span></span>
<span data-ttu-id="6ca6c-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ca6c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ca6c-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="6ca6c-115">-JobName</span></span>
<span data-ttu-id="6ca6c-116">함수가 속한 Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca6c-116">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="6ca6c-117">이 cmdlet은 이 매개 변수가 지정하는 작업의 함수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ca6c-117">This cmdlet gets functions for the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="6ca6c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6ca6c-118">-Name</span></span>
<span data-ttu-id="6ca6c-119">이 cmdlet에서 얻을 Stream Analytics 함수의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca6c-119">Specifies the name of the Stream Analytics function that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6ca6c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca6c-120">-ResourceGroupName</span></span>
<span data-ttu-id="6ca6c-121">Stream Analytics 함수가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca6c-121">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="6ca6c-122">이 cmdlet은 이 매개 변수가 지정하는 그룹에 대한 함수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ca6c-122">This cmdlet gets functions for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6ca6c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca6c-123">CommonParameters</span></span>
<span data-ttu-id="6ca6c-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ca6c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca6c-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6ca6c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca6c-126">입력</span><span class="sxs-lookup"><span data-stu-id="6ca6c-126">INPUTS</span></span>

### <span data-ttu-id="6ca6c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="6ca6c-127">System.String</span></span>

## <span data-ttu-id="6ca6c-128">출력</span><span class="sxs-lookup"><span data-stu-id="6ca6c-128">OUTPUTS</span></span>

### <span data-ttu-id="6ca6c-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="6ca6c-129">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="6ca6c-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6ca6c-130">NOTES</span></span>

## <span data-ttu-id="6ca6c-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ca6c-131">RELATED LINKS</span></span>

[<span data-ttu-id="6ca6c-132">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6ca6c-132">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="6ca6c-133">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6ca6c-133">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="6ca6c-134">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6ca6c-134">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


