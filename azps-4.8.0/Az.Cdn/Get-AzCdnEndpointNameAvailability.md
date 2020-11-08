---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204670"
---
# <span data-ttu-id="8e678-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="8e678-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="8e678-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e678-102">SYNOPSIS</span></span>
<span data-ttu-id="8e678-103">CDN 끝점의 가용성 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8e678-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="8e678-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e678-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e678-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8e678-105">DESCRIPTION</span></span>
<span data-ttu-id="8e678-106">**AzCdnEndpointNameAvailability** CMDLET은 CDN (Azure Content Delivery Network) 끝점의 가용성 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8e678-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="8e678-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8e678-107">EXAMPLES</span></span>

## <span data-ttu-id="8e678-108">변수</span><span class="sxs-lookup"><span data-stu-id="8e678-108">PARAMETERS</span></span>

### <span data-ttu-id="8e678-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e678-109">-DefaultProfile</span></span>
<span data-ttu-id="8e678-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8e678-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e678-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8e678-111">-EndpointName</span></span>
<span data-ttu-id="8e678-112">끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e678-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="8e678-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e678-113">CommonParameters</span></span>
<span data-ttu-id="8e678-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e678-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e678-115">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8e678-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e678-116">입력</span><span class="sxs-lookup"><span data-stu-id="8e678-116">INPUTS</span></span>

### <span data-ttu-id="8e678-117">않아야</span><span class="sxs-lookup"><span data-stu-id="8e678-117">None</span></span>

## <span data-ttu-id="8e678-118">출력</span><span class="sxs-lookup"><span data-stu-id="8e678-118">OUTPUTS</span></span>

### <span data-ttu-id="8e678-119">PSCheckNameAvailabilityOutput를 통해 끝점을 보세요.</span><span class="sxs-lookup"><span data-stu-id="8e678-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="8e678-120">상속자</span><span class="sxs-lookup"><span data-stu-id="8e678-120">NOTES</span></span>

## <span data-ttu-id="8e678-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e678-121">RELATED LINKS</span></span>
