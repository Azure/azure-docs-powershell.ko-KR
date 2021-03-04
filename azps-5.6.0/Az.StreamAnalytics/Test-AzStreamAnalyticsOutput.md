---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 28a595b3e63a01439417ed07f6fd47c1cfc40a79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981963"
---
# <span data-ttu-id="0062e-101">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0062e-101">Test-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="0062e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0062e-102">SYNOPSIS</span></span>
<span data-ttu-id="0062e-103">출력의 연결 상태를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="0062e-103">Tests the connection status of an output.</span></span>

## <span data-ttu-id="0062e-104">구문</span><span class="sxs-lookup"><span data-stu-id="0062e-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0062e-105">설명</span><span class="sxs-lookup"><span data-stu-id="0062e-105">DESCRIPTION</span></span>
<span data-ttu-id="0062e-106">**Test-AzStreamAnalyticsOutput** cmdlet은 Stream Analytics에서 출력에 연결하는 기능을 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="0062e-106">The **Test-AzStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="0062e-107">예제</span><span class="sxs-lookup"><span data-stu-id="0062e-107">EXAMPLES</span></span>

### <span data-ttu-id="0062e-108">예제 1: 출력의 연결 상태 테스트</span><span class="sxs-lookup"><span data-stu-id="0062e-108">Example 1: Test the connection status of an output</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="0062e-109">이렇게 하여 StreamingJob의 출력 출력의 연결 상태를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="0062e-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="0062e-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0062e-110">PARAMETERS</span></span>

### <span data-ttu-id="0062e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0062e-111">-DefaultProfile</span></span>
<span data-ttu-id="0062e-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0062e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0062e-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="0062e-113">-JobName</span></span>
<span data-ttu-id="0062e-114">원하는 Azure Stream Analytics 출력이 속하는 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0062e-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="0062e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0062e-115">-Name</span></span>
<span data-ttu-id="0062e-116">테스트할 Azure Stream Analytics 출력의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0062e-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="0062e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0062e-117">-ResourceGroupName</span></span>
<span data-ttu-id="0062e-118">Azure Stream Analytics 출력이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0062e-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="0062e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0062e-119">CommonParameters</span></span>
<span data-ttu-id="0062e-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0062e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0062e-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0062e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0062e-122">입력</span><span class="sxs-lookup"><span data-stu-id="0062e-122">INPUTS</span></span>

### <span data-ttu-id="0062e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0062e-123">System.String</span></span>

## <span data-ttu-id="0062e-124">출력</span><span class="sxs-lookup"><span data-stu-id="0062e-124">OUTPUTS</span></span>

### <span data-ttu-id="0062e-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0062e-125">System.Boolean</span></span>

## <span data-ttu-id="0062e-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0062e-126">NOTES</span></span>

## <span data-ttu-id="0062e-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0062e-127">RELATED LINKS</span></span>

[<span data-ttu-id="0062e-128">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0062e-128">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="0062e-129">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0062e-129">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="0062e-130">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0062e-130">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)


