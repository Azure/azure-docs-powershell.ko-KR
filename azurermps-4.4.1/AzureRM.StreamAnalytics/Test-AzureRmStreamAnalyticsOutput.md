---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 5c961289267b0680a88cd16d58574c906a9f4408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532201"
---
# <span data-ttu-id="0b286-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0b286-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="0b286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b286-102">SYNOPSIS</span></span>
<span data-ttu-id="0b286-103">출력의 연결 상태를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b286-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b286-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0b286-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b286-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0b286-105">DESCRIPTION</span></span>
<span data-ttu-id="0b286-106">**AzureRmStreamAnalyticsOutput** Cmdlet은 스트림 분석에서 출력에 연결 하는 기능을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b286-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="0b286-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0b286-107">EXAMPLES</span></span>

### <span data-ttu-id="0b286-108">예제 1: 출력의 연결 상태 테스트</span><span class="sxs-lookup"><span data-stu-id="0b286-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="0b286-109">이는 StreamingJob에서 출력 출력의 연결 상태를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b286-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="0b286-110">변수</span><span class="sxs-lookup"><span data-stu-id="0b286-110">PARAMETERS</span></span>

### <span data-ttu-id="0b286-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="0b286-111">-JobName</span></span>
<span data-ttu-id="0b286-112">원하는 Azure Stream Analytics 출력이 속한 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b286-112">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="0b286-113">-이름</span><span class="sxs-lookup"><span data-stu-id="0b286-113">-Name</span></span>
<span data-ttu-id="0b286-114">테스트할 Azure Stream Analytics 출력의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b286-114">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="0b286-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b286-115">-ResourceGroupName</span></span>
<span data-ttu-id="0b286-116">Azure Stream Analytics 출력이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b286-116">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="0b286-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b286-117">-DefaultProfile</span></span>
<span data-ttu-id="0b286-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b286-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b286-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b286-119">CommonParameters</span></span>
<span data-ttu-id="0b286-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b286-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b286-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b286-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b286-122">입력</span><span class="sxs-lookup"><span data-stu-id="0b286-122">INPUTS</span></span>

## <span data-ttu-id="0b286-123">출력</span><span class="sxs-lookup"><span data-stu-id="0b286-123">OUTPUTS</span></span>

### <span data-ttu-id="0b286-124">System. 개체</span><span class="sxs-lookup"><span data-stu-id="0b286-124">System.Object</span></span>

## <span data-ttu-id="0b286-125">상속자</span><span class="sxs-lookup"><span data-stu-id="0b286-125">NOTES</span></span>

## <span data-ttu-id="0b286-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b286-126">RELATED LINKS</span></span>

[<span data-ttu-id="0b286-127">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0b286-127">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="0b286-128">새로운 AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0b286-128">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="0b286-129">제거-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0b286-129">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


