---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: E711FBFF-FB6D-4DFD-BAE8-7961EB4FD16B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 29002234ac769ffd46aa3ca338e5ce61f0e3b848
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526507"
---
# <span data-ttu-id="3b4e2-101">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3b4e2-101">Test-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="3b4e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b4e2-102">SYNOPSIS</span></span>
<span data-ttu-id="3b4e2-103">스트림 분석에서 함수에 연결할 수 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b4e2-103">Tests whether Stream Analytics can connect to a function.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b4e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3b4e2-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b4e2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3b4e2-105">DESCRIPTION</span></span>
<span data-ttu-id="3b4e2-106">**테스트 AzureRmStreamAnalyticsFunction** Cmdlet은 Azure Stream Analytics가 함수에 연결할 수 있는지 여부를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b4e2-106">The **Test-AzureRmStreamAnalyticsFunction** cmdlet tests whether Azure Stream Analytics can connect to a function.</span></span>

## <span data-ttu-id="3b4e2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3b4e2-107">EXAMPLES</span></span>

### <span data-ttu-id="3b4e2-108">예제 1: Stream Analytics 함수 테스트</span><span class="sxs-lookup"><span data-stu-id="3b4e2-108">Example 1: Test a Stream Analytics function</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="3b4e2-109">이 명령은 StreamJob22 이라는 작업에서 ScoreTweet 이라는 함수의 연결 상태를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b4e2-109">This command tests the connection status of the function named ScoreTweet in the job named StreamJob22.</span></span>

## <span data-ttu-id="3b4e2-110">변수</span><span class="sxs-lookup"><span data-stu-id="3b4e2-110">PARAMETERS</span></span>

### <span data-ttu-id="3b4e2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b4e2-111">-DefaultProfile</span></span>
<span data-ttu-id="3b4e2-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3b4e2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b4e2-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="3b4e2-113">-JobName</span></span>
<span data-ttu-id="3b4e2-114">함수가 속한 Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b4e2-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b4e2-115">-이름</span><span class="sxs-lookup"><span data-stu-id="3b4e2-115">-Name</span></span>
<span data-ttu-id="3b4e2-116">이 cmdlet이 테스트 하는 Stream Analytics 함수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b4e2-116">Specifies the name of the Stream Analytics function that this cmdlet tests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b4e2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b4e2-117">-ResourceGroupName</span></span>
<span data-ttu-id="3b4e2-118">Stream Analytics 함수가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b4e2-118">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="3b4e2-119">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹의 함수를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b4e2-119">This cmdlet tests a function in the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b4e2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b4e2-120">CommonParameters</span></span>
<span data-ttu-id="3b4e2-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b4e2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b4e2-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b4e2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b4e2-123">입력</span><span class="sxs-lookup"><span data-stu-id="3b4e2-123">INPUTS</span></span>

### <span data-ttu-id="3b4e2-124">않아야</span><span class="sxs-lookup"><span data-stu-id="3b4e2-124">None</span></span>
<span data-ttu-id="3b4e2-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b4e2-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b4e2-126">출력</span><span class="sxs-lookup"><span data-stu-id="3b4e2-126">OUTPUTS</span></span>

### <span data-ttu-id="3b4e2-127">System. 개체</span><span class="sxs-lookup"><span data-stu-id="3b4e2-127">System.Object</span></span>

## <span data-ttu-id="3b4e2-128">상속자</span><span class="sxs-lookup"><span data-stu-id="3b4e2-128">NOTES</span></span>

## <span data-ttu-id="3b4e2-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b4e2-129">RELATED LINKS</span></span>

[<span data-ttu-id="3b4e2-130">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3b4e2-130">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="3b4e2-131">새로운 AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3b4e2-131">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="3b4e2-132">제거-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="3b4e2-132">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)


