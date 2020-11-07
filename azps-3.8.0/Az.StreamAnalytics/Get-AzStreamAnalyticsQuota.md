---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: abce6b39b0dfa77ed4aa815ed9551b3ebff427ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879717"
---
# <span data-ttu-id="8e22b-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="8e22b-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="8e22b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e22b-102">SYNOPSIS</span></span>
<span data-ttu-id="8e22b-103">영역의 스트리밍 단위 할당량에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8e22b-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="8e22b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e22b-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e22b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8e22b-105">DESCRIPTION</span></span>
<span data-ttu-id="8e22b-106">**AzStreamAnalyticsQuota** cmdlet은 지역에 대 한 스트리밍 단위 할당량에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8e22b-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="8e22b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8e22b-107">EXAMPLES</span></span>

### <span data-ttu-id="8e22b-108">예제 1: 지역에 대 한 스트리밍 단위 할당량에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="8e22b-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="8e22b-109">이 명령은 서쪽의 미국 지역에서 스트리밍 단위 할당량 및 사용량에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e22b-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="8e22b-110">변수</span><span class="sxs-lookup"><span data-stu-id="8e22b-110">PARAMETERS</span></span>

### <span data-ttu-id="8e22b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e22b-111">-DefaultProfile</span></span>
<span data-ttu-id="8e22b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e22b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e22b-113">-위치</span><span class="sxs-lookup"><span data-stu-id="8e22b-113">-Location</span></span>
<span data-ttu-id="8e22b-114">스트리밍 단위 할당량 정보를 가져올 Azure region 또는 데이터 센터 위치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e22b-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="8e22b-115"> http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services지원 되는 Azure 지역 목록은를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8e22b-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="8e22b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e22b-116">CommonParameters</span></span>
<span data-ttu-id="8e22b-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e22b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e22b-118">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e22b-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e22b-119">입력</span><span class="sxs-lookup"><span data-stu-id="8e22b-119">INPUTS</span></span>

### <span data-ttu-id="8e22b-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8e22b-120">System.String</span></span>

## <span data-ttu-id="8e22b-121">출력</span><span class="sxs-lookup"><span data-stu-id="8e22b-121">OUTPUTS</span></span>

### <span data-ttu-id="8e22b-122">Microsoft. StreamAnalytics. PSQuota</span><span class="sxs-lookup"><span data-stu-id="8e22b-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="8e22b-123">상속자</span><span class="sxs-lookup"><span data-stu-id="8e22b-123">NOTES</span></span>

## <span data-ttu-id="8e22b-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e22b-124">RELATED LINKS</span></span>

[<span data-ttu-id="8e22b-125">Azure Stream Analytics Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8e22b-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


