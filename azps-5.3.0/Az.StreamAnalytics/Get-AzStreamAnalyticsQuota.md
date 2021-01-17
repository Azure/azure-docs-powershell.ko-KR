---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/get-azstreamanalyticsquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Get-AzStreamAnalyticsQuota.md
ms.openlocfilehash: abce6b39b0dfa77ed4aa815ed9551b3ebff427ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384350"
---
# <span data-ttu-id="661d8-101">Get-AzStreamAnalyticsQuota</span><span class="sxs-lookup"><span data-stu-id="661d8-101">Get-AzStreamAnalyticsQuota</span></span>

## <span data-ttu-id="661d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="661d8-102">SYNOPSIS</span></span>
<span data-ttu-id="661d8-103">지역에 대한 스트리밍 단위 할당량에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="661d8-103">Gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="661d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="661d8-104">SYNTAX</span></span>

```
Get-AzStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="661d8-105">설명</span><span class="sxs-lookup"><span data-stu-id="661d8-105">DESCRIPTION</span></span>
<span data-ttu-id="661d8-106">**Get-AzStreamAnalyticsQuota** cmdlet은 지역에 대한 스트리밍 단위 할당량에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="661d8-106">The **Get-AzStreamAnalyticsQuota** cmdlet gets information about the Streaming Unit quota for a region.</span></span>

## <span data-ttu-id="661d8-107">예제</span><span class="sxs-lookup"><span data-stu-id="661d8-107">EXAMPLES</span></span>

### <span data-ttu-id="661d8-108">예제 1: 지역에 대한 스트리밍 단위 할당량에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="661d8-108">EXAMPLE 1: Get information about the Streaming Unit quota for a region</span></span>
```
PS C:\>Get-AzStreamAnalyticsQuota -Location "West US"
```

<span data-ttu-id="661d8-109">이 명령은 미국 서부 지역의 스트리밍 단위 할당량 및 사용량에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="661d8-109">This command returns information about Streaming Unit quota and usage in the West US region.</span></span>

## <span data-ttu-id="661d8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="661d8-110">PARAMETERS</span></span>

### <span data-ttu-id="661d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="661d8-111">-DefaultProfile</span></span>
<span data-ttu-id="661d8-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="661d8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="661d8-113">-Location</span><span class="sxs-lookup"><span data-stu-id="661d8-113">-Location</span></span>
<span data-ttu-id="661d8-114">스트리밍 단위 할당량 정보를 얻을 Azure 지역 또는 데이터 센터 위치의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="661d8-114">Specifies the name of an Azure region or data center location for which to get Streaming Unit quota information.</span></span>
<span data-ttu-id="661d8-115">지원되는 http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services Azure 지역 목록을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="661d8-115">See http://azure.microsoft.com/en-us/regions/#serviceshttp://azure.microsoft.com/en-us/regions/#services for a list of supported Azure regions.</span></span>

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

### <span data-ttu-id="661d8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="661d8-116">CommonParameters</span></span>
<span data-ttu-id="661d8-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="661d8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="661d8-118">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="661d8-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="661d8-119">입력</span><span class="sxs-lookup"><span data-stu-id="661d8-119">INPUTS</span></span>

### <span data-ttu-id="661d8-120">System.String</span><span class="sxs-lookup"><span data-stu-id="661d8-120">System.String</span></span>

## <span data-ttu-id="661d8-121">출력</span><span class="sxs-lookup"><span data-stu-id="661d8-121">OUTPUTS</span></span>

### <span data-ttu-id="661d8-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span><span class="sxs-lookup"><span data-stu-id="661d8-122">Microsoft.Azure.Commands.StreamAnalytics.Models.PSQuota</span></span>

## <span data-ttu-id="661d8-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="661d8-123">NOTES</span></span>

## <span data-ttu-id="661d8-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="661d8-124">RELATED LINKS</span></span>

[<span data-ttu-id="661d8-125">Azure Stream Analytics Cmdlet</span><span class="sxs-lookup"><span data-stu-id="661d8-125">Azure Stream Analytics Cmdlets</span></span>](./Az.StreamAnalytics.md)


