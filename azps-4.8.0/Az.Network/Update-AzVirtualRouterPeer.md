---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 242a3985d75e0a741c5e2175c098139b448f3e70
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056137"
---
# <span data-ttu-id="afc96-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="afc96-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="afc96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afc96-102">SYNOPSIS</span></span>
<span data-ttu-id="afc96-103">Azure VirtualRouter 피어 업데이트</span><span class="sxs-lookup"><span data-stu-id="afc96-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="afc96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="afc96-104">SYNTAX</span></span>

### <span data-ttu-id="afc96-105">VirtualRouterNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="afc96-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afc96-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="afc96-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afc96-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="afc96-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afc96-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="afc96-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afc96-109">설명은</span><span class="sxs-lookup"><span data-stu-id="afc96-109">DESCRIPTION</span></span>
<span data-ttu-id="afc96-110">**업데이트 AzVirtualRouterPeer** Cmdlet은 Virtualrouter 피어를 Azure virtualrouter로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="afc96-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="afc96-111">예제의</span><span class="sxs-lookup"><span data-stu-id="afc96-111">EXAMPLES</span></span>

### <span data-ttu-id="afc96-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="afc96-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="afc96-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="afc96-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="afc96-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="afc96-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="afc96-115">변수</span><span class="sxs-lookup"><span data-stu-id="afc96-115">PARAMETERS</span></span>

### <span data-ttu-id="afc96-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afc96-116">-AsJob</span></span>
<span data-ttu-id="afc96-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="afc96-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="afc96-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afc96-118">-DefaultProfile</span></span>
<span data-ttu-id="afc96-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="afc96-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afc96-120">-Force</span><span class="sxs-lookup"><span data-stu-id="afc96-120">-Force</span></span>
<span data-ttu-id="afc96-121">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="afc96-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="afc96-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afc96-122">-InputObject</span></span>
<span data-ttu-id="afc96-123">가상 라우터 피어 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="afc96-123">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="afc96-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="afc96-124">-PeerAsn</span></span>
<span data-ttu-id="afc96-125">피어 ASN.</span><span class="sxs-lookup"><span data-stu-id="afc96-125">Peer ASN.</span></span>

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

### <span data-ttu-id="afc96-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="afc96-126">-PeerIp</span></span>
<span data-ttu-id="afc96-127">피어 Ip.</span><span class="sxs-lookup"><span data-stu-id="afc96-127">Peer Ip.</span></span>

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

### <span data-ttu-id="afc96-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="afc96-128">-PeerName</span></span>
<span data-ttu-id="afc96-129">가상 라우터 피어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afc96-129">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="afc96-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afc96-130">-ResourceGroupName</span></span>
<span data-ttu-id="afc96-131">가상 라우터/피어의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afc96-131">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="afc96-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afc96-132">-ResourceId</span></span>
<span data-ttu-id="afc96-133">가상 라우터 피어 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="afc96-133">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="afc96-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="afc96-134">-VirtualRouterName</span></span>
<span data-ttu-id="afc96-135">피어가 있는 가상 라우터입니다.</span><span class="sxs-lookup"><span data-stu-id="afc96-135">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="afc96-136">-확인</span><span class="sxs-lookup"><span data-stu-id="afc96-136">-Confirm</span></span>
<span data-ttu-id="afc96-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="afc96-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afc96-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afc96-138">-WhatIf</span></span>
<span data-ttu-id="afc96-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="afc96-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afc96-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="afc96-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afc96-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afc96-141">CommonParameters</span></span>
<span data-ttu-id="afc96-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="afc96-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afc96-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="afc96-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afc96-144">입력</span><span class="sxs-lookup"><span data-stu-id="afc96-144">INPUTS</span></span>

### <span data-ttu-id="afc96-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="afc96-145">System.String</span></span>

### <span data-ttu-id="afc96-146">시스템. UInt32</span><span class="sxs-lookup"><span data-stu-id="afc96-146">System.UInt32</span></span>

### <span data-ttu-id="afc96-147">Microsoft. 네트워크 모델. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="afc96-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="afc96-148">출력</span><span class="sxs-lookup"><span data-stu-id="afc96-148">OUTPUTS</span></span>

### <span data-ttu-id="afc96-149">Microsoft. 네트워크 모델. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="afc96-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="afc96-150">상속자</span><span class="sxs-lookup"><span data-stu-id="afc96-150">NOTES</span></span>

## <span data-ttu-id="afc96-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="afc96-151">RELATED LINKS</span></span>
