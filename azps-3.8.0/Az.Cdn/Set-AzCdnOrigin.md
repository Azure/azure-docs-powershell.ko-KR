---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 9635031d6eaea5a7920a6862fb8cf20ce536c1db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042832"
---
# <span data-ttu-id="ef63a-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="ef63a-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="ef63a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef63a-102">SYNOPSIS</span></span>
<span data-ttu-id="ef63a-103">CDN 원본 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef63a-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="ef63a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ef63a-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef63a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ef63a-105">DESCRIPTION</span></span>
<span data-ttu-id="ef63a-106">**AzCdnOrigin** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 원본 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef63a-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="ef63a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ef63a-107">EXAMPLES</span></span>

## <span data-ttu-id="ef63a-108">변수</span><span class="sxs-lookup"><span data-stu-id="ef63a-108">PARAMETERS</span></span>

### <span data-ttu-id="ef63a-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="ef63a-109">-CdnOrigin</span></span>
<span data-ttu-id="ef63a-110">이 cmdlet이 업데이트 하는 원본 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef63a-110">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="ef63a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef63a-111">-DefaultProfile</span></span>
<span data-ttu-id="ef63a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ef63a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef63a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef63a-113">CommonParameters</span></span>
<span data-ttu-id="ef63a-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef63a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef63a-115">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ef63a-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef63a-116">입력</span><span class="sxs-lookup"><span data-stu-id="ef63a-116">INPUTS</span></span>

### <span data-ttu-id="ef63a-117">Microsoft. Cdn. 원본 PSOrigin</span><span class="sxs-lookup"><span data-stu-id="ef63a-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="ef63a-118">출력</span><span class="sxs-lookup"><span data-stu-id="ef63a-118">OUTPUTS</span></span>

### <span data-ttu-id="ef63a-119">Microsoft. Cdn. 원본 PSOrigin</span><span class="sxs-lookup"><span data-stu-id="ef63a-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="ef63a-120">상속자</span><span class="sxs-lookup"><span data-stu-id="ef63a-120">NOTES</span></span>

## <span data-ttu-id="ef63a-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef63a-121">RELATED LINKS</span></span>

[<span data-ttu-id="ef63a-122">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="ef63a-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


