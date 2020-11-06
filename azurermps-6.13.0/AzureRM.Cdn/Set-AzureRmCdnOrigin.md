---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnOrigin.md
ms.openlocfilehash: 395ee4b20ae2c26d05ad66489b3c643d0f4245a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531420"
---
# <span data-ttu-id="ac5e8-101">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="ac5e8-101">Set-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="ac5e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac5e8-102">SYNOPSIS</span></span>
<span data-ttu-id="ac5e8-103">CDN 원본 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac5e8-103">Updates a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac5e8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ac5e8-104">SYNTAX</span></span>

```
Set-AzureRmCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac5e8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ac5e8-105">DESCRIPTION</span></span>
<span data-ttu-id="ac5e8-106">**AzureRmCdnOrigin** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 원본 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac5e8-106">The **Set-AzureRmCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="ac5e8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ac5e8-107">EXAMPLES</span></span>

## <span data-ttu-id="ac5e8-108">변수</span><span class="sxs-lookup"><span data-stu-id="ac5e8-108">PARAMETERS</span></span>

### <span data-ttu-id="ac5e8-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="ac5e8-109">-CdnOrigin</span></span>
<span data-ttu-id="ac5e8-110">이 cmdlet이 업데이트 하는 원본 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac5e8-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac5e8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac5e8-111">-DefaultProfile</span></span>
<span data-ttu-id="ac5e8-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ac5e8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac5e8-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac5e8-113">CommonParameters</span></span>
<span data-ttu-id="ac5e8-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac5e8-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac5e8-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac5e8-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac5e8-116">입력</span><span class="sxs-lookup"><span data-stu-id="ac5e8-116">INPUTS</span></span>

### <span data-ttu-id="ac5e8-117">Microsoft. Cdn. 원본 PSOrigin</span><span class="sxs-lookup"><span data-stu-id="ac5e8-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>
<span data-ttu-id="ac5e8-118">매개 변수: CdnOrigin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ac5e8-118">Parameters: CdnOrigin (ByValue)</span></span>

## <span data-ttu-id="ac5e8-119">출력</span><span class="sxs-lookup"><span data-stu-id="ac5e8-119">OUTPUTS</span></span>

### <span data-ttu-id="ac5e8-120">Microsoft. Cdn. 원본 PSOrigin</span><span class="sxs-lookup"><span data-stu-id="ac5e8-120">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="ac5e8-121">상속자</span><span class="sxs-lookup"><span data-stu-id="ac5e8-121">NOTES</span></span>

## <span data-ttu-id="ac5e8-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac5e8-122">RELATED LINKS</span></span>

[<span data-ttu-id="ac5e8-123">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="ac5e8-123">Get-AzureRmCdnOrigin</span></span>](./Get-AzureRmCdnOrigin.md)


