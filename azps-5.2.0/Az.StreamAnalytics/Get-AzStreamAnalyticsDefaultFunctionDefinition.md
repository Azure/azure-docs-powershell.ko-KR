---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EF16CE43-1035-4ED0-B9D1-E475DF659ECE
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsdefaultfunctiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsDefaultFunctionDefinition.md
ms.openlocfilehash: 1854c2e060dbbc83ba196043debb0ba08c9a933e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366465"
---
# <span data-ttu-id="17359-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span><span class="sxs-lookup"><span data-stu-id="17359-101">Get-AzStreamAnalyticsDefaultFunctionDefinition</span></span>

## <span data-ttu-id="17359-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17359-102">SYNOPSIS</span></span>
<span data-ttu-id="17359-103">Stream Analytics에서 함수의 기본 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17359-103">Gets the default definition of a function in Stream Analytics.</span></span>

## <span data-ttu-id="17359-104">구문</span><span class="sxs-lookup"><span data-stu-id="17359-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsDefaultFunctionDefinition [-JobName] <String> [-Name] <String> [-File] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17359-105">설명</span><span class="sxs-lookup"><span data-stu-id="17359-105">DESCRIPTION</span></span>
<span data-ttu-id="17359-106">**Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet은 Azure Stream Analytics에서 함수의 기본 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17359-106">The **Get-AzStreamAnalyticsDefaultFunctionDefinition** cmdlet gets the default definition of a function in Azure Stream Analytics.</span></span>
<span data-ttu-id="17359-107">기본 정의 및 New-AzStreamAnalyticsFunction cmdlet을 사용하여 함수를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17359-107">You can use the default definition and the New-AzStreamAnalyticsFunction cmdlet to create a function.</span></span>
<span data-ttu-id="17359-108">함수를 만들기 전에 기본 정의를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17359-108">You can modify the default definition before you create a function.</span></span>

## <span data-ttu-id="17359-109">예제</span><span class="sxs-lookup"><span data-stu-id="17359-109">EXAMPLES</span></span>

### <span data-ttu-id="17359-110">예제 1: Stream Analytics 함수의 기본 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17359-110">Example 1: Get the default definition of a Stream Analytics function</span></span>
```
PS C:\>Get-AzStreamAnalyticsDefaultFunctionDefinition -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\RetrieveDefaultDefinitionRequest.json" -Name "ScoreTweet"
```

<span data-ttu-id="17359-111">이 명령은 RetrieveDefaultDefinitionRequest.json 파일에 지정된 매개 변수를 사용하여 ScoreTweet이라는 함수의 기본 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17359-111">This command gets the default definition of the function named ScoreTweet by using the parameters specified in the RetrieveDefaultDefinitionRequest.json file.</span></span>

## <span data-ttu-id="17359-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17359-112">PARAMETERS</span></span>

### <span data-ttu-id="17359-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17359-113">-DefaultProfile</span></span>
<span data-ttu-id="17359-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17359-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17359-115">-File</span><span class="sxs-lookup"><span data-stu-id="17359-115">-File</span></span>
<span data-ttu-id="17359-116">기본 함수 정의 요청에 대한 요청 본문의 JSON(JavaScript Object Notation) 표현을 포함하는 .json 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17359-116">Specifies the path of a .json file that contains the JavaScript Object Notation (JSON) representation of the request body for the retrieve default function definition request.</span></span>

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

### <span data-ttu-id="17359-117">-JobName</span><span class="sxs-lookup"><span data-stu-id="17359-117">-JobName</span></span>
<span data-ttu-id="17359-118">함수가 속한 Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17359-118">Specifies the name of the Stream Analytics job to which functions belong.</span></span>
<span data-ttu-id="17359-119">이 cmdlet은 이 매개 변수가 지정하는 작업의 함수에 대한 기본 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17359-119">This cmdlet gets the default definition for a function in the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="17359-120">-Name</span><span class="sxs-lookup"><span data-stu-id="17359-120">-Name</span></span>
<span data-ttu-id="17359-121">이 cmdlet이 기본 정의를 얻을 Stream Analytics 함수의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17359-121">Specifies the name of the Stream Analytics function for which this cmdlet gets the default definition.</span></span>

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

### <span data-ttu-id="17359-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17359-122">-ResourceGroupName</span></span>
<span data-ttu-id="17359-123">Stream Analytics 함수가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17359-123">Specifies the name of the resource group to which Stream Analytics functions belongs.</span></span>
<span data-ttu-id="17359-124">이 cmdlet은 이 매개 변수가 지정하는 그룹에 대한 함수 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="17359-124">This cmdlet gets a function definition for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="17359-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17359-125">CommonParameters</span></span>
<span data-ttu-id="17359-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17359-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17359-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="17359-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17359-128">입력</span><span class="sxs-lookup"><span data-stu-id="17359-128">INPUTS</span></span>

### <span data-ttu-id="17359-129">System.String</span><span class="sxs-lookup"><span data-stu-id="17359-129">System.String</span></span>

## <span data-ttu-id="17359-130">출력</span><span class="sxs-lookup"><span data-stu-id="17359-130">OUTPUTS</span></span>

### <span data-ttu-id="17359-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="17359-131">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="17359-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="17359-132">NOTES</span></span>

## <span data-ttu-id="17359-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17359-133">RELATED LINKS</span></span>

[<span data-ttu-id="17359-134">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="17359-134">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)


