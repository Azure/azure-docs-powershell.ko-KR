---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Test-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: d0357e06257ad1df97b47ea7be59a1797e0f6902
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703084"
---
# <span data-ttu-id="f2ec0-101">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f2ec0-101">Test-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="f2ec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ec0-103">입력의 연결 상태를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2ec0-103">Tests the connection status of an input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2ec0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2ec0-104">SYNTAX</span></span>

```
Test-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2ec0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f2ec0-105">DESCRIPTION</span></span>
<span data-ttu-id="f2ec0-106">**AzureRmStreamAnalyticsInput** Cmdlet은 스트림 분석을 입력에 연결 하는 기능을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2ec0-106">The **Test-AzureRmStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="f2ec0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f2ec0-107">EXAMPLES</span></span>

### <span data-ttu-id="f2ec0-108">예제 1: 입력 스트림의 연결 상태 테스트</span><span class="sxs-lookup"><span data-stu-id="f2ec0-108">EXAMPLE 1: Test the connection status of an input stream</span></span>
```
PS C:\>Test-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="f2ec0-109">이는 StreamingJob에서 입력 EntryStream 연결 상태를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2ec0-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="f2ec0-110">변수</span><span class="sxs-lookup"><span data-stu-id="f2ec0-110">PARAMETERS</span></span>

### <span data-ttu-id="f2ec0-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="f2ec0-111">-JobName</span></span>
<span data-ttu-id="f2ec0-112">Azure Stream Analytics 입력이 속한 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2ec0-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="f2ec0-113">-이름</span><span class="sxs-lookup"><span data-stu-id="f2ec0-113">-Name</span></span>
<span data-ttu-id="f2ec0-114">테스트할 Azure Stream Analytics 입력의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2ec0-114">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="f2ec0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2ec0-115">-ResourceGroupName</span></span>
<span data-ttu-id="f2ec0-116">Azure Stream Analytics 입력이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2ec0-116">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="f2ec0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2ec0-117">-DefaultProfile</span></span>
<span data-ttu-id="f2ec0-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2ec0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2ec0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ec0-119">CommonParameters</span></span>
<span data-ttu-id="f2ec0-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2ec0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ec0-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2ec0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ec0-122">입력</span><span class="sxs-lookup"><span data-stu-id="f2ec0-122">INPUTS</span></span>

## <span data-ttu-id="f2ec0-123">출력</span><span class="sxs-lookup"><span data-stu-id="f2ec0-123">OUTPUTS</span></span>

### <span data-ttu-id="f2ec0-124">System. 개체</span><span class="sxs-lookup"><span data-stu-id="f2ec0-124">System.Object</span></span>

## <span data-ttu-id="f2ec0-125">상속자</span><span class="sxs-lookup"><span data-stu-id="f2ec0-125">NOTES</span></span>

## <span data-ttu-id="f2ec0-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2ec0-126">RELATED LINKS</span></span>

[<span data-ttu-id="f2ec0-127">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f2ec0-127">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="f2ec0-128">새로운 AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f2ec0-128">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="f2ec0-129">제거-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f2ec0-129">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)


