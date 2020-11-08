---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: e353e1e8be820c96f1eb1381274a8e245f542947
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056863"
---
# <span data-ttu-id="8245d-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="8245d-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="8245d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8245d-102">SYNOPSIS</span></span>
<span data-ttu-id="8245d-103">입력의 연결 상태를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8245d-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="8245d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8245d-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8245d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8245d-105">DESCRIPTION</span></span>
<span data-ttu-id="8245d-106">**AzStreamAnalyticsInput** Cmdlet은 스트림 분석을 입력에 연결 하는 기능을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8245d-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="8245d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8245d-107">EXAMPLES</span></span>

### <span data-ttu-id="8245d-108">예제 1: 입력 스트림의 연결 상태 테스트</span><span class="sxs-lookup"><span data-stu-id="8245d-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="8245d-109">이는 StreamingJob에서 입력 EntryStream 연결 상태를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8245d-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="8245d-110">변수</span><span class="sxs-lookup"><span data-stu-id="8245d-110">PARAMETERS</span></span>

### <span data-ttu-id="8245d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8245d-111">-DefaultProfile</span></span>
<span data-ttu-id="8245d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8245d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8245d-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="8245d-113">-JobName</span></span>
<span data-ttu-id="8245d-114">Azure Stream Analytics 입력이 속한 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8245d-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="8245d-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8245d-115">-Name</span></span>
<span data-ttu-id="8245d-116">테스트할 Azure Stream Analytics 입력의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8245d-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="8245d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8245d-117">-ResourceGroupName</span></span>
<span data-ttu-id="8245d-118">Azure Stream Analytics 입력이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8245d-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="8245d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8245d-119">CommonParameters</span></span>
<span data-ttu-id="8245d-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8245d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8245d-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8245d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8245d-122">입력</span><span class="sxs-lookup"><span data-stu-id="8245d-122">INPUTS</span></span>

### <span data-ttu-id="8245d-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8245d-123">System.String</span></span>

## <span data-ttu-id="8245d-124">출력</span><span class="sxs-lookup"><span data-stu-id="8245d-124">OUTPUTS</span></span>

### <span data-ttu-id="8245d-125">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8245d-125">System.Boolean</span></span>

## <span data-ttu-id="8245d-126">상속자</span><span class="sxs-lookup"><span data-stu-id="8245d-126">NOTES</span></span>

## <span data-ttu-id="8245d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8245d-127">RELATED LINKS</span></span>

[<span data-ttu-id="8245d-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="8245d-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="8245d-129">새로운 AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="8245d-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="8245d-130">제거-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="8245d-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


