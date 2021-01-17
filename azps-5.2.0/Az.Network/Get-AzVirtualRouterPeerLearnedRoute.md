---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 8c01f935196cb5aaaf553d1c1041589def80aeeb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352682"
---
# <span data-ttu-id="c49a7-101">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="c49a7-101">Get-AzVirtualRouterPeerLearnedRoute</span></span>

## <span data-ttu-id="c49a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c49a7-102">SYNOPSIS</span></span>
<span data-ttu-id="c49a7-103">특정 가상 라우터 피어에서 학습한 경로 나열</span><span class="sxs-lookup"><span data-stu-id="c49a7-103">List routes learned by a specific virtual router peer</span></span>

## <span data-ttu-id="c49a7-104">구문</span><span class="sxs-lookup"><span data-stu-id="c49a7-104">SYNTAX</span></span>

### <span data-ttu-id="c49a7-105">VirtualRouterPeerNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c49a7-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c49a7-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c49a7-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c49a7-107">설명</span><span class="sxs-lookup"><span data-stu-id="c49a7-107">DESCRIPTION</span></span>
<span data-ttu-id="c49a7-108">다른 원본의 가상 라우터 피어에서 학습한 경로를 열회합니다.</span><span class="sxs-lookup"><span data-stu-id="c49a7-108">Enumerate routes learned by a virtual router peer from other sources.</span></span>

## <span data-ttu-id="c49a7-109">예제</span><span class="sxs-lookup"><span data-stu-id="c49a7-109">EXAMPLES</span></span>

### <span data-ttu-id="c49a7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c49a7-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="c49a7-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="c49a7-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="c49a7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c49a7-112">PARAMETERS</span></span>

### <span data-ttu-id="c49a7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c49a7-113">-AsJob</span></span>
<span data-ttu-id="c49a7-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c49a7-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c49a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c49a7-115">-DefaultProfile</span></span>
<span data-ttu-id="c49a7-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c49a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c49a7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c49a7-117">-InputObject</span></span>
<span data-ttu-id="c49a7-118">가상 라우터 피어 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c49a7-118">The virtual router peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c49a7-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="c49a7-119">-PeerName</span></span>
<span data-ttu-id="c49a7-120">가상 라우터 피어 이름</span><span class="sxs-lookup"><span data-stu-id="c49a7-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="c49a7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c49a7-121">-ResourceGroupName</span></span>
<span data-ttu-id="c49a7-122">가상 라우터 피어 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="c49a7-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="c49a7-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="c49a7-123">-VirtualRouterName</span></span>
<span data-ttu-id="c49a7-124">가상 라우터 이름</span><span class="sxs-lookup"><span data-stu-id="c49a7-124">Virtual router name</span></span>

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

### <span data-ttu-id="c49a7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c49a7-125">CommonParameters</span></span>
<span data-ttu-id="c49a7-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c49a7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c49a7-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c49a7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c49a7-128">입력</span><span class="sxs-lookup"><span data-stu-id="c49a7-128">INPUTS</span></span>

### <span data-ttu-id="c49a7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c49a7-129">System.String</span></span>

### <span data-ttu-id="c49a7-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="c49a7-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="c49a7-131">출력</span><span class="sxs-lookup"><span data-stu-id="c49a7-131">OUTPUTS</span></span>

### <span data-ttu-id="c49a7-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="c49a7-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="c49a7-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c49a7-133">NOTES</span></span>

## <span data-ttu-id="c49a7-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c49a7-134">RELATED LINKS</span></span>
