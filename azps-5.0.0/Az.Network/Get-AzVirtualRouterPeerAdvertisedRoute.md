---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeeradvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
ms.openlocfilehash: 259fb6948abee3a00788e68c8d362196e5c12d51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216902"
---
# <span data-ttu-id="c0900-101">Get-AzVirtualRouterPeerAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="c0900-101">Get-AzVirtualRouterPeerAdvertisedRoute</span></span>

## <span data-ttu-id="c0900-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0900-102">SYNOPSIS</span></span>
<span data-ttu-id="c0900-103">특정 가상 라우터 피어로 알린 경로 나열</span><span class="sxs-lookup"><span data-stu-id="c0900-103">List routes being advertised by specific virtual router peer</span></span>

## <span data-ttu-id="c0900-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0900-104">SYNTAX</span></span>

### <span data-ttu-id="c0900-105">VirtualRouterPeerNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c0900-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -ResourceGroupName <String> -VirtualRouterName <String>
 -PeerName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0900-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0900-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0900-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c0900-107">DESCRIPTION</span></span>
<span data-ttu-id="c0900-108">가상 라우터 피어를 이름 또는 개체로 지정 하 여 특정 가상 라우터로 해당 피어에 알린 경로를 열거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0900-108">Given A virtual router peer either by name or by object, enumerate routes being advertised to that peer by a specific virtual router.</span></span>

## <span data-ttu-id="c0900-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c0900-109">EXAMPLES</span></span>

### <span data-ttu-id="c0900-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c0900-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerAdvertisedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="c0900-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="c0900-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerAdvertisedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="c0900-112">변수</span><span class="sxs-lookup"><span data-stu-id="c0900-112">PARAMETERS</span></span>

### <span data-ttu-id="c0900-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0900-113">-AsJob</span></span>
<span data-ttu-id="c0900-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c0900-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0900-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0900-115">-DefaultProfile</span></span>
<span data-ttu-id="c0900-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0900-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0900-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0900-117">-InputObject</span></span>
<span data-ttu-id="c0900-118">가상 라우터 피어 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c0900-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="c0900-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="c0900-119">-PeerName</span></span>
<span data-ttu-id="c0900-120">가상 라우터 피어 이름</span><span class="sxs-lookup"><span data-stu-id="c0900-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="c0900-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0900-121">-ResourceGroupName</span></span>
<span data-ttu-id="c0900-122">가상 라우터 피어 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="c0900-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="c0900-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="c0900-123">-VirtualRouterName</span></span>
<span data-ttu-id="c0900-124">가상 라우터 이름</span><span class="sxs-lookup"><span data-stu-id="c0900-124">Virtual router name</span></span>

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

### <span data-ttu-id="c0900-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0900-125">CommonParameters</span></span>
<span data-ttu-id="c0900-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0900-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0900-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c0900-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0900-128">입력</span><span class="sxs-lookup"><span data-stu-id="c0900-128">INPUTS</span></span>

### <span data-ttu-id="c0900-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c0900-129">System.String</span></span>

### <span data-ttu-id="c0900-130">Microsoft. 네트워크 모델. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="c0900-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="c0900-131">출력</span><span class="sxs-lookup"><span data-stu-id="c0900-131">OUTPUTS</span></span>

### <span data-ttu-id="c0900-132">PSPeerRoute에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c0900-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="c0900-133">상속자</span><span class="sxs-lookup"><span data-stu-id="c0900-133">NOTES</span></span>

## <span data-ttu-id="c0900-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0900-134">RELATED LINKS</span></span>
