---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeer.md
ms.openlocfilehash: 363e9518234551f55bf75fb6c93f8b0b70b495ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379793"
---
# <span data-ttu-id="3ea9e-101">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="3ea9e-101">Get-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="3ea9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ea9e-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea9e-103">Azure VirtualRouter에서 VirtualRouter 피어를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3ea9e-103">Gets a VirtualRouter peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="3ea9e-104">구문</span><span class="sxs-lookup"><span data-stu-id="3ea9e-104">SYNTAX</span></span>

### <span data-ttu-id="3ea9e-105">VirtualRouterPeerNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3ea9e-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ea9e-106">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ea9e-106">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Get-AzVirtualRouterPeer -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ea9e-107">설명</span><span class="sxs-lookup"><span data-stu-id="3ea9e-107">DESCRIPTION</span></span>
<span data-ttu-id="3ea9e-108">**Get-AzVirtualRouterPeer** cmdlet은 Azure VirtualRouter에서 피어를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3ea9e-108">The **Get-AzVirtualRouterPeer** cmdlet gets a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="3ea9e-109">예제</span><span class="sxs-lookup"><span data-stu-id="3ea9e-109">EXAMPLES</span></span>

### <span data-ttu-id="3ea9e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3ea9e-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -VirtualRouterName virtualRouter -PeerName csr
```

### <span data-ttu-id="3ea9e-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="3ea9e-111">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Get-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

## <span data-ttu-id="3ea9e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ea9e-112">PARAMETERS</span></span>

### <span data-ttu-id="3ea9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea9e-113">-DefaultProfile</span></span>
<span data-ttu-id="3ea9e-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ea9e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ea9e-115">-PeerName</span><span class="sxs-lookup"><span data-stu-id="3ea9e-115">-PeerName</span></span>
<span data-ttu-id="3ea9e-116">가상 라우터 피어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ea9e-116">The name of the virtual router peer.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ea9e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ea9e-117">-ResourceGroupName</span></span>
<span data-ttu-id="3ea9e-118">가상 라우터의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ea9e-118">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ea9e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ea9e-119">-ResourceId</span></span>
<span data-ttu-id="3ea9e-120">가상 라우터의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="3ea9e-120">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ea9e-121">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="3ea9e-121">-VirtualRouterName</span></span>
<span data-ttu-id="3ea9e-122">가상 라우터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ea9e-122">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ea9e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea9e-123">CommonParameters</span></span>
<span data-ttu-id="3ea9e-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3ea9e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea9e-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3ea9e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea9e-126">입력</span><span class="sxs-lookup"><span data-stu-id="3ea9e-126">INPUTS</span></span>

### <span data-ttu-id="3ea9e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="3ea9e-127">System.String</span></span>

## <span data-ttu-id="3ea9e-128">출력</span><span class="sxs-lookup"><span data-stu-id="3ea9e-128">OUTPUTS</span></span>

### <span data-ttu-id="3ea9e-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="3ea9e-129">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="3ea9e-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3ea9e-130">NOTES</span></span>

## <span data-ttu-id="3ea9e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ea9e-131">RELATED LINKS</span></span>
