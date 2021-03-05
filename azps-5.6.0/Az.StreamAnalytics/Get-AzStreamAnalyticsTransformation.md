---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 0c009ed05b475e466ab0b2c0dd7c6f18e70c2f9d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973840"
---
# <span data-ttu-id="19dfd-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="19dfd-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="19dfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="19dfd-103">Stream Analytics 작업 변환에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19dfd-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="19dfd-104">구문</span><span class="sxs-lookup"><span data-stu-id="19dfd-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19dfd-105">설명</span><span class="sxs-lookup"><span data-stu-id="19dfd-105">DESCRIPTION</span></span>
<span data-ttu-id="19dfd-106">**Get-AzStreamAnalyticsTransformation** cmdlet은 Stream Analytics 작업에서 정의된 변환에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19dfd-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="19dfd-107">예제</span><span class="sxs-lookup"><span data-stu-id="19dfd-107">EXAMPLES</span></span>

### <span data-ttu-id="19dfd-108">예제 1: Stream Analytics 변환에 대한 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="19dfd-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="19dfd-109">이 명령은 StreamingJob이라는 작업에서 StreamingJob이라는 변환에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="19dfd-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="19dfd-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="19dfd-110">PARAMETERS</span></span>

### <span data-ttu-id="19dfd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19dfd-111">-DefaultProfile</span></span>
<span data-ttu-id="19dfd-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19dfd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19dfd-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="19dfd-113">-JobName</span></span>
<span data-ttu-id="19dfd-114">Azure Stream Analytics 변환이 속한 Azure Stream Analytics 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19dfd-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="19dfd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="19dfd-115">-Name</span></span>
<span data-ttu-id="19dfd-116">검색할 Azure Stream Analytics 변환의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19dfd-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="19dfd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19dfd-117">-ResourceGroupName</span></span>
<span data-ttu-id="19dfd-118">Azure Stream Analytics 변환이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19dfd-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="19dfd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19dfd-119">CommonParameters</span></span>
<span data-ttu-id="19dfd-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="19dfd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19dfd-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="19dfd-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19dfd-122">입력</span><span class="sxs-lookup"><span data-stu-id="19dfd-122">INPUTS</span></span>

### <span data-ttu-id="19dfd-123">System.String</span><span class="sxs-lookup"><span data-stu-id="19dfd-123">System.String</span></span>

## <span data-ttu-id="19dfd-124">출력</span><span class="sxs-lookup"><span data-stu-id="19dfd-124">OUTPUTS</span></span>

### <span data-ttu-id="19dfd-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="19dfd-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="19dfd-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="19dfd-126">NOTES</span></span>

## <span data-ttu-id="19dfd-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19dfd-127">RELATED LINKS</span></span>

[<span data-ttu-id="19dfd-128">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="19dfd-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


