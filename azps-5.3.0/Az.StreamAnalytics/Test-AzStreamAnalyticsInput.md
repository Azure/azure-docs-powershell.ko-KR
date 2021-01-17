---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: e353e1e8be820c96f1eb1381274a8e245f542947
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384245"
---
# <span data-ttu-id="2c2f4-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2c2f4-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="2c2f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c2f4-102">SYNOPSIS</span></span>
<span data-ttu-id="2c2f4-103">입력의 연결 상태를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2f4-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="2c2f4-104">구문</span><span class="sxs-lookup"><span data-stu-id="2c2f4-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c2f4-105">설명</span><span class="sxs-lookup"><span data-stu-id="2c2f4-105">DESCRIPTION</span></span>
<span data-ttu-id="2c2f4-106">**Test-AzStreamAnalyticsInput** cmdlet은 Stream Analytics가 입력에 연결하는 기능을 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2f4-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="2c2f4-107">예제</span><span class="sxs-lookup"><span data-stu-id="2c2f4-107">EXAMPLES</span></span>

### <span data-ttu-id="2c2f4-108">예제 1: 입력 스트림의 연결 상태 테스트</span><span class="sxs-lookup"><span data-stu-id="2c2f4-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="2c2f4-109">StreamingJob에서 입력 EntryStream의 연결 상태를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2f4-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="2c2f4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c2f4-110">PARAMETERS</span></span>

### <span data-ttu-id="2c2f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c2f4-111">-DefaultProfile</span></span>
<span data-ttu-id="2c2f4-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c2f4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c2f4-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="2c2f4-113">-JobName</span></span>
<span data-ttu-id="2c2f4-114">Azure Stream Analytics 입력이 속한 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2f4-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="2c2f4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2c2f4-115">-Name</span></span>
<span data-ttu-id="2c2f4-116">테스트할 Azure Stream Analytics 입력의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2f4-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="2c2f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c2f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c2f4-118">Azure Stream Analytics 입력이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2f4-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="2c2f4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c2f4-119">CommonParameters</span></span>
<span data-ttu-id="2c2f4-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2c2f4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c2f4-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2c2f4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c2f4-122">입력</span><span class="sxs-lookup"><span data-stu-id="2c2f4-122">INPUTS</span></span>

### <span data-ttu-id="2c2f4-123">System.String</span><span class="sxs-lookup"><span data-stu-id="2c2f4-123">System.String</span></span>

## <span data-ttu-id="2c2f4-124">출력</span><span class="sxs-lookup"><span data-stu-id="2c2f4-124">OUTPUTS</span></span>

### <span data-ttu-id="2c2f4-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2c2f4-125">System.Boolean</span></span>

## <span data-ttu-id="2c2f4-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2c2f4-126">NOTES</span></span>

## <span data-ttu-id="2c2f4-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c2f4-127">RELATED LINKS</span></span>

[<span data-ttu-id="2c2f4-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2c2f4-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="2c2f4-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2c2f4-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="2c2f4-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="2c2f4-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


