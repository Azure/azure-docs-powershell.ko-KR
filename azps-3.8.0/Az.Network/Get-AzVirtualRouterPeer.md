---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: cf662dcd74182776131a5b7cfe3df3d86d20c14b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034824"
---
# <span data-ttu-id="89ec4-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="89ec4-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="89ec4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89ec4-102">SYNOPSIS</span></span>
<span data-ttu-id="89ec4-103">Azure VirtualRouter에서 VirtualRouter 피어를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89ec4-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>


## <span data-ttu-id="89ec4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89ec4-104">SYNTAX</span></span>

### <span data-ttu-id="89ec4-105">VirtualRouterPeerNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="89ec4-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89ec4-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89ec4-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89ec4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="89ec4-107">DESCRIPTION</span></span>
<span data-ttu-id="89ec4-108">**AzVirtualRouterPeer** Cmdlet은 Azure Virtualrouter에서 피어를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89ec4-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="89ec4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="89ec4-109">EXAMPLES</span></span>

### <span data-ttu-id="89ec4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="89ec4-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -RouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="89ec4-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="89ec4-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="89ec4-112">변수</span><span class="sxs-lookup"><span data-stu-id="89ec4-112">PARAMETERS</span></span>

### <span data-ttu-id="89ec4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ec4-113">-DefaultProfile</span></span>
<span data-ttu-id="89ec4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89ec4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ec4-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="89ec4-115">-PeerName</span></span>
<span data-ttu-id="89ec4-116">가상 라우터 피어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89ec4-116">The name of the virtual router peer.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ec4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89ec4-117">-ResourceGroupName</span></span>
<span data-ttu-id="89ec4-118">가상 라우터의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89ec4-118">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ec4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89ec4-119">-ResourceId</span></span>
<span data-ttu-id="89ec4-120">가상 라우터의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="89ec4-120">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ec4-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="89ec4-121">-VirtualRouterName</span></span>
<span data-ttu-id="89ec4-122">가상 라우터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89ec4-122">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ec4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ec4-123">CommonParameters</span></span>
<span data-ttu-id="89ec4-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89ec4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ec4-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89ec4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ec4-126">입력</span><span class="sxs-lookup"><span data-stu-id="89ec4-126">INPUTS</span></span>

### <span data-ttu-id="89ec4-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="89ec4-127">System.String</span></span>

## <span data-ttu-id="89ec4-128">출력</span><span class="sxs-lookup"><span data-stu-id="89ec4-128">OUTPUTS</span></span>

### <span data-ttu-id="89ec4-129">Microsoft. 네트워크 모델. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="89ec4-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="89ec4-130">상속자</span><span class="sxs-lookup"><span data-stu-id="89ec4-130">NOTES</span></span>

## <span data-ttu-id="89ec4-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89ec4-131">RELATED LINKS</span></span>
