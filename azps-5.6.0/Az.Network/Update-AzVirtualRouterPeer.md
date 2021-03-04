---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 9e82946d13ac830d50affc621c965cfe8b81c503
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951483"
---
# <span data-ttu-id="d20c8-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="d20c8-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="d20c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d20c8-102">SYNOPSIS</span></span>
<span data-ttu-id="d20c8-103">Azure VirtualRouter에서 피어 업데이트</span><span class="sxs-lookup"><span data-stu-id="d20c8-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="d20c8-104">구문</span><span class="sxs-lookup"><span data-stu-id="d20c8-104">SYNTAX</span></span>

### <span data-ttu-id="d20c8-105">VirtualRouterNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d20c8-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d20c8-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d20c8-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d20c8-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d20c8-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d20c8-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d20c8-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d20c8-109">설명</span><span class="sxs-lookup"><span data-stu-id="d20c8-109">DESCRIPTION</span></span>
<span data-ttu-id="d20c8-110">**Update-AzVirtualRouterPeer** cmdlet은 VirtualRouter 피어를 Azure VirtualRouter로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d20c8-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="d20c8-111">예제</span><span class="sxs-lookup"><span data-stu-id="d20c8-111">EXAMPLES</span></span>

### <span data-ttu-id="d20c8-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="d20c8-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="d20c8-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d20c8-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="d20c8-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="d20c8-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="d20c8-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d20c8-115">PARAMETERS</span></span>

### <span data-ttu-id="d20c8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d20c8-116">-AsJob</span></span>
<span data-ttu-id="d20c8-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d20c8-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d20c8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d20c8-118">-DefaultProfile</span></span>
<span data-ttu-id="d20c8-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d20c8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d20c8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d20c8-120">-Force</span></span>
<span data-ttu-id="d20c8-121">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d20c8-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d20c8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d20c8-122">-InputObject</span></span>
<span data-ttu-id="d20c8-123">가상 라우터 피어 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d20c8-123">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="d20c8-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="d20c8-124">-PeerAsn</span></span>
<span data-ttu-id="d20c8-125">피어 ASN.</span><span class="sxs-lookup"><span data-stu-id="d20c8-125">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d20c8-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="d20c8-126">-PeerIp</span></span>
<span data-ttu-id="d20c8-127">피어 IP입니다.</span><span class="sxs-lookup"><span data-stu-id="d20c8-127">Peer Ip.</span></span>

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

### <span data-ttu-id="d20c8-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="d20c8-128">-PeerName</span></span>
<span data-ttu-id="d20c8-129">가상 라우터 피어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d20c8-129">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="d20c8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d20c8-130">-ResourceGroupName</span></span>
<span data-ttu-id="d20c8-131">가상 라우터/피어의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d20c8-131">The resource group name of the virtual router/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d20c8-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d20c8-132">-ResourceId</span></span>
<span data-ttu-id="d20c8-133">가상 라우터 피어 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d20c8-133">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="d20c8-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="d20c8-134">-VirtualRouterName</span></span>
<span data-ttu-id="d20c8-135">피어가 있는 가상 라우터입니다.</span><span class="sxs-lookup"><span data-stu-id="d20c8-135">The virtual router where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d20c8-136">-확인</span><span class="sxs-lookup"><span data-stu-id="d20c8-136">-Confirm</span></span>
<span data-ttu-id="d20c8-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d20c8-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d20c8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d20c8-138">-WhatIf</span></span>
<span data-ttu-id="d20c8-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d20c8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d20c8-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d20c8-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d20c8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d20c8-141">CommonParameters</span></span>
<span data-ttu-id="d20c8-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d20c8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d20c8-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d20c8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d20c8-144">입력</span><span class="sxs-lookup"><span data-stu-id="d20c8-144">INPUTS</span></span>

### <span data-ttu-id="d20c8-145">System.String</span><span class="sxs-lookup"><span data-stu-id="d20c8-145">System.String</span></span>

### <span data-ttu-id="d20c8-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="d20c8-146">System.UInt32</span></span>

### <span data-ttu-id="d20c8-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="d20c8-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="d20c8-148">출력</span><span class="sxs-lookup"><span data-stu-id="d20c8-148">OUTPUTS</span></span>

### <span data-ttu-id="d20c8-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="d20c8-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="d20c8-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d20c8-150">NOTES</span></span>

## <span data-ttu-id="d20c8-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d20c8-151">RELATED LINKS</span></span>
