---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: f9139514850fe9d538c58d14813e91d2d24de502
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874301"
---
# <span data-ttu-id="49373-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="49373-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="49373-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49373-102">SYNOPSIS</span></span>
<span data-ttu-id="49373-103">스트림 분석에서 함수에 연결할 수 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="49373-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="49373-104">구문과</span><span class="sxs-lookup"><span data-stu-id="49373-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49373-105">설명은</span><span class="sxs-lookup"><span data-stu-id="49373-105">DESCRIPTION</span></span>
<span data-ttu-id="49373-106">**테스트 AzStreamAnalyticsFunction** Cmdlet은 Azure Stream Analytics가 함수에 연결할 수 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="49373-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="49373-107">예제의</span><span class="sxs-lookup"><span data-stu-id="49373-107">EXAMPLES</span></span>

### <span data-ttu-id="49373-108">예제 1: Stream Analytics 함수 테스트</span><span class="sxs-lookup"><span data-stu-id="49373-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="49373-109">이 명령은 StreamJob22 이라는 작업에서 ScoreTweet 이라는 함수의 연결 상태를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="49373-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="49373-110">변수</span><span class="sxs-lookup"><span data-stu-id="49373-110">PARAMETERS</span></span>

### <span data-ttu-id="49373-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49373-111">-DefaultProfile</span></span>
<span data-ttu-id="49373-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49373-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49373-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="49373-113">-JobName</span></span>
<span data-ttu-id="49373-114">함수가 속한 Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49373-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="49373-115">-이름</span><span class="sxs-lookup"><span data-stu-id="49373-115">-Name</span></span>
<span data-ttu-id="49373-116">이 cmdlet이 테스트 하는 Stream Analytics 함수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49373-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="49373-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49373-117">-ResourceGroupName</span></span>
<span data-ttu-id="49373-118">Stream Analytics 함수가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="49373-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="49373-119">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹의 함수를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="49373-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="49373-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49373-120">CommonParameters</span></span>
<span data-ttu-id="49373-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="49373-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49373-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49373-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49373-123">입력</span><span class="sxs-lookup"><span data-stu-id="49373-123">INPUTS</span></span>

### <span data-ttu-id="49373-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="49373-124">System.String</span></span>

## <span data-ttu-id="49373-125">출력</span><span class="sxs-lookup"><span data-stu-id="49373-125">OUTPUTS</span></span>

### <span data-ttu-id="49373-126">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="49373-126">System.Boolean</span></span>

## <span data-ttu-id="49373-127">상속자</span><span class="sxs-lookup"><span data-stu-id="49373-127">NOTES</span></span>

## <span data-ttu-id="49373-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49373-128">RELATED LINKS</span></span>

[<span data-ttu-id="49373-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="49373-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="49373-130">새로운 AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="49373-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="49373-131">제거-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="49373-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


