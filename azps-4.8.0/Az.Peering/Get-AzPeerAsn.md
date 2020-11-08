---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e6d47a040c9eb34361e0073421f618c27b4b762a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048799"
---
# <span data-ttu-id="a98b4-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="a98b4-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="a98b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a98b4-102">SYNOPSIS</span></span>
<span data-ttu-id="a98b4-103">ARM에서 PeerAsn 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a98b4-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="a98b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a98b4-104">SYNTAX</span></span>

### <span data-ttu-id="a98b4-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a98b4-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a98b4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a98b4-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a98b4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a98b4-107">DESCRIPTION</span></span>
<span data-ttu-id="a98b4-108">구독에 대 한 PeerAsn을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a98b4-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="a98b4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a98b4-109">EXAMPLES</span></span>

### <span data-ttu-id="a98b4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a98b4-110">Example 1</span></span>
```powershell
PS C:> Get-AzPeerAsn -Name Contoso

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="a98b4-111">PeerAsn을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a98b4-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="a98b4-112">변수</span><span class="sxs-lookup"><span data-stu-id="a98b4-112">PARAMETERS</span></span>

### <span data-ttu-id="a98b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a98b4-113">-DefaultProfile</span></span>
<span data-ttu-id="a98b4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a98b4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a98b4-115">-이름</span><span class="sxs-lookup"><span data-stu-id="a98b4-115">-Name</span></span>
<span data-ttu-id="a98b4-116">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a98b4-116">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a98b4-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a98b4-117">-ResourceId</span></span>
<span data-ttu-id="a98b4-118">리소스 id 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a98b4-118">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a98b4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a98b4-119">CommonParameters</span></span>
<span data-ttu-id="a98b4-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98b4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a98b4-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a98b4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a98b4-122">입력</span><span class="sxs-lookup"><span data-stu-id="a98b4-122">INPUTS</span></span>

### <span data-ttu-id="a98b4-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a98b4-123">System.String</span></span>

## <span data-ttu-id="a98b4-124">출력</span><span class="sxs-lookup"><span data-stu-id="a98b4-124">OUTPUTS</span></span>

### <span data-ttu-id="a98b4-125">PSPeerAsn (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a98b4-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="a98b4-126">상속자</span><span class="sxs-lookup"><span data-stu-id="a98b4-126">NOTES</span></span>

## <span data-ttu-id="a98b4-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a98b4-127">RELATED LINKS</span></span>
