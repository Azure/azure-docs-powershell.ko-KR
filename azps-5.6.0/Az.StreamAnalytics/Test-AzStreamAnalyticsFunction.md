---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: d45a46cd0ff38f925a218c2bbab6edf70b97a4ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963499"
---
# <span data-ttu-id="e888d-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e888d-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="e888d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e888d-102">SYNOPSIS</span></span>
<span data-ttu-id="e888d-103">Stream Analytics가 함수에 연결할 수 있는지 여부를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="e888d-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="e888d-104">구문</span><span class="sxs-lookup"><span data-stu-id="e888d-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e888d-105">설명</span><span class="sxs-lookup"><span data-stu-id="e888d-105">DESCRIPTION</span></span>
<span data-ttu-id="e888d-106">**Test-AzStreamAnalyticsFunction** cmdlet은 Azure Stream Analytics가 함수에 연결할 수 있는지 여부를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="e888d-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="e888d-107">예제</span><span class="sxs-lookup"><span data-stu-id="e888d-107">EXAMPLES</span></span>

### <span data-ttu-id="e888d-108">예제 1: Stream Analytics 함수 테스트</span><span class="sxs-lookup"><span data-stu-id="e888d-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="e888d-109">이 명령은 StreamJob22라는 작업에서 ScoreTweet이라는 함수의 연결 상태를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="e888d-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="e888d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e888d-110">PARAMETERS</span></span>

### <span data-ttu-id="e888d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e888d-111">-DefaultProfile</span></span>
<span data-ttu-id="e888d-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e888d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e888d-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="e888d-113">-JobName</span></span>
<span data-ttu-id="e888d-114">함수가 속한 Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e888d-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="e888d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e888d-115">-Name</span></span>
<span data-ttu-id="e888d-116">이 cmdlet에서 테스트하는 Stream Analytics 함수의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e888d-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="e888d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e888d-117">-ResourceGroupName</span></span>
<span data-ttu-id="e888d-118">Stream Analytics 함수가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e888d-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="e888d-119">이 cmdlet은 이 매개 변수가 지정하는 리소스 그룹의 함수를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="e888d-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e888d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e888d-120">CommonParameters</span></span>
<span data-ttu-id="e888d-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e888d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e888d-122">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e888d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e888d-123">입력</span><span class="sxs-lookup"><span data-stu-id="e888d-123">INPUTS</span></span>

### <span data-ttu-id="e888d-124">System.String</span><span class="sxs-lookup"><span data-stu-id="e888d-124">System.String</span></span>

## <span data-ttu-id="e888d-125">출력</span><span class="sxs-lookup"><span data-stu-id="e888d-125">OUTPUTS</span></span>

### <span data-ttu-id="e888d-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e888d-126">System.Boolean</span></span>

## <span data-ttu-id="e888d-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e888d-127">NOTES</span></span>

## <span data-ttu-id="e888d-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e888d-128">RELATED LINKS</span></span>

[<span data-ttu-id="e888d-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e888d-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="e888d-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e888d-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="e888d-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="e888d-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


