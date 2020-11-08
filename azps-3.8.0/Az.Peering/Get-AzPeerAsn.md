---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: 559d2d8c069d7e36630600d0fcdc16ea475da9f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044491"
---
# <span data-ttu-id="659af-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="659af-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="659af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="659af-102">SYNOPSIS</span></span>
<span data-ttu-id="659af-103">ARM에서 PeerAsn 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="659af-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="659af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="659af-104">SYNTAX</span></span>

```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="659af-105">설명은</span><span class="sxs-lookup"><span data-stu-id="659af-105">DESCRIPTION</span></span>
<span data-ttu-id="659af-106">구독에 대 한 PeerAsn을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="659af-106">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="659af-107">예제의</span><span class="sxs-lookup"><span data-stu-id="659af-107">EXAMPLES</span></span>

### <span data-ttu-id="659af-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="659af-108">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -PeerName Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="659af-109">PeerAsn을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="659af-109">Gets the PeerAsn</span></span>

## <span data-ttu-id="659af-110">변수</span><span class="sxs-lookup"><span data-stu-id="659af-110">PARAMETERS</span></span>

### <span data-ttu-id="659af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="659af-111">-DefaultProfile</span></span>
<span data-ttu-id="659af-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="659af-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="659af-113">-이름</span><span class="sxs-lookup"><span data-stu-id="659af-113">-Name</span></span>
<span data-ttu-id="659af-114">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="659af-114">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="659af-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="659af-115">CommonParameters</span></span>
<span data-ttu-id="659af-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="659af-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="659af-117">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="659af-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="659af-118">입력</span><span class="sxs-lookup"><span data-stu-id="659af-118">INPUTS</span></span>

### <span data-ttu-id="659af-119">않아야</span><span class="sxs-lookup"><span data-stu-id="659af-119">None</span></span>

## <span data-ttu-id="659af-120">출력</span><span class="sxs-lookup"><span data-stu-id="659af-120">OUTPUTS</span></span>

### <span data-ttu-id="659af-121">PSPeerAsn (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="659af-121">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="659af-122">상속자</span><span class="sxs-lookup"><span data-stu-id="659af-122">NOTES</span></span>

## <span data-ttu-id="659af-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="659af-123">RELATED LINKS</span></span>
