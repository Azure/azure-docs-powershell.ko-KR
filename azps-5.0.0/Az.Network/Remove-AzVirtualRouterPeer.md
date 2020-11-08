---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 147689b38f18caa1aa39ccd72d478e912336ad2b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216073"
---
# <span data-ttu-id="5c724-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="5c724-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="5c724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c724-102">SYNOPSIS</span></span>
<span data-ttu-id="5c724-103">Azure VirtualRouter 피어를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c724-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="5c724-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5c724-104">SYNTAX</span></span>

### <span data-ttu-id="5c724-105">VirtualRouterPeerNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5c724-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c724-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c724-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c724-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c724-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c724-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5c724-108">DESCRIPTION</span></span>
<span data-ttu-id="5c724-109">**AzVirtualRouterPeer** Cmdlet은 Azure VirtualRouter Virtualrouter 피어를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c724-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="5c724-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5c724-110">EXAMPLES</span></span>

### <span data-ttu-id="5c724-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5c724-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="5c724-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="5c724-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="5c724-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="5c724-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="5c724-114">변수</span><span class="sxs-lookup"><span data-stu-id="5c724-114">PARAMETERS</span></span>

### <span data-ttu-id="5c724-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c724-115">-AsJob</span></span>
<span data-ttu-id="5c724-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5c724-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c724-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c724-117">-DefaultProfile</span></span>
<span data-ttu-id="5c724-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c724-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c724-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5c724-119">-Force</span></span>
<span data-ttu-id="5c724-120">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="5c724-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5c724-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c724-121">-InputObject</span></span>
<span data-ttu-id="5c724-122">가상 라우터 피어 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5c724-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="5c724-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="5c724-123">-PeerName</span></span>
<span data-ttu-id="5c724-124">가상 라우터 피어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c724-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="5c724-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c724-125">-ResourceGroupName</span></span>
<span data-ttu-id="5c724-126">가상 라우터/피어의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c724-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="5c724-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c724-127">-ResourceId</span></span>
<span data-ttu-id="5c724-128">가상 라우터 피어 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="5c724-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="5c724-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="5c724-129">-VirtualRouterName</span></span>
<span data-ttu-id="5c724-130">피어가 있는 가상 라우터입니다.</span><span class="sxs-lookup"><span data-stu-id="5c724-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="5c724-131">-확인</span><span class="sxs-lookup"><span data-stu-id="5c724-131">-Confirm</span></span>
<span data-ttu-id="5c724-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c724-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c724-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c724-133">-WhatIf</span></span>
<span data-ttu-id="5c724-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5c724-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c724-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c724-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c724-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c724-136">CommonParameters</span></span>
<span data-ttu-id="5c724-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c724-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c724-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5c724-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c724-139">입력</span><span class="sxs-lookup"><span data-stu-id="5c724-139">INPUTS</span></span>

### <span data-ttu-id="5c724-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5c724-140">System.String</span></span>

### <span data-ttu-id="5c724-141">Microsoft. 네트워크 모델. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="5c724-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="5c724-142">출력</span><span class="sxs-lookup"><span data-stu-id="5c724-142">OUTPUTS</span></span>

### <span data-ttu-id="5c724-143">Microsoft. 네트워크 모델. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="5c724-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="5c724-144">상속자</span><span class="sxs-lookup"><span data-stu-id="5c724-144">NOTES</span></span>

## <span data-ttu-id="5c724-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c724-145">RELATED LINKS</span></span>
