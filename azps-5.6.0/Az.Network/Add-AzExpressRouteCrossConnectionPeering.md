---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: b16206fdcaf775315947ca9fe71f487d1f9d8df1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011915"
---
# <span data-ttu-id="66345-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="66345-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="66345-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66345-102">SYNOPSIS</span></span>
<span data-ttu-id="66345-103">ExpressRoute 교차 연결에 피어링 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="66345-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="66345-104">구문</span><span class="sxs-lookup"><span data-stu-id="66345-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66345-105">설명</span><span class="sxs-lookup"><span data-stu-id="66345-105">DESCRIPTION</span></span>
<span data-ttu-id="66345-106">**Add-AzExpressRouteCrossConnectionPeering** cmdlet은 ExpressRoute 교차 연결에 피어링 구성을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="66345-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="66345-107">**Add-AzExpressRouteCrossConnectionPeering을** 실행한 후 구성을 활성화하려면 Set-AzExpressRouteCrossConnection cmdlet을 호출해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66345-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering**, you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="66345-108">예제</span><span class="sxs-lookup"><span data-stu-id="66345-108">EXAMPLES</span></span>

### <span data-ttu-id="66345-109">예제 1: 기존 ExpressRoute 교차 연결에 피어 추가</span><span class="sxs-lookup"><span data-stu-id="66345-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$parameters = @{
    Name = 'AzurePrivatePeering'
    CrossConnection = $cc
    PeeringType = 'AzurePrivatePeering'
    PeerASN = 100
    PrimaryPeerAddressPrefix = '10.6.1.0/30'
    SecondaryPeerAddressPrefix = '10.6.2.0/30'
    VlanId  = 200
}
Add-AzExpressRouteCrossConnectionPeering @parameters
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="66345-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="66345-110">PARAMETERS</span></span>

### <span data-ttu-id="66345-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66345-111">-DefaultProfile</span></span>
<span data-ttu-id="66345-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66345-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66345-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="66345-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="66345-114">수정되는 ExpressRoute 교차 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="66345-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="66345-115">**Get-AzExpressRouteCrossConnection** cmdlet에서 반환되는 Azure 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="66345-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66345-116">-Force</span><span class="sxs-lookup"><span data-stu-id="66345-116">-Force</span></span>
<span data-ttu-id="66345-117">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66345-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="66345-118">-MicrosoftConfigAdvertisedPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="66345-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="66345-119">MicrosoftPeering의 PeeringType의 경우 BGP 세션을 통해 보급하려는 모든 사전 목록을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66345-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="66345-120">공용 IP 주소 도두사만 허용됩니다.</span><span class="sxs-lookup"><span data-stu-id="66345-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="66345-121">콤마로 구분된 목록을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66345-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="66345-122">이러한 사전은 라우팅 레지스트리 이름(RIR/IRR)에 등록해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66345-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66345-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="66345-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="66345-124">피어링 AS 번호에 등록되지 않은 광고 도두사인 경우 등록된 AS 번호를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66345-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66345-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="66345-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="66345-126">AS 번호 및 약어가 등록되는 라우팅 레지스트리 이름(RIR/IRR)입니다.</span><span class="sxs-lookup"><span data-stu-id="66345-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66345-127">-Name</span><span class="sxs-lookup"><span data-stu-id="66345-127">-Name</span></span>
<span data-ttu-id="66345-128">추가할 피어링 관계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66345-128">The name of the peering relationship to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66345-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="66345-129">-PeerAddressType</span></span>
<span data-ttu-id="66345-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="66345-130">PeerAddressType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66345-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="66345-131">-PeerASN</span></span>
<span data-ttu-id="66345-132">ExpressRoute 교차 연결의 AS 수입니다.</span><span class="sxs-lookup"><span data-stu-id="66345-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="66345-133">PeeringType이 AzurePublicPeering인 경우 공용 ASN이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66345-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66345-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="66345-134">-PeeringType</span></span>
<span data-ttu-id="66345-135">이 매개 변수에 대해 허용되는 값은 `AzurePrivatePeering` , `AzurePublicPeering` , 및 `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="66345-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66345-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="66345-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="66345-137">이 피어링 관계의 기본 라우팅 경로에 대한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="66345-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="66345-138">/30 CIDR 서브넷이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66345-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="66345-139">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66345-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="66345-140">Azure는 Azure 라우터 인터페이스에 대한 다음 조차 번호 매기기 주소를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="66345-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66345-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="66345-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="66345-142">이 피어링 관계의 보조 라우팅 경로에 대한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="66345-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="66345-143">/30 CIDR 서브넷이 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66345-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="66345-144">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66345-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="66345-145">Azure는 Azure 라우터 인터페이스에 대한 다음 조차 번호 매기기 주소를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="66345-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66345-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="66345-146">-SharedKey</span></span>
<span data-ttu-id="66345-147">피어링 구성에 대한 사전 공유 키로 사용되는 선택적 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="66345-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66345-148">-VlanId</span><span class="sxs-lookup"><span data-stu-id="66345-148">-VlanId</span></span>
<span data-ttu-id="66345-149">이 피어링에 할당된 VLAN의 ID 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="66345-149">This is the Id number of the VLAN assigned for this peering.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66345-150">-확인</span><span class="sxs-lookup"><span data-stu-id="66345-150">-Confirm</span></span>
<span data-ttu-id="66345-151">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="66345-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66345-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66345-152">-WhatIf</span></span>
<span data-ttu-id="66345-153">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="66345-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66345-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66345-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66345-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66345-155">CommonParameters</span></span>
<span data-ttu-id="66345-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66345-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66345-157">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="66345-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66345-158">입력</span><span class="sxs-lookup"><span data-stu-id="66345-158">INPUTS</span></span>

### <span data-ttu-id="66345-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="66345-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="66345-160">매개 변수 'ExpressRouteCrossConnection'은 파이프라인에서 'PSExpressRouteCrossConnection' 형식의 값을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="66345-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="66345-161">출력</span><span class="sxs-lookup"><span data-stu-id="66345-161">OUTPUTS</span></span>

### <span data-ttu-id="66345-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="66345-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="66345-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66345-163">NOTES</span></span>

## <span data-ttu-id="66345-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66345-164">RELATED LINKS</span></span>

[<span data-ttu-id="66345-165">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="66345-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="66345-166">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="66345-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="66345-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="66345-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="66345-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="66345-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
