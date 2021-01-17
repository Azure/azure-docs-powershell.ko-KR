---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: aef3bb0f5be7e354bbf1a4d7270cf0d7f8a1530f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366409"
---
# <span data-ttu-id="368e4-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="368e4-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="368e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="368e4-102">SYNOPSIS</span></span>
<span data-ttu-id="368e4-103">Stream Analytics 작업 변환에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="368e4-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="368e4-104">구문</span><span class="sxs-lookup"><span data-stu-id="368e4-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="368e4-105">설명</span><span class="sxs-lookup"><span data-stu-id="368e4-105">DESCRIPTION</span></span>
<span data-ttu-id="368e4-106">**Get-AzStreamAnalyticsTransformation** cmdlet은 Stream Analytics 작업에서 정의된 변환에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="368e4-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="368e4-107">예제</span><span class="sxs-lookup"><span data-stu-id="368e4-107">EXAMPLES</span></span>

### <span data-ttu-id="368e4-108">예제 1: Stream Analytics 변환에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="368e4-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="368e4-109">이 명령은 StreamingJob이라는 작업에서 StreamingJob이라는 변환에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="368e4-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="368e4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="368e4-110">PARAMETERS</span></span>

### <span data-ttu-id="368e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="368e4-111">-DefaultProfile</span></span>
<span data-ttu-id="368e4-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="368e4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="368e4-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="368e4-113">-JobName</span></span>
<span data-ttu-id="368e4-114">Azure Stream Analytics 변환이 속한 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="368e4-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="368e4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="368e4-115">-Name</span></span>
<span data-ttu-id="368e4-116">검색할 Azure Stream Analytics 변환의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="368e4-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="368e4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="368e4-117">-ResourceGroupName</span></span>
<span data-ttu-id="368e4-118">Azure Stream Analytics 변환이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="368e4-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="368e4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="368e4-119">CommonParameters</span></span>
<span data-ttu-id="368e4-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="368e4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="368e4-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="368e4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="368e4-122">입력</span><span class="sxs-lookup"><span data-stu-id="368e4-122">INPUTS</span></span>

### <span data-ttu-id="368e4-123">System.String</span><span class="sxs-lookup"><span data-stu-id="368e4-123">System.String</span></span>

## <span data-ttu-id="368e4-124">출력</span><span class="sxs-lookup"><span data-stu-id="368e4-124">OUTPUTS</span></span>

### <span data-ttu-id="368e4-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="368e4-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="368e4-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="368e4-126">NOTES</span></span>

## <span data-ttu-id="368e4-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="368e4-127">RELATED LINKS</span></span>

[<span data-ttu-id="368e4-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="368e4-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


