---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: 281bc9cd39891ab2794901d0425b299cc72c4644
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524240"
---
# <span data-ttu-id="8a1f0-101">Get-AzureRmStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="8a1f0-101">Get-AzureRmStreamAnalyticsQuota</span></span>

## <span data-ttu-id="8a1f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a1f0-102">SYNOPSIS</span></span>
<span data-ttu-id="8a1f0-103">영역의 스트리밍 단위 할당량에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f0-103">Gets information about the Streaming Unit quota for a region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a1f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a1f0-104">SYNTAX</span></span>

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a1f0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8a1f0-105">DESCRIPTION</span></span>
<span data-ttu-id="8a1f0-106">**AzureRmStreamAnalyticsQuota** cmdlet은 지역에 대 한 스트리밍 단위 할당량에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f0-106">The **Get-AzureRmStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="8a1f0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8a1f0-107">EXAMPLES</span></span>

### <span data-ttu-id="8a1f0-108">예제 1: 지역에 대 한 스트리밍 단위 할당량에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="8a1f0-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="8a1f0-109">이 명령은 서쪽의 미국 지역에서 스트리밍 단위 할당량 및 사용량에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f0-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="8a1f0-110">변수</span><span class="sxs-lookup"><span data-stu-id="8a1f0-110">PARAMETERS</span></span>

### <span data-ttu-id="8a1f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a1f0-111">-DefaultProfile</span></span>
<span data-ttu-id="8a1f0-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a1f0-113">-위치</span><span class="sxs-lookup"><span data-stu-id="8a1f0-113">-Location</span></span>
<span data-ttu-id="8a1f0-114">스트리밍 단위 할당량 정보를 가져올 Azure region 또는 데이터 센터 위치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f0-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="8a1f0-115"> https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services지원 되는 Azure 지역 목록은를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8a1f0-115">See https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="8a1f0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a1f0-116">CommonParameters</span></span>
<span data-ttu-id="8a1f0-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a1f0-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a1f0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a1f0-119">입력</span><span class="sxs-lookup"><span data-stu-id="8a1f0-119">INPUTS</span></span>

### <span data-ttu-id="8a1f0-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8a1f0-120">System.String</span></span>

## <span data-ttu-id="8a1f0-121">출력</span><span class="sxs-lookup"><span data-stu-id="8a1f0-121">OUTPUTS</span></span>

### <span data-ttu-id="8a1f0-122">Microsoft. StreamAnalytics. PSQuota</span><span class="sxs-lookup"><span data-stu-id="8a1f0-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="8a1f0-123">상속자</span><span class="sxs-lookup"><span data-stu-id="8a1f0-123">NOTES</span></span>

## <span data-ttu-id="8a1f0-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a1f0-124">RELATED LINKS</span></span>

[<span data-ttu-id="8a1f0-125">Azure Stream Analytics Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8a1f0-125">Azure Stream Analytics Cmdlets</span></span>](./AzureRM.StreamAnalytics.md)


