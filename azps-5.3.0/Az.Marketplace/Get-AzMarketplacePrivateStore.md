---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: fcd59eb37a518cc4f6cd0b5d1c580706d2f6e8bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492806"
---
# <span data-ttu-id="1c063-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="1c063-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="1c063-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c063-102">SYNOPSIS</span></span>
<span data-ttu-id="1c063-103">개인 저장소 목록 다운로드</span><span class="sxs-lookup"><span data-stu-id="1c063-103">Get private store list</span></span>

## <span data-ttu-id="1c063-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c063-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c063-105">설명</span><span class="sxs-lookup"><span data-stu-id="1c063-105">DESCRIPTION</span></span>
<span data-ttu-id="1c063-106">테넌트 범위에서 만든 개인 저장소 목록 다운로드</span><span class="sxs-lookup"><span data-stu-id="1c063-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="1c063-107">예제</span><span class="sxs-lookup"><span data-stu-id="1c063-107">EXAMPLES</span></span>

### <span data-ttu-id="1c063-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1c063-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="1c063-109">테넌트 범위에서 만든 개인 저장소 목록</span><span class="sxs-lookup"><span data-stu-id="1c063-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="1c063-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c063-110">PARAMETERS</span></span>

### <span data-ttu-id="1c063-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c063-111">-DefaultProfile</span></span>
<span data-ttu-id="1c063-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c063-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c063-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c063-113">CommonParameters</span></span>
<span data-ttu-id="1c063-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c063-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c063-115">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c063-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c063-116">입력</span><span class="sxs-lookup"><span data-stu-id="1c063-116">INPUTS</span></span>

### <span data-ttu-id="1c063-117">없음</span><span class="sxs-lookup"><span data-stu-id="1c063-117">None</span></span>

## <span data-ttu-id="1c063-118">출력</span><span class="sxs-lookup"><span data-stu-id="1c063-118">OUTPUTS</span></span>

### <span data-ttu-id="1c063-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="1c063-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="1c063-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c063-120">NOTES</span></span>

## <span data-ttu-id="1c063-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c063-121">RELATED LINKS</span></span>
