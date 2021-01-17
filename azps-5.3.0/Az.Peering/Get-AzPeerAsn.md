---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeerAsn.md
ms.openlocfilehash: e6d47a040c9eb34361e0073421f618c27b4b762a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491732"
---
# <span data-ttu-id="158f6-101">Get-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="158f6-101">Get-AzPeerAsn</span></span>

## <span data-ttu-id="158f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="158f6-102">SYNOPSIS</span></span>
<span data-ttu-id="158f6-103">다음에서 PeerAsn 개체를 ARM.</span><span class="sxs-lookup"><span data-stu-id="158f6-103">Gets PeerAsn object from ARM.</span></span>

## <span data-ttu-id="158f6-104">구문</span><span class="sxs-lookup"><span data-stu-id="158f6-104">SYNTAX</span></span>

### <span data-ttu-id="158f6-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="158f6-105">ByName (Default)</span></span>
```
Get-AzPeerAsn [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="158f6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="158f6-106">ByResourceId</span></span>
```
Get-AzPeerAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="158f6-107">설명</span><span class="sxs-lookup"><span data-stu-id="158f6-107">DESCRIPTION</span></span>
<span data-ttu-id="158f6-108">구독에 대한 PeerAsn을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="158f6-108">Gets the PeerAsn for a subscription.</span></span>

## <span data-ttu-id="158f6-109">예제</span><span class="sxs-lookup"><span data-stu-id="158f6-109">EXAMPLES</span></span>

### <span data-ttu-id="158f6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="158f6-110">Example 1</span></span>
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

<span data-ttu-id="158f6-111">PeerAsn을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="158f6-111">Gets the PeerAsn</span></span>

## <span data-ttu-id="158f6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="158f6-112">PARAMETERS</span></span>

### <span data-ttu-id="158f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158f6-113">-DefaultProfile</span></span>
<span data-ttu-id="158f6-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="158f6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="158f6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="158f6-115">-Name</span></span>
<span data-ttu-id="158f6-116">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="158f6-116">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="158f6-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="158f6-117">-ResourceId</span></span>
<span data-ttu-id="158f6-118">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="158f6-118">The resource id string name.</span></span>

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

### <span data-ttu-id="158f6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158f6-119">CommonParameters</span></span>
<span data-ttu-id="158f6-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="158f6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158f6-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="158f6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158f6-122">입력</span><span class="sxs-lookup"><span data-stu-id="158f6-122">INPUTS</span></span>

### <span data-ttu-id="158f6-123">System.String</span><span class="sxs-lookup"><span data-stu-id="158f6-123">System.String</span></span>

## <span data-ttu-id="158f6-124">출력</span><span class="sxs-lookup"><span data-stu-id="158f6-124">OUTPUTS</span></span>

### <span data-ttu-id="158f6-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="158f6-125">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="158f6-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="158f6-126">NOTES</span></span>

## <span data-ttu-id="158f6-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="158f6-127">RELATED LINKS</span></span>
