---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 242a3985d75e0a741c5e2175c098139b448f3e70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184124"
---
# <span data-ttu-id="2ef41-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="2ef41-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="2ef41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ef41-102">SYNOPSIS</span></span>
<span data-ttu-id="2ef41-103">Azure VirtualRouter에서 피어 업데이트</span><span class="sxs-lookup"><span data-stu-id="2ef41-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="2ef41-104">구문</span><span class="sxs-lookup"><span data-stu-id="2ef41-104">SYNTAX</span></span>

### <span data-ttu-id="2ef41-105">VirtualRouterNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2ef41-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ef41-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ef41-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ef41-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ef41-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ef41-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ef41-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ef41-109">설명</span><span class="sxs-lookup"><span data-stu-id="2ef41-109">DESCRIPTION</span></span>
<span data-ttu-id="2ef41-110">**Update-AzVirtualRouterPeer** cmdlet은 VirtualRouter 피어를 Azure VirtualRouter로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef41-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="2ef41-111">예제</span><span class="sxs-lookup"><span data-stu-id="2ef41-111">EXAMPLES</span></span>

### <span data-ttu-id="2ef41-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="2ef41-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="2ef41-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="2ef41-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="2ef41-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="2ef41-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="2ef41-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ef41-115">PARAMETERS</span></span>

### <span data-ttu-id="2ef41-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ef41-116">-AsJob</span></span>
<span data-ttu-id="2ef41-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2ef41-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ef41-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ef41-118">-DefaultProfile</span></span>
<span data-ttu-id="2ef41-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef41-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ef41-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2ef41-120">-Force</span></span>
<span data-ttu-id="2ef41-121">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef41-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2ef41-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ef41-122">-InputObject</span></span>
<span data-ttu-id="2ef41-123">가상 라우터 피어 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef41-123">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="2ef41-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="2ef41-124">-PeerAsn</span></span>
<span data-ttu-id="2ef41-125">피어 ASN.</span><span class="sxs-lookup"><span data-stu-id="2ef41-125">Peer ASN.</span></span>

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

### <span data-ttu-id="2ef41-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="2ef41-126">-PeerIp</span></span>
<span data-ttu-id="2ef41-127">피어 IP.</span><span class="sxs-lookup"><span data-stu-id="2ef41-127">Peer Ip.</span></span>

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

### <span data-ttu-id="2ef41-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="2ef41-128">-PeerName</span></span>
<span data-ttu-id="2ef41-129">가상 라우터 피어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef41-129">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="2ef41-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ef41-130">-ResourceGroupName</span></span>
<span data-ttu-id="2ef41-131">가상 라우터/피어의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef41-131">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="2ef41-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ef41-132">-ResourceId</span></span>
<span data-ttu-id="2ef41-133">가상 라우터 피어 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef41-133">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="2ef41-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="2ef41-134">-VirtualRouterName</span></span>
<span data-ttu-id="2ef41-135">피어가 있는 가상 라우터입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef41-135">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="2ef41-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ef41-136">-Confirm</span></span>
<span data-ttu-id="2ef41-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef41-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ef41-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ef41-138">-WhatIf</span></span>
<span data-ttu-id="2ef41-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2ef41-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ef41-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef41-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ef41-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ef41-141">CommonParameters</span></span>
<span data-ttu-id="2ef41-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef41-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ef41-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2ef41-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ef41-144">입력</span><span class="sxs-lookup"><span data-stu-id="2ef41-144">INPUTS</span></span>

### <span data-ttu-id="2ef41-145">System.String</span><span class="sxs-lookup"><span data-stu-id="2ef41-145">System.String</span></span>

### <span data-ttu-id="2ef41-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="2ef41-146">System.UInt32</span></span>

### <span data-ttu-id="2ef41-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="2ef41-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="2ef41-148">출력</span><span class="sxs-lookup"><span data-stu-id="2ef41-148">OUTPUTS</span></span>

### <span data-ttu-id="2ef41-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="2ef41-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="2ef41-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2ef41-150">NOTES</span></span>

## <span data-ttu-id="2ef41-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ef41-151">RELATED LINKS</span></span>
