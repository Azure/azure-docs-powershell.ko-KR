---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 147689b38f18caa1aa39ccd72d478e912336ad2b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496583"
---
# <span data-ttu-id="ee285-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="ee285-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="ee285-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee285-102">SYNOPSIS</span></span>
<span data-ttu-id="ee285-103">Azure VirtualRouter에서 피어를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ee285-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="ee285-104">구문</span><span class="sxs-lookup"><span data-stu-id="ee285-104">SYNTAX</span></span>

### <span data-ttu-id="ee285-105">VirtualRouterPeerNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ee285-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee285-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee285-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee285-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee285-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee285-108">설명</span><span class="sxs-lookup"><span data-stu-id="ee285-108">DESCRIPTION</span></span>
<span data-ttu-id="ee285-109">**Remove-AzVirtualRouterPeer** cmdlet은 Azure VirtualRouter에서 VirtualRouter 피어를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ee285-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="ee285-110">예제</span><span class="sxs-lookup"><span data-stu-id="ee285-110">EXAMPLES</span></span>

### <span data-ttu-id="ee285-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee285-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="ee285-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="ee285-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="ee285-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="ee285-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="ee285-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee285-114">PARAMETERS</span></span>

### <span data-ttu-id="ee285-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee285-115">-AsJob</span></span>
<span data-ttu-id="ee285-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ee285-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee285-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee285-117">-DefaultProfile</span></span>
<span data-ttu-id="ee285-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee285-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee285-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ee285-119">-Force</span></span>
<span data-ttu-id="ee285-120">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee285-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ee285-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee285-121">-InputObject</span></span>
<span data-ttu-id="ee285-122">가상 라우터 피어 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ee285-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="ee285-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="ee285-123">-PeerName</span></span>
<span data-ttu-id="ee285-124">가상 라우터 피어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee285-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="ee285-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee285-125">-ResourceGroupName</span></span>
<span data-ttu-id="ee285-126">가상 라우터/피어의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee285-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="ee285-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee285-127">-ResourceId</span></span>
<span data-ttu-id="ee285-128">가상 라우터 피어 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ee285-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="ee285-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="ee285-129">-VirtualRouterName</span></span>
<span data-ttu-id="ee285-130">피어가 있는 가상 라우터입니다.</span><span class="sxs-lookup"><span data-stu-id="ee285-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="ee285-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee285-131">-Confirm</span></span>
<span data-ttu-id="ee285-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee285-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee285-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee285-133">-WhatIf</span></span>
<span data-ttu-id="ee285-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ee285-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee285-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee285-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee285-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee285-136">CommonParameters</span></span>
<span data-ttu-id="ee285-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ee285-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee285-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ee285-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee285-139">입력</span><span class="sxs-lookup"><span data-stu-id="ee285-139">INPUTS</span></span>

### <span data-ttu-id="ee285-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ee285-140">System.String</span></span>

### <span data-ttu-id="ee285-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="ee285-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="ee285-142">출력</span><span class="sxs-lookup"><span data-stu-id="ee285-142">OUTPUTS</span></span>

### <span data-ttu-id="ee285-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="ee285-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="ee285-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ee285-144">NOTES</span></span>

## <span data-ttu-id="ee285-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee285-145">RELATED LINKS</span></span>
