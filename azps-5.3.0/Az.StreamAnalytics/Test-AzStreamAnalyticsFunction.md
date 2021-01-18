---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 1f2c7e653e96f697a714fef9f7b56c70240f0456
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494639"
---
# <span data-ttu-id="3cd82-101">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3cd82-101">Test-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="3cd82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cd82-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd82-103">Stream Analytics가 함수에 연결할 수 있는지 여부를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd82-103">Tests whether Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="3cd82-104">구문</span><span class="sxs-lookup"><span data-stu-id="3cd82-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cd82-105">설명</span><span class="sxs-lookup"><span data-stu-id="3cd82-105">DESCRIPTION</span></span>
<span data-ttu-id="3cd82-106">**Test-AzStreamAnalyticsFunction** cmdlet은 Azure Stream Analytics가 함수에 연결할 수 있는지 여부를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd82-106">The **Test-AzStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="3cd82-107">예제</span><span class="sxs-lookup"><span data-stu-id="3cd82-107">EXAMPLES</span></span>

### <span data-ttu-id="3cd82-108">예제 1: Stream Analytics 함수 테스트</span><span class="sxs-lookup"><span data-stu-id="3cd82-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="3cd82-109">이 명령은 StreamJob22라는 작업에서 ScoreTweet이라는 함수의 연결 상태를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd82-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="3cd82-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cd82-110">PARAMETERS</span></span>

### <span data-ttu-id="3cd82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd82-111">-DefaultProfile</span></span>
<span data-ttu-id="3cd82-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3cd82-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cd82-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="3cd82-113">-JobName</span></span>
<span data-ttu-id="3cd82-114">함수가 속한 Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd82-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

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

### <span data-ttu-id="3cd82-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3cd82-115">-Name</span></span>
<span data-ttu-id="3cd82-116">이 cmdlet에서 테스트하는 Stream Analytics 함수의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd82-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

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

### <span data-ttu-id="3cd82-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cd82-117">-ResourceGroupName</span></span>
<span data-ttu-id="3cd82-118">Stream Analytics 함수가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd82-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="3cd82-119">이 cmdlet은 이 매개 변수가 지정하는 리소스 그룹의 함수를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd82-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3cd82-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd82-120">CommonParameters</span></span>
<span data-ttu-id="3cd82-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3cd82-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd82-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3cd82-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd82-123">입력</span><span class="sxs-lookup"><span data-stu-id="3cd82-123">INPUTS</span></span>

### <span data-ttu-id="3cd82-124">System.String</span><span class="sxs-lookup"><span data-stu-id="3cd82-124">System.String</span></span>

## <span data-ttu-id="3cd82-125">출력</span><span class="sxs-lookup"><span data-stu-id="3cd82-125">OUTPUTS</span></span>

### <span data-ttu-id="3cd82-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3cd82-126">System.Boolean</span></span>

## <span data-ttu-id="3cd82-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3cd82-127">NOTES</span></span>

## <span data-ttu-id="3cd82-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3cd82-128">RELATED LINKS</span></span>

[<span data-ttu-id="3cd82-129">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3cd82-129">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="3cd82-130">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3cd82-130">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="3cd82-131">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3cd82-131">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)


