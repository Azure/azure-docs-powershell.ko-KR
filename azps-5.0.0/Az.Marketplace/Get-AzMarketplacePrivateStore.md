---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: fcd59eb37a518cc4f6cd0b5d1c580706d2f6e8bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218639"
---
# <span data-ttu-id="ba851-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="ba851-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="ba851-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba851-102">SYNOPSIS</span></span>
<span data-ttu-id="ba851-103">개인 스토어 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="ba851-103">Get private store list</span></span>

## <span data-ttu-id="ba851-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba851-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba851-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ba851-105">DESCRIPTION</span></span>
<span data-ttu-id="ba851-106">테 넌 트 범위 아래에 만들어진 개인 저장소 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="ba851-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="ba851-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ba851-107">EXAMPLES</span></span>

### <span data-ttu-id="ba851-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ba851-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="ba851-109">테 넌 트 범위 아래에 만들어진 개인 저장소 목록</span><span class="sxs-lookup"><span data-stu-id="ba851-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="ba851-110">변수</span><span class="sxs-lookup"><span data-stu-id="ba851-110">PARAMETERS</span></span>

### <span data-ttu-id="ba851-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba851-111">-DefaultProfile</span></span>
<span data-ttu-id="ba851-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba851-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba851-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba851-113">CommonParameters</span></span>
<span data-ttu-id="ba851-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba851-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba851-115">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba851-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba851-116">입력</span><span class="sxs-lookup"><span data-stu-id="ba851-116">INPUTS</span></span>

### <span data-ttu-id="ba851-117">않아야</span><span class="sxs-lookup"><span data-stu-id="ba851-117">None</span></span>

## <span data-ttu-id="ba851-118">출력</span><span class="sxs-lookup"><span data-stu-id="ba851-118">OUTPUTS</span></span>

### <span data-ttu-id="ba851-119">PrivateStore. PSPrivateStore에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="ba851-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="ba851-120">상속자</span><span class="sxs-lookup"><span data-stu-id="ba851-120">NOTES</span></span>

## <span data-ttu-id="ba851-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba851-121">RELATED LINKS</span></span>
