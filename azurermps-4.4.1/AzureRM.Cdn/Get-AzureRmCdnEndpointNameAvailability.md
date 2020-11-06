---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
ms.openlocfilehash: 6c5c11123ab39d92bb7b702542b007c8c075f9b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533156"
---
# <span data-ttu-id="d5daf-101">Get-AzureRmCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="d5daf-101">Get-AzureRmCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="d5daf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5daf-102">SYNOPSIS</span></span>
<span data-ttu-id="d5daf-103">CDN 끝점의 가용성 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d5daf-103">Gets availability status of the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5daf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5daf-104">SYNTAX</span></span>

```
Get-AzureRmCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5daf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d5daf-105">DESCRIPTION</span></span>
<span data-ttu-id="d5daf-106">**AzureRmCdnEndpointNameAvailability** CMDLET은 CDN (Azure Content Delivery Network) 끝점의 가용성 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d5daf-106">The **Get-AzureRmCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="d5daf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d5daf-107">EXAMPLES</span></span>

## <span data-ttu-id="d5daf-108">변수</span><span class="sxs-lookup"><span data-stu-id="d5daf-108">PARAMETERS</span></span>

### <span data-ttu-id="d5daf-109">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d5daf-109">-EndpointName</span></span>
<span data-ttu-id="d5daf-110">끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5daf-110">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="d5daf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5daf-111">-DefaultProfile</span></span>
<span data-ttu-id="d5daf-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5daf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5daf-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5daf-113">CommonParameters</span></span>
<span data-ttu-id="d5daf-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5daf-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5daf-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5daf-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5daf-116">입력</span><span class="sxs-lookup"><span data-stu-id="d5daf-116">INPUTS</span></span>

## <span data-ttu-id="d5daf-117">출력</span><span class="sxs-lookup"><span data-stu-id="d5daf-117">OUTPUTS</span></span>

### <span data-ttu-id="d5daf-118">PSCheckNameAvailabilityOutput를 통해 끝점을 보세요.</span><span class="sxs-lookup"><span data-stu-id="d5daf-118">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="d5daf-119">상속자</span><span class="sxs-lookup"><span data-stu-id="d5daf-119">NOTES</span></span>

## <span data-ttu-id="d5daf-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5daf-120">RELATED LINKS</span></span>

