---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
ms.openlocfilehash: bf202a971497a9c43f7ed3731b7c53bc12e58d73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527031"
---
# <span data-ttu-id="d640a-101">Get-AzureRmCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="d640a-101">Get-AzureRmCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="d640a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d640a-102">SYNOPSIS</span></span>
<span data-ttu-id="d640a-103">CDN 끝점의 가용성 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d640a-103">Gets availability status of the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d640a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d640a-104">SYNTAX</span></span>

```
Get-AzureRmCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d640a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d640a-105">DESCRIPTION</span></span>
<span data-ttu-id="d640a-106">**AzureRmCdnEndpointNameAvailability** CMDLET은 CDN (Azure Content Delivery Network) 끝점의 가용성 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d640a-106">The **Get-AzureRmCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="d640a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d640a-107">EXAMPLES</span></span>

## <span data-ttu-id="d640a-108">변수</span><span class="sxs-lookup"><span data-stu-id="d640a-108">PARAMETERS</span></span>

### <span data-ttu-id="d640a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d640a-109">-DefaultProfile</span></span>
<span data-ttu-id="d640a-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d640a-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d640a-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d640a-111">-EndpointName</span></span>
<span data-ttu-id="d640a-112">끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d640a-112">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d640a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d640a-113">CommonParameters</span></span>
<span data-ttu-id="d640a-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d640a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d640a-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d640a-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d640a-116">입력</span><span class="sxs-lookup"><span data-stu-id="d640a-116">INPUTS</span></span>

### <span data-ttu-id="d640a-117">않아야</span><span class="sxs-lookup"><span data-stu-id="d640a-117">None</span></span>
<span data-ttu-id="d640a-118">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d640a-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d640a-119">출력</span><span class="sxs-lookup"><span data-stu-id="d640a-119">OUTPUTS</span></span>

### <span data-ttu-id="d640a-120">PSCheckNameAvailabilityOutput를 통해 끝점을 보세요.</span><span class="sxs-lookup"><span data-stu-id="d640a-120">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="d640a-121">상속자</span><span class="sxs-lookup"><span data-stu-id="d640a-121">NOTES</span></span>

## <span data-ttu-id="d640a-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d640a-122">RELATED LINKS</span></span>

