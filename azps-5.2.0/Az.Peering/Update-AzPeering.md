---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: 0f757c6bbde541876a3b4889f300a8d18e1cf113
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352149"
---
# <span data-ttu-id="e791f-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="e791f-101">Update-AzPeering</span></span>

## <span data-ttu-id="e791f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e791f-102">SYNOPSIS</span></span>
<span data-ttu-id="e791f-103">피어링을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e791f-103">Sets the Peering.</span></span> <span data-ttu-id="e791f-104">이 명령을 또는 에 함께 `Set-AzDirectPeeringConnectionObject` 사용 `Set-AzExchangePeeringConnectionObject`</span><span class="sxs-lookup"><span data-stu-id="e791f-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="e791f-105">구문</span><span class="sxs-lookup"><span data-stu-id="e791f-105">SYNTAX</span></span>

### <span data-ttu-id="e791f-106">DefaultExchange(기본값)</span><span class="sxs-lookup"><span data-stu-id="e791f-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e791f-107">DefaultDirect</span><span class="sxs-lookup"><span data-stu-id="e791f-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e791f-108">ByResourceIdDirect</span><span class="sxs-lookup"><span data-stu-id="e791f-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e791f-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="e791f-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e791f-110">직접</span><span class="sxs-lookup"><span data-stu-id="e791f-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e791f-111">Exchange</span><span class="sxs-lookup"><span data-stu-id="e791f-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e791f-112">설명</span><span class="sxs-lookup"><span data-stu-id="e791f-112">DESCRIPTION</span></span>
<span data-ttu-id="e791f-113">PSPeering 개체 설정</span><span class="sxs-lookup"><span data-stu-id="e791f-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="e791f-114">예제</span><span class="sxs-lookup"><span data-stu-id="e791f-114">EXAMPLES</span></span>

### <span data-ttu-id="e791f-115">Md5 인증 키 업데이트</span><span class="sxs-lookup"><span data-stu-id="e791f-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="e791f-116">Md5 인증 키 설정</span><span class="sxs-lookup"><span data-stu-id="e791f-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="e791f-117">UseForPeeringService 업데이트</span><span class="sxs-lookup"><span data-stu-id="e791f-117">Update UseForPeeringService</span></span>
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

<span data-ttu-id="e791f-118">피어링 서비스 플래그에 대한 사용 설정</span><span class="sxs-lookup"><span data-stu-id="e791f-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="e791f-119">Exchange 피어링에 대한 IPv4 주소 업데이트</span><span class="sxs-lookup"><span data-stu-id="e791f-119">Update IPv4 Address for Exchange Peering</span></span>
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

<span data-ttu-id="e791f-120">ResourceId를 사용하여 Exchange 피어링에 대한 Ipv4 주소 설정</span><span class="sxs-lookup"><span data-stu-id="e791f-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="e791f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e791f-121">PARAMETERS</span></span>

### <span data-ttu-id="e791f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e791f-122">-DefaultProfile</span></span>
<span data-ttu-id="e791f-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e791f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e791f-124">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="e791f-124">-DirectConnection</span></span>
<span data-ttu-id="e791f-125">다음 명령을 사용하여 새 직접 New-AzDirectPeeringConnectionObject 이 명령에 파이프합니다.</span><span class="sxs-lookup"><span data-stu-id="e791f-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

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

### <span data-ttu-id="e791f-126">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="e791f-126">-ExchangeConnection</span></span>
<span data-ttu-id="e791f-127">다음 명령을 사용하여 새 Exchange New-AzExchangePeeringConnectionObject 이 명령에 파이프합니다.</span><span class="sxs-lookup"><span data-stu-id="e791f-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

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

### <span data-ttu-id="e791f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e791f-128">-InputObject</span></span>
<span data-ttu-id="e791f-129">피어링 개체</span><span class="sxs-lookup"><span data-stu-id="e791f-129">The Peering object</span></span> 

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

### <span data-ttu-id="e791f-130">-Name</span><span class="sxs-lookup"><span data-stu-id="e791f-130">-Name</span></span>
<span data-ttu-id="e791f-131">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e791f-131">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e791f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e791f-132">-ResourceGroupName</span></span>
<span data-ttu-id="e791f-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e791f-133">The resource group name.</span></span>

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

### <span data-ttu-id="e791f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e791f-134">-ResourceId</span></span>
<span data-ttu-id="e791f-135">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e791f-135">The resource id string name.</span></span>

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

### <span data-ttu-id="e791f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e791f-136">-Confirm</span></span>
<span data-ttu-id="e791f-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e791f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e791f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e791f-138">-WhatIf</span></span>
<span data-ttu-id="e791f-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e791f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e791f-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e791f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e791f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e791f-141">CommonParameters</span></span>
<span data-ttu-id="e791f-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e791f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e791f-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e791f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e791f-144">입력</span><span class="sxs-lookup"><span data-stu-id="e791f-144">INPUTS</span></span>

### <span data-ttu-id="e791f-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="e791f-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="e791f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="e791f-146">System.String</span></span>

## <span data-ttu-id="e791f-147">출력</span><span class="sxs-lookup"><span data-stu-id="e791f-147">OUTPUTS</span></span>

### <span data-ttu-id="e791f-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="e791f-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="e791f-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e791f-149">NOTES</span></span>

## <span data-ttu-id="e791f-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e791f-150">RELATED LINKS</span></span>
