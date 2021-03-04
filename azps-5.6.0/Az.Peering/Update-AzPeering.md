---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: 0824693c2d9f849b80f36065814f8dc57209a2a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989184"
---
# <span data-ttu-id="077a6-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="077a6-101">Update-AzPeering</span></span>

## <span data-ttu-id="077a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="077a6-102">SYNOPSIS</span></span>
<span data-ttu-id="077a6-103">피어링을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="077a6-103">Sets the Peering.</span></span> <span data-ttu-id="077a6-104">또는 와 함께 이 명령을 `Set-AzDirectPeeringConnectionObject` 사용 `Set-AzExchangePeeringConnectionObject` 합니다.</span><span class="sxs-lookup"><span data-stu-id="077a6-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="077a6-105">구문</span><span class="sxs-lookup"><span data-stu-id="077a6-105">SYNTAX</span></span>

### <span data-ttu-id="077a6-106">DefaultExchange(기본값)</span><span class="sxs-lookup"><span data-stu-id="077a6-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="077a6-107">DefaultDirect</span><span class="sxs-lookup"><span data-stu-id="077a6-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="077a6-108">ByResourceIdDirect</span><span class="sxs-lookup"><span data-stu-id="077a6-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="077a6-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="077a6-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="077a6-110">직접</span><span class="sxs-lookup"><span data-stu-id="077a6-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="077a6-111">Exchange</span><span class="sxs-lookup"><span data-stu-id="077a6-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="077a6-112">설명</span><span class="sxs-lookup"><span data-stu-id="077a6-112">DESCRIPTION</span></span>
<span data-ttu-id="077a6-113">PSPeering 개체 설정</span><span class="sxs-lookup"><span data-stu-id="077a6-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="077a6-114">예제</span><span class="sxs-lookup"><span data-stu-id="077a6-114">EXAMPLES</span></span>

### <span data-ttu-id="077a6-115">Md5 인증 키 업데이트</span><span class="sxs-lookup"><span data-stu-id="077a6-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="077a6-116">Md5 인증 키 설정</span><span class="sxs-lookup"><span data-stu-id="077a6-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="077a6-117">UseForPeeringService 업데이트</span><span class="sxs-lookup"><span data-stu-id="077a6-117">Update UseForPeeringService</span></span>
```powershell
PS C:> Update-AzPeering -ResourceGroupName rg1 -Name ContosoPeering -UseForPeeringService $true

Name                 : ContosoPeering
Sku.Name             : Premium_Direct_Free
Kind                 : Direct
Connections          : {71}
PeerAsn.Id           : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso
UseForPeeringService : True
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : West US 2
Id                   : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoPeering
Type                 : Microsoft.Peering/peerings
Tags                 : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="077a6-118">피어링 서비스 플래그 사용 설정</span><span class="sxs-lookup"><span data-stu-id="077a6-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="077a6-119">Exchange 피어링용 IPv4 주소 업데이트</span><span class="sxs-lookup"><span data-stu-id="077a6-119">Update IPv4 Address for Exchange Peering</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1  -PeerName "ContosoExchangePeering" 
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address $ipv4Address
PS C:> Update-AzPeering -ResourceId $peering.Id $peering.Connections

Name              : ContosoExchangePeering
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {13, 13}
PeerAsn.Id        : /subscriptions//providers/Microsoft.Peering/peerAsns/PeerName6935
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : West US 2
Id                : /subscriptions//resourceGroups/rg1/providers/Microsoft.Peering/peerings/ContosoExchangePeering
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="077a6-120">ResourceId를 사용하여 Exchange 피어링에 대한 Ipv4 주소 설정</span><span class="sxs-lookup"><span data-stu-id="077a6-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="077a6-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="077a6-121">PARAMETERS</span></span>

### <span data-ttu-id="077a6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="077a6-122">-DefaultProfile</span></span>
<span data-ttu-id="077a6-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="077a6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="077a6-124">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="077a6-124">-DirectConnection</span></span>
<span data-ttu-id="077a6-125">이 명령에 대한 New-AzDirectPeeringConnectionObject 파이프를 사용하여 새 직접 연결을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="077a6-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection[]
Parameter Sets: DefaultDirect, ByResourceIdDirect, Direct
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077a6-126">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="077a6-126">-ExchangeConnection</span></span>
<span data-ttu-id="077a6-127">이 명령에 대한 New-AzExchangePeeringConnectionObject 및 파이프를 사용하여 새 Exchange 연결을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="077a6-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: DefaultExchange
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection[]
Parameter Sets: ByResourceIdExchange, Exchange
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077a6-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="077a6-128">-InputObject</span></span>
<span data-ttu-id="077a6-129">피어링 개체</span><span class="sxs-lookup"><span data-stu-id="077a6-129">The Peering object</span></span> 

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: DefaultExchange, DefaultDirect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="077a6-130">-Name</span><span class="sxs-lookup"><span data-stu-id="077a6-130">-Name</span></span>
<span data-ttu-id="077a6-131">PSPeering의 고유한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="077a6-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077a6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="077a6-132">-ResourceGroupName</span></span>
<span data-ttu-id="077a6-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="077a6-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Direct, Exchange
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="077a6-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="077a6-134">-ResourceId</span></span>
<span data-ttu-id="077a6-135">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="077a6-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdDirect, ByResourceIdExchange
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="077a6-136">-확인</span><span class="sxs-lookup"><span data-stu-id="077a6-136">-Confirm</span></span>
<span data-ttu-id="077a6-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="077a6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="077a6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="077a6-138">-WhatIf</span></span>
<span data-ttu-id="077a6-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="077a6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="077a6-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="077a6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="077a6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="077a6-141">CommonParameters</span></span>
<span data-ttu-id="077a6-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="077a6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="077a6-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="077a6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="077a6-144">입력</span><span class="sxs-lookup"><span data-stu-id="077a6-144">INPUTS</span></span>

### <span data-ttu-id="077a6-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="077a6-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="077a6-146">System.String</span><span class="sxs-lookup"><span data-stu-id="077a6-146">System.String</span></span>

## <span data-ttu-id="077a6-147">출력</span><span class="sxs-lookup"><span data-stu-id="077a6-147">OUTPUTS</span></span>

### <span data-ttu-id="077a6-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="077a6-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="077a6-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="077a6-149">NOTES</span></span>

## <span data-ttu-id="077a6-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="077a6-150">RELATED LINKS</span></span>
