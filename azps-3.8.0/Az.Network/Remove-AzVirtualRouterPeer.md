---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 871a06a2bbd3a844dd758dbc16189afdb261db2d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043965"
---
# <span data-ttu-id="e2e05-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="e2e05-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="e2e05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2e05-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e05-103">Azure VirtualRouter 피어를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e05-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="e2e05-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2e05-104">SYNTAX</span></span>

### <span data-ttu-id="e2e05-105">VirtualRouterPeerNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e2e05-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2e05-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2e05-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2e05-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2e05-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2e05-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e2e05-108">DESCRIPTION</span></span>
<span data-ttu-id="e2e05-109">**AzVirtualRouterPeer** Cmdlet은 Azure VirtualRouter Virtualrouter 피어를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e05-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="e2e05-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e2e05-110">EXAMPLES</span></span>

### <span data-ttu-id="e2e05-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e2e05-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="e2e05-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="e2e05-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="e2e05-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="e2e05-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="e2e05-114">변수</span><span class="sxs-lookup"><span data-stu-id="e2e05-114">PARAMETERS</span></span>

### <span data-ttu-id="e2e05-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2e05-115">-AsJob</span></span>
<span data-ttu-id="e2e05-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e2e05-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e05-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e05-117">-DefaultProfile</span></span>
<span data-ttu-id="e2e05-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2e05-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2e05-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e2e05-119">-Force</span></span>
<span data-ttu-id="e2e05-120">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="e2e05-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e05-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2e05-121">-InputObject</span></span>
<span data-ttu-id="e2e05-122">가상 라우터 피어 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e2e05-122">The virtual router peer input object.</span></span>

```yaml
Type: PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e05-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="e2e05-123">-PeerName</span></span>
<span data-ttu-id="e2e05-124">가상 라우터 피어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2e05-124">The name of the virtual router Peer.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e05-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2e05-125">-ResourceGroupName</span></span>
<span data-ttu-id="e2e05-126">가상 라우터/피어의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2e05-126">The resource group name of the virtual router/peer.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet, VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e05-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2e05-127">-ResourceId</span></span>
<span data-ttu-id="e2e05-128">가상 라우터 피어 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="e2e05-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="e2e05-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="e2e05-129">-VirtualRouterName</span></span>
<span data-ttu-id="e2e05-130">피어가 있는 가상 라우터입니다.</span><span class="sxs-lookup"><span data-stu-id="e2e05-130">The virtual router where peer exists.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet, VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e05-131">-확인</span><span class="sxs-lookup"><span data-stu-id="e2e05-131">-Confirm</span></span>
<span data-ttu-id="e2e05-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e05-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e05-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2e05-133">-WhatIf</span></span>
<span data-ttu-id="e2e05-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2e05-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2e05-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2e05-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e05-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e05-136">CommonParameters</span></span>
<span data-ttu-id="e2e05-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e05-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e05-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2e05-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e05-139">입력</span><span class="sxs-lookup"><span data-stu-id="e2e05-139">INPUTS</span></span>

### <span data-ttu-id="e2e05-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e2e05-140">System.String</span></span>

### <span data-ttu-id="e2e05-141">Microsoft. 네트워크 모델. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="e2e05-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="e2e05-142">출력</span><span class="sxs-lookup"><span data-stu-id="e2e05-142">OUTPUTS</span></span>

### <span data-ttu-id="e2e05-143">Microsoft. 네트워크 모델. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e2e05-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="e2e05-144">상속자</span><span class="sxs-lookup"><span data-stu-id="e2e05-144">NOTES</span></span>

## <span data-ttu-id="e2e05-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2e05-145">RELATED LINKS</span></span>
