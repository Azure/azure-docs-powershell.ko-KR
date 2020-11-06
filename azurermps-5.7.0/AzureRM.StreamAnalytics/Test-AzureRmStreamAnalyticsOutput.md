---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 5e93638489749702a3da2608927318f794bc4a3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533548"
---
# <span data-ttu-id="0faa5-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0faa5-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="0faa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0faa5-102">SYNOPSIS</span></span>
<span data-ttu-id="0faa5-103">출력의 연결 상태를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0faa5-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0faa5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0faa5-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0faa5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0faa5-105">DESCRIPTION</span></span>
<span data-ttu-id="0faa5-106">**AzureRmStreamAnalyticsOutput** Cmdlet은 스트림 분석에서 출력에 연결 하는 기능을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0faa5-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="0faa5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0faa5-107">EXAMPLES</span></span>

### <span data-ttu-id="0faa5-108">예제 1: 출력의 연결 상태 테스트</span><span class="sxs-lookup"><span data-stu-id="0faa5-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="0faa5-109">이는 StreamingJob에서 출력 출력의 연결 상태를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0faa5-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="0faa5-110">변수</span><span class="sxs-lookup"><span data-stu-id="0faa5-110">PARAMETERS</span></span>

### <span data-ttu-id="0faa5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0faa5-111">-DefaultProfile</span></span>
<span data-ttu-id="0faa5-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0faa5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0faa5-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="0faa5-113">-JobName</span></span>
<span data-ttu-id="0faa5-114">원하는 Azure Stream Analytics 출력이 속한 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0faa5-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="0faa5-115">-이름</span><span class="sxs-lookup"><span data-stu-id="0faa5-115">-Name</span></span>
<span data-ttu-id="0faa5-116">테스트할 Azure Stream Analytics 출력의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0faa5-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="0faa5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0faa5-117">-ResourceGroupName</span></span>
<span data-ttu-id="0faa5-118">Azure Stream Analytics 출력이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0faa5-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="0faa5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0faa5-119">CommonParameters</span></span>
<span data-ttu-id="0faa5-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0faa5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0faa5-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0faa5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0faa5-122">입력</span><span class="sxs-lookup"><span data-stu-id="0faa5-122">INPUTS</span></span>

### <span data-ttu-id="0faa5-123">않아야</span><span class="sxs-lookup"><span data-stu-id="0faa5-123">None</span></span>
<span data-ttu-id="0faa5-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0faa5-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0faa5-125">출력</span><span class="sxs-lookup"><span data-stu-id="0faa5-125">OUTPUTS</span></span>

### <span data-ttu-id="0faa5-126">System. 개체</span><span class="sxs-lookup"><span data-stu-id="0faa5-126">System.Object</span></span>

## <span data-ttu-id="0faa5-127">상속자</span><span class="sxs-lookup"><span data-stu-id="0faa5-127">NOTES</span></span>

## <span data-ttu-id="0faa5-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0faa5-128">RELATED LINKS</span></span>

[<span data-ttu-id="0faa5-129">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0faa5-129">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="0faa5-130">새로운 AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0faa5-130">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="0faa5-131">제거-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0faa5-131">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


