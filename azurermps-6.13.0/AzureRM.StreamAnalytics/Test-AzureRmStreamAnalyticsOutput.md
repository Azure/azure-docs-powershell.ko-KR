---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F57C53E2-2873-441F-90E6-E6100418D519
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: f8bd4feab9bdcf99daf713d3a584a574f699a8b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525955"
---
# <span data-ttu-id="1d691-101">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="1d691-101">Test-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="1d691-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d691-102">SYNOPSIS</span></span>
<span data-ttu-id="1d691-103">출력의 연결 상태를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d691-103">Tests the connection status of an output.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d691-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1d691-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d691-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1d691-105">DESCRIPTION</span></span>
<span data-ttu-id="1d691-106">**AzureRmStreamAnalyticsOutput** Cmdlet은 스트림 분석에서 출력에 연결 하는 기능을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d691-106">The **Test-AzureRmStreamAnalyticsOutput** cmdlet tests the ability of Stream Analytics to connect to an output.</span></span>

## <span data-ttu-id="1d691-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1d691-107">EXAMPLES</span></span>

### <span data-ttu-id="1d691-108">예제 1: 출력의 연결 상태 테스트</span><span class="sxs-lookup"><span data-stu-id="1d691-108">EXAMPLE 1: Test the connection status of an output</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="1d691-109">이는 StreamingJob에서 출력 출력의 연결 상태를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d691-109">This tests the connection status of the output Output in StreamingJob.</span></span>

## <span data-ttu-id="1d691-110">변수</span><span class="sxs-lookup"><span data-stu-id="1d691-110">PARAMETERS</span></span>

### <span data-ttu-id="1d691-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d691-111">-DefaultProfile</span></span>
<span data-ttu-id="1d691-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d691-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d691-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="1d691-113">-JobName</span></span>
<span data-ttu-id="1d691-114">원하는 Azure Stream Analytics 출력이 속한 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d691-114">Specifies the name of the Azure Stream Analytics job to which the desired Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="1d691-115">-이름</span><span class="sxs-lookup"><span data-stu-id="1d691-115">-Name</span></span>
<span data-ttu-id="1d691-116">테스트할 Azure Stream Analytics 출력의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d691-116">Specifies the name of the Azure Stream Analytics output to test.</span></span>

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

### <span data-ttu-id="1d691-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d691-117">-ResourceGroupName</span></span>
<span data-ttu-id="1d691-118">Azure Stream Analytics 출력이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d691-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="1d691-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d691-119">CommonParameters</span></span>
<span data-ttu-id="1d691-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d691-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d691-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d691-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d691-122">입력</span><span class="sxs-lookup"><span data-stu-id="1d691-122">INPUTS</span></span>

### <span data-ttu-id="1d691-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1d691-123">System.String</span></span>

## <span data-ttu-id="1d691-124">출력</span><span class="sxs-lookup"><span data-stu-id="1d691-124">OUTPUTS</span></span>

### <span data-ttu-id="1d691-125">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1d691-125">System.Boolean</span></span>

## <span data-ttu-id="1d691-126">상속자</span><span class="sxs-lookup"><span data-stu-id="1d691-126">NOTES</span></span>

## <span data-ttu-id="1d691-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d691-127">RELATED LINKS</span></span>

[<span data-ttu-id="1d691-128">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="1d691-128">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="1d691-129">새로운 AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="1d691-129">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="1d691-130">제거-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="1d691-130">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)


