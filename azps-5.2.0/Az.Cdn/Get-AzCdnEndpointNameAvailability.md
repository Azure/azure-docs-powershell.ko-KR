---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350277"
---
# <span data-ttu-id="768a4-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="768a4-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="768a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="768a4-102">SYNOPSIS</span></span>
<span data-ttu-id="768a4-103">CDN 엔드포인트의 가용성 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="768a4-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="768a4-104">구문</span><span class="sxs-lookup"><span data-stu-id="768a4-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="768a4-105">설명</span><span class="sxs-lookup"><span data-stu-id="768a4-105">DESCRIPTION</span></span>
<span data-ttu-id="768a4-106">**Get-AzCdnEndpointNameAvailability** cmdlet은 Azure CDN(Content Delivery Network) 엔드포인트의 가용성 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="768a4-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="768a4-107">예제</span><span class="sxs-lookup"><span data-stu-id="768a4-107">EXAMPLES</span></span>

## <span data-ttu-id="768a4-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="768a4-108">PARAMETERS</span></span>

### <span data-ttu-id="768a4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="768a4-109">-DefaultProfile</span></span>
<span data-ttu-id="768a4-110">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="768a4-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="768a4-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="768a4-111">-EndpointName</span></span>
<span data-ttu-id="768a4-112">엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="768a4-112">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="768a4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="768a4-113">CommonParameters</span></span>
<span data-ttu-id="768a4-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="768a4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="768a4-115">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="768a4-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="768a4-116">입력</span><span class="sxs-lookup"><span data-stu-id="768a4-116">INPUTS</span></span>

### <span data-ttu-id="768a4-117">없음</span><span class="sxs-lookup"><span data-stu-id="768a4-117">None</span></span>

## <span data-ttu-id="768a4-118">출력</span><span class="sxs-lookup"><span data-stu-id="768a4-118">OUTPUTS</span></span>

### <span data-ttu-id="768a4-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="768a4-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="768a4-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="768a4-120">NOTES</span></span>

## <span data-ttu-id="768a4-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="768a4-121">RELATED LINKS</span></span>
