---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/update-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Update-AzPeering.md
ms.openlocfilehash: 0f757c6bbde541876a3b4889f300a8d18e1cf113
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218227"
---
# <span data-ttu-id="2e2b2-101">Update-AzPeering</span><span class="sxs-lookup"><span data-stu-id="2e2b2-101">Update-AzPeering</span></span>

## <span data-ttu-id="2e2b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e2b2-102">SYNOPSIS</span></span>
<span data-ttu-id="2e2b2-103">피어 링을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-103">Sets the Peering.</span></span> <span data-ttu-id="2e2b2-104">이 명령을 or와 함께 사용 `Set-AzDirectPeeringConnectionObject` `Set-AzExchangePeeringConnectionObject` 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-104">Use this Command in conjunction with `Set-AzDirectPeeringConnectionObject` or `Set-AzExchangePeeringConnectionObject`.</span></span>

## <span data-ttu-id="2e2b2-105">구문과</span><span class="sxs-lookup"><span data-stu-id="2e2b2-105">SYNTAX</span></span>

### <span data-ttu-id="2e2b2-106">DefaultExchange (기본값)</span><span class="sxs-lookup"><span data-stu-id="2e2b2-106">DefaultExchange (Default)</span></span>
```
Update-AzPeering -InputObject <PSPeering> [[-ExchangeConnection] <PSExchangeConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e2b2-107">DefaultDirect</span><span class="sxs-lookup"><span data-stu-id="2e2b2-107">DefaultDirect</span></span>
```
Update-AzPeering -InputObject <PSPeering> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e2b2-108">ByResourceIdDirect</span><span class="sxs-lookup"><span data-stu-id="2e2b2-108">ByResourceIdDirect</span></span>
```
Update-AzPeering -ResourceId <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e2b2-109">ByResourceIdExchange</span><span class="sxs-lookup"><span data-stu-id="2e2b2-109">ByResourceIdExchange</span></span>
```
Update-AzPeering -ResourceId <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e2b2-110">Dm</span><span class="sxs-lookup"><span data-stu-id="2e2b2-110">Direct</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-DirectConnection <PSDirectConnection[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e2b2-111">교환</span><span class="sxs-lookup"><span data-stu-id="2e2b2-111">Exchange</span></span>
```
Update-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-ExchangeConnection] <PSExchangeConnection[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e2b2-112">설명은</span><span class="sxs-lookup"><span data-stu-id="2e2b2-112">DESCRIPTION</span></span>
<span data-ttu-id="2e2b2-113">PSPeering 개체를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-113">Sets the PSPeering Object</span></span>

## <span data-ttu-id="2e2b2-114">예제의</span><span class="sxs-lookup"><span data-stu-id="2e2b2-114">EXAMPLES</span></span>

### <span data-ttu-id="2e2b2-115">Md5 인증 키 업데이트</span><span class="sxs-lookup"><span data-stu-id="2e2b2-115">Update Md5 Authentication Key</span></span>
```powershell
PS C:> $peering = Get-AzPeering -ResourceGroupName rg1 -PeerName "ContosoPeering"  
PS C:> $peering.Connections[0] = $peering.Connections[0] | Set-AzPeeringDirectConnectionObject -MD5AuthenticationKey $hash
PS C:> $peering | Update-AzPeering
```

<span data-ttu-id="2e2b2-116">Md5 인증 키를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-116">Sets the Md5 Authentication Key</span></span>

### <span data-ttu-id="2e2b2-117">UseForPeeringService 업데이트</span><span class="sxs-lookup"><span data-stu-id="2e2b2-117">Update UseForPeeringService</span></span>
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

<span data-ttu-id="2e2b2-118">피어 링 서비스 플래그의 사용을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-118">Sets the Use for Peering Service Flag</span></span>

### <span data-ttu-id="2e2b2-119">Exchange 피어 링에 대 한 IPv4 주소 업데이트</span><span class="sxs-lookup"><span data-stu-id="2e2b2-119">Update IPv4 Address for Exchange Peering</span></span>
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

<span data-ttu-id="2e2b2-120">ResourceId를 사용 하 여 Exchange 피어 링에 대 한 Ipv4 주소를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-120">Sets the Ipv4 Address for an Exchange Peering using ResourceId</span></span>

## <span data-ttu-id="2e2b2-121">변수</span><span class="sxs-lookup"><span data-stu-id="2e2b2-121">PARAMETERS</span></span>

### <span data-ttu-id="2e2b2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e2b2-122">-DefaultProfile</span></span>
<span data-ttu-id="2e2b2-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e2b2-124">-DirectConnection</span><span class="sxs-lookup"><span data-stu-id="2e2b2-124">-DirectConnection</span></span>
<span data-ttu-id="2e2b2-125">New-AzDirectPeeringConnectionObject 및 파이프를 사용 하 여이 명령에 대 한 새 직접 연결을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-125">Create a new Direct connections using the New-AzDirectPeeringConnectionObject and pipe to this command.</span></span>

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

### <span data-ttu-id="2e2b2-126">-ExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="2e2b2-126">-ExchangeConnection</span></span>
<span data-ttu-id="2e2b2-127">New-AzExchangePeeringConnectionObject를 사용 하 여 새 Exchange 연결을 만들고이 명령에 파이프 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-127">Create a new Exchange connection using the New-AzExchangePeeringConnectionObject and pipe to this command.</span></span>

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

### <span data-ttu-id="2e2b2-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e2b2-128">-InputObject</span></span>
<span data-ttu-id="2e2b2-129">피어 링 개체</span><span class="sxs-lookup"><span data-stu-id="2e2b2-129">The Peering object</span></span> 

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

### <span data-ttu-id="2e2b2-130">-이름</span><span class="sxs-lookup"><span data-stu-id="2e2b2-130">-Name</span></span>
<span data-ttu-id="2e2b2-131">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-131">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="2e2b2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e2b2-132">-ResourceGroupName</span></span>
<span data-ttu-id="2e2b2-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-133">The resource group name.</span></span>

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

### <span data-ttu-id="2e2b2-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e2b2-134">-ResourceId</span></span>
<span data-ttu-id="2e2b2-135">리소스 id 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-135">The resource id string name.</span></span>

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

### <span data-ttu-id="2e2b2-136">-확인</span><span class="sxs-lookup"><span data-stu-id="2e2b2-136">-Confirm</span></span>
<span data-ttu-id="2e2b2-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e2b2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e2b2-138">-WhatIf</span></span>
<span data-ttu-id="2e2b2-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e2b2-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e2b2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e2b2-141">CommonParameters</span></span>
<span data-ttu-id="2e2b2-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e2b2-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e2b2-144">입력</span><span class="sxs-lookup"><span data-stu-id="2e2b2-144">INPUTS</span></span>

### <span data-ttu-id="2e2b2-145">PSPeering (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="2e2b2-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2e2b2-146">System.String</span></span>

## <span data-ttu-id="2e2b2-147">출력</span><span class="sxs-lookup"><span data-stu-id="2e2b2-147">OUTPUTS</span></span>

### <span data-ttu-id="2e2b2-148">PSPeering (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2e2b2-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="2e2b2-149">상속자</span><span class="sxs-lookup"><span data-stu-id="2e2b2-149">NOTES</span></span>

## <span data-ttu-id="2e2b2-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e2b2-150">RELATED LINKS</span></span>
