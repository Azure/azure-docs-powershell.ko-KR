---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: c675a8da84e61b659c593cc1f963dd1b07c7f316
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524243"
---
# <span data-ttu-id="f3a64-101">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f3a64-101">Get-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="f3a64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3a64-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a64-103">지정한 Stream Analytics 작업 또는 출력에 정의 된 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f3a64-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3a64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3a64-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3a64-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f3a64-105">DESCRIPTION</span></span>
<span data-ttu-id="f3a64-106">**AzureRmStreamAnalyticsOutput** cmdlet은 지정 된 Stream Analytics 작업에 정의 된 모든 출력을 나열 하거나 특정 출력에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f3a64-106">The **Get-AzureRmStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="f3a64-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f3a64-107">EXAMPLES</span></span>

### <span data-ttu-id="f3a64-108">예제 1: 작업 출력에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="f3a64-108">EXAMPLE 1: Get information about job outputs</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="f3a64-109">이 명령은 작업 StreamingJob에 정의 된 출력에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a64-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="f3a64-110">예제 2: 특정 작업 출력에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="f3a64-110">EXAMPLE 2: Get information about a specific job output</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="f3a64-111">이 명령은 job StreamingJob에 정의 된 output 이라는 출력에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a64-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="f3a64-112">변수</span><span class="sxs-lookup"><span data-stu-id="f3a64-112">PARAMETERS</span></span>

### <span data-ttu-id="f3a64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3a64-113">-DefaultProfile</span></span>
<span data-ttu-id="f3a64-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3a64-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3a64-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="f3a64-115">-JobName</span></span>
<span data-ttu-id="f3a64-116">Azure Stream Analytics 출력이 속한 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a64-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="f3a64-117">-이름</span><span class="sxs-lookup"><span data-stu-id="f3a64-117">-Name</span></span>
<span data-ttu-id="f3a64-118">검색할 Azure Stream Analytics 출력의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a64-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="f3a64-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3a64-119">-ResourceGroupName</span></span>
<span data-ttu-id="f3a64-120">Azure Stream Analytics 출력이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a64-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="f3a64-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a64-121">CommonParameters</span></span>
<span data-ttu-id="f3a64-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3a64-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a64-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3a64-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a64-124">입력</span><span class="sxs-lookup"><span data-stu-id="f3a64-124">INPUTS</span></span>

### <span data-ttu-id="f3a64-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f3a64-125">System.String</span></span>

## <span data-ttu-id="f3a64-126">출력</span><span class="sxs-lookup"><span data-stu-id="f3a64-126">OUTPUTS</span></span>

### <span data-ttu-id="f3a64-127">Microsoft. StreamAnalytics. PSOutput</span><span class="sxs-lookup"><span data-stu-id="f3a64-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="f3a64-128">상속자</span><span class="sxs-lookup"><span data-stu-id="f3a64-128">NOTES</span></span>

## <span data-ttu-id="f3a64-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3a64-129">RELATED LINKS</span></span>

[<span data-ttu-id="f3a64-130">새로운 AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f3a64-130">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="f3a64-131">제거-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f3a64-131">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="f3a64-132">테스트-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="f3a64-132">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


