---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 04A6FD47-482C-4EA6-9375-D8B6FD1F2659
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 1f959f96b02296d4cc25cca06ae6c95bdef98af7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973856"
---
# <span data-ttu-id="0af79-101">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0af79-101">Get-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="0af79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0af79-102">SYNOPSIS</span></span>
<span data-ttu-id="0af79-103">지정된 Stream Analytics 작업 또는 출력에 정의된 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0af79-103">Gets the outputs defined in a specified Stream Analytics job or output.</span></span>

## <span data-ttu-id="0af79-104">구문</span><span class="sxs-lookup"><span data-stu-id="0af79-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0af79-105">설명</span><span class="sxs-lookup"><span data-stu-id="0af79-105">DESCRIPTION</span></span>
<span data-ttu-id="0af79-106">**Get-AzStreamAnalyticsOutput** cmdlet은 지정된 Stream Analytics 작업에서 정의되거나 특정 출력에 대한 정보를 얻을 수 있는 모든 출력을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0af79-106">The **Get-AzStreamAnalyticsOutput** cmdlet lists all of the outputs that are defined in a specified Stream Analytics job or gets information about a specific output.</span></span>

## <span data-ttu-id="0af79-107">예제</span><span class="sxs-lookup"><span data-stu-id="0af79-107">EXAMPLES</span></span>

### <span data-ttu-id="0af79-108">예제 1: 작업 출력에 대한 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0af79-108">Example 1: Get information about job outputs</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

<span data-ttu-id="0af79-109">이 명령은 StreamingJob 작업에서 정의된 출력에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0af79-109">This command returns information about the outputs defined on the job StreamingJob.</span></span>

### <span data-ttu-id="0af79-110">예제 2: 특정 작업 출력에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="0af79-110">Example 2: Get information about a specific job output</span></span>
```powershell
PS C:\>Get-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="0af79-111">이 명령은 StreamingJob 작업에서 정의된 출력이라는 출력에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0af79-111">This command returns information about the output named Output defined on the job StreamingJob.</span></span>

## <span data-ttu-id="0af79-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0af79-112">PARAMETERS</span></span>

### <span data-ttu-id="0af79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af79-113">-DefaultProfile</span></span>
<span data-ttu-id="0af79-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0af79-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0af79-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="0af79-115">-JobName</span></span>
<span data-ttu-id="0af79-116">Azure Stream Analytics 출력이 속한 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0af79-116">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="0af79-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0af79-117">-Name</span></span>
<span data-ttu-id="0af79-118">검색할 Azure Stream Analytics 출력의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0af79-118">Specifies the name of the Azure Stream Analytics output to retrieve.</span></span>

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

### <span data-ttu-id="0af79-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0af79-119">-ResourceGroupName</span></span>
<span data-ttu-id="0af79-120">Azure Stream Analytics 출력이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0af79-120">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="0af79-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af79-121">CommonParameters</span></span>
<span data-ttu-id="0af79-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0af79-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af79-123">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0af79-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af79-124">입력</span><span class="sxs-lookup"><span data-stu-id="0af79-124">INPUTS</span></span>

### <span data-ttu-id="0af79-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0af79-125">System.String</span></span>

## <span data-ttu-id="0af79-126">출력</span><span class="sxs-lookup"><span data-stu-id="0af79-126">OUTPUTS</span></span>

### <span data-ttu-id="0af79-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="0af79-127">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="0af79-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0af79-128">NOTES</span></span>

## <span data-ttu-id="0af79-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0af79-129">RELATED LINKS</span></span>

[<span data-ttu-id="0af79-130">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0af79-130">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="0af79-131">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0af79-131">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="0af79-132">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0af79-132">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


