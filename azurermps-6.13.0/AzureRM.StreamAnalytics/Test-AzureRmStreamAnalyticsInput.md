---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/test-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 6256fc57d4084a55b2288875b56c6c616b16f8b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535039"
---
# <span data-ttu-id="ce676-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ce676-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="ce676-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce676-102">SYNOPSIS</span></span>
<span data-ttu-id="ce676-103">입력의 연결 상태를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce676-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce676-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce676-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce676-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ce676-105">DESCRIPTION</span></span>
<span data-ttu-id="ce676-106">**AzureRmStreamAnalyticsInput** Cmdlet은 스트림 분석을 입력에 연결 하는 기능을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce676-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="ce676-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ce676-107">EXAMPLES</span></span>

### <span data-ttu-id="ce676-108">예제 1: 입력 스트림의 연결 상태 테스트</span><span class="sxs-lookup"><span data-stu-id="ce676-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="ce676-109">이는 StreamingJob에서 입력 EntryStream 연결 상태를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce676-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="ce676-110">변수</span><span class="sxs-lookup"><span data-stu-id="ce676-110">PARAMETERS</span></span>

### <span data-ttu-id="ce676-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce676-111">-DefaultProfile</span></span>
<span data-ttu-id="ce676-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce676-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce676-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="ce676-113">-JobName</span></span>
<span data-ttu-id="ce676-114">Azure Stream Analytics 입력이 속한 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce676-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="ce676-115">-이름</span><span class="sxs-lookup"><span data-stu-id="ce676-115">-Name</span></span>
<span data-ttu-id="ce676-116">테스트할 Azure Stream Analytics 입력의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce676-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="ce676-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce676-117">-ResourceGroupName</span></span>
<span data-ttu-id="ce676-118">Azure Stream Analytics 입력이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce676-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="ce676-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce676-119">CommonParameters</span></span>
<span data-ttu-id="ce676-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce676-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce676-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce676-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce676-122">입력</span><span class="sxs-lookup"><span data-stu-id="ce676-122">INPUTS</span></span>

### <span data-ttu-id="ce676-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ce676-123">System.String</span></span>

## <span data-ttu-id="ce676-124">출력</span><span class="sxs-lookup"><span data-stu-id="ce676-124">OUTPUTS</span></span>

### <span data-ttu-id="ce676-125">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ce676-125">System.Boolean</span></span>

## <span data-ttu-id="ce676-126">상속자</span><span class="sxs-lookup"><span data-stu-id="ce676-126">NOTES</span></span>

## <span data-ttu-id="ce676-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce676-127">RELATED LINKS</span></span>

[<span data-ttu-id="ce676-128">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ce676-128">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="ce676-129">새로운 AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ce676-129">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="ce676-130">제거-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ce676-130">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)


