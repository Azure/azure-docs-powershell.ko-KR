---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: c900973947418ebfb1eba3b503fc40a9f81a68ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973968"
---
# <span data-ttu-id="df95b-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="df95b-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="df95b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df95b-102">SYNOPSIS</span></span>
<span data-ttu-id="df95b-103">Stream Analytics에서 함수의 기본 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="df95b-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="df95b-104">구문</span><span class="sxs-lookup"><span data-stu-id="df95b-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df95b-105">설명</span><span class="sxs-lookup"><span data-stu-id="df95b-105">DESCRIPTION</span></span>
<span data-ttu-id="df95b-106">**Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet은 Azure Stream Analytics에서 함수의 기본 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="df95b-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="df95b-107">기본 정의 및 New-AzStreamAnalyticsFunction cmdlet을 사용하여 함수를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df95b-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="df95b-108">함수를 만들기 전에 기본 정의를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df95b-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="df95b-109">예제</span><span class="sxs-lookup"><span data-stu-id="df95b-109">EXAMPLES</span></span>

### <span data-ttu-id="df95b-110">예제 1: Stream Analytics 함수의 기본 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="df95b-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="df95b-111">이 명령은 on 파일에 지정된 매개 변수를 사용하여 ScoreTweet이라는 함수의 RetrieveDefaultDefinitionRequest.js정의합니다.</span><span class="sxs-lookup"><span data-stu-id="df95b-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="df95b-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="df95b-112">PARAMETERS</span></span>

### <span data-ttu-id="df95b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df95b-113">-DefaultProfile</span></span>
<span data-ttu-id="df95b-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df95b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df95b-115">-File</span><span class="sxs-lookup"><span data-stu-id="df95b-115">-File</span></span>
<span data-ttu-id="df95b-116">검색 기본 함수 정의 요청에 대한 요청 본문의 JSON(JavaScript 개체 표기)을 포함하는 .json 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df95b-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df95b-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="df95b-117">-JobName</span></span>
<span data-ttu-id="df95b-118">함수가 속한 Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df95b-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="df95b-119">이 cmdlet은 이 매개 변수가 지정하는 작업의 함수에 대한 기본 정의를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="df95b-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="df95b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="df95b-120">-Name</span></span>
<span data-ttu-id="df95b-121">이 cmdlet이 기본 정의를 제공하는 Stream Analytics 함수의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df95b-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df95b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df95b-122">-ResourceGroupName</span></span>
<span data-ttu-id="df95b-123">Stream Analytics 함수가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="df95b-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="df95b-124">이 cmdlet은 이 매개 변수가 지정하는 그룹에 대한 함수 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="df95b-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="df95b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df95b-125">CommonParameters</span></span>
<span data-ttu-id="df95b-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="df95b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df95b-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="df95b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df95b-128">입력</span><span class="sxs-lookup"><span data-stu-id="df95b-128">INPUTS</span></span>

### <span data-ttu-id="df95b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="df95b-129">System.String</span></span>

## <span data-ttu-id="df95b-130">출력</span><span class="sxs-lookup"><span data-stu-id="df95b-130">OUTPUTS</span></span>

### <span data-ttu-id="df95b-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="df95b-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="df95b-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="df95b-132">NOTES</span></span>

## <span data-ttu-id="df95b-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df95b-133">RELATED LINKS</span></span>

[<span data-ttu-id="df95b-134">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="df95b-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)


