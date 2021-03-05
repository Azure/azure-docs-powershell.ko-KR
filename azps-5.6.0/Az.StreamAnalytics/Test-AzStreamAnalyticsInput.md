---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: DEAC40AB-D90B-41D8-86AB-A66B60A908BD
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/test-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Test-AzStreamAnalyticsInput.md
ms.openlocfilehash: 09cf95f6fd7feb17053063952ae7110098353c86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002176"
---
# <span data-ttu-id="4577d-101">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4577d-101">Test-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="4577d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4577d-102">SYNOPSIS</span></span>
<span data-ttu-id="4577d-103">입력의 연결 상태를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="4577d-103">Tests the connection status of an input.</span></span>

## <span data-ttu-id="4577d-104">구문</span><span class="sxs-lookup"><span data-stu-id="4577d-104">SYNTAX</span></span>

```
Test-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4577d-105">설명</span><span class="sxs-lookup"><span data-stu-id="4577d-105">DESCRIPTION</span></span>
<span data-ttu-id="4577d-106">**Test-AzStreamAnalyticsInput** cmdlet은 Stream Analytics의 기능을 테스트하여 입력에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="4577d-106">The **Test-AzStreamAnalyticsInput** cmdlet tests the ability of Stream Analytics to connect to an input.</span></span>

## <span data-ttu-id="4577d-107">예제</span><span class="sxs-lookup"><span data-stu-id="4577d-107">EXAMPLES</span></span>

### <span data-ttu-id="4577d-108">예제 1: 입력 스트림의 연결 상태 테스트</span><span class="sxs-lookup"><span data-stu-id="4577d-108">Example 1: Test the connection status of an input stream</span></span>
```powershell
PS C:\>Test-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

<span data-ttu-id="4577d-109">이 테스트는 StreamingJob의 Input EntryStream의 연결 상태를 테스트합니다.</span><span class="sxs-lookup"><span data-stu-id="4577d-109">This tests the connection status of the input EntryStream in StreamingJob.</span></span>

## <span data-ttu-id="4577d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4577d-110">PARAMETERS</span></span>

### <span data-ttu-id="4577d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4577d-111">-DefaultProfile</span></span>
<span data-ttu-id="4577d-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4577d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4577d-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="4577d-113">-JobName</span></span>
<span data-ttu-id="4577d-114">Azure Stream Analytics 입력이 속한 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4577d-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="4577d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4577d-115">-Name</span></span>
<span data-ttu-id="4577d-116">테스트할 Azure Stream Analytics 입력의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4577d-116">Specifies the name of the Azure Stream Analytics input to test.</span></span>

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

### <span data-ttu-id="4577d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4577d-117">-ResourceGroupName</span></span>
<span data-ttu-id="4577d-118">Azure Stream Analytics 입력이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4577d-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="4577d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4577d-119">CommonParameters</span></span>
<span data-ttu-id="4577d-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4577d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4577d-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4577d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4577d-122">입력</span><span class="sxs-lookup"><span data-stu-id="4577d-122">INPUTS</span></span>

### <span data-ttu-id="4577d-123">System.String</span><span class="sxs-lookup"><span data-stu-id="4577d-123">System.String</span></span>

## <span data-ttu-id="4577d-124">출력</span><span class="sxs-lookup"><span data-stu-id="4577d-124">OUTPUTS</span></span>

### <span data-ttu-id="4577d-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4577d-125">System.Boolean</span></span>

## <span data-ttu-id="4577d-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4577d-126">NOTES</span></span>

## <span data-ttu-id="4577d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4577d-127">RELATED LINKS</span></span>

[<span data-ttu-id="4577d-128">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4577d-128">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="4577d-129">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4577d-129">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="4577d-130">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4577d-130">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)


