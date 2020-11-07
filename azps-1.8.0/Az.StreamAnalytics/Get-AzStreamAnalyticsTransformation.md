---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 34E1CC9E-9F81-4DA6-A777-D816B09BDE1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: ce933affbe3b99854f1ce907c968f35645c1d777
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698457"
---
# <span data-ttu-id="0fc57-101">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="0fc57-101">Get-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="0fc57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fc57-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc57-103">스트림 분석 작업 변환에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0fc57-103">Gets information about a Stream Analytics job transformation.</span></span>

## <span data-ttu-id="0fc57-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0fc57-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsTransformation [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fc57-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0fc57-105">DESCRIPTION</span></span>
<span data-ttu-id="0fc57-106">**AzStreamAnalyticsTransformation** Cmdlet은 Stream Analytics 작업에 정의 된 변환에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0fc57-106">The **Get-AzStreamAnalyticsTransformation** cmdlet gets information about a transformation defined on a Stream Analytics job.</span></span>

## <span data-ttu-id="0fc57-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0fc57-107">EXAMPLES</span></span>

### <span data-ttu-id="0fc57-108">예제 1: Stream Analytics 변환에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="0fc57-108">EXAMPLE 1: Get information about a Stream Analytics transformation</span></span>
```
PS C:\>Get-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "StreamingJob"
```

<span data-ttu-id="0fc57-109">이 명령은 StreamingJob 이라는 작업의 StreamingJob 이라는 변형에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc57-109">This command returns information about the transformation called StreamingJob on the job called StreamingJob.</span></span>

## <span data-ttu-id="0fc57-110">변수</span><span class="sxs-lookup"><span data-stu-id="0fc57-110">PARAMETERS</span></span>

### <span data-ttu-id="0fc57-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc57-111">-DefaultProfile</span></span>
<span data-ttu-id="0fc57-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc57-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fc57-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="0fc57-113">-JobName</span></span>
<span data-ttu-id="0fc57-114">Azure Stream Analytics 변환이 속한 Azure Stream Analytics 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc57-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="0fc57-115">-이름</span><span class="sxs-lookup"><span data-stu-id="0fc57-115">-Name</span></span>
<span data-ttu-id="0fc57-116">검색할 Azure Stream Analytics 변환의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc57-116">Specifies the name of the Azure Stream Analytics transformation to retrieve.</span></span>

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

### <span data-ttu-id="0fc57-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fc57-117">-ResourceGroupName</span></span>
<span data-ttu-id="0fc57-118">Azure Stream Analytics 변환이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc57-118">Specifies the name of the resource group to which the Azure Stream Analytics transformation belongs.</span></span>

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

### <span data-ttu-id="0fc57-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc57-119">CommonParameters</span></span>
<span data-ttu-id="0fc57-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc57-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc57-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fc57-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc57-122">입력</span><span class="sxs-lookup"><span data-stu-id="0fc57-122">INPUTS</span></span>

### <span data-ttu-id="0fc57-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0fc57-123">System.String</span></span>

## <span data-ttu-id="0fc57-124">출력</span><span class="sxs-lookup"><span data-stu-id="0fc57-124">OUTPUTS</span></span>

### <span data-ttu-id="0fc57-125">PSTransformation를 통한 명령.</span><span class="sxs-lookup"><span data-stu-id="0fc57-125">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="0fc57-126">상속자</span><span class="sxs-lookup"><span data-stu-id="0fc57-126">NOTES</span></span>

## <span data-ttu-id="0fc57-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0fc57-127">RELATED LINKS</span></span>

[<span data-ttu-id="0fc57-128">새로운 AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="0fc57-128">New-AzStreamAnalyticsTransformation</span></span>](./New-AzStreamAnalyticsTransformation.md)


