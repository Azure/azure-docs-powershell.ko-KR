---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C44AD23A-E575-418C-BE90-323B44D6D2E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 3899bfcd607e4d3e5e5b1d92e8a62096037102a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217053"
---
# <span data-ttu-id="32601-101">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="32601-101">Add-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="32601-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32601-102">SYNOPSIS</span></span>
<span data-ttu-id="32601-103">Express 경로 연결에 피어 링 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="32601-103">Adds a peering configuration to an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="32601-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32601-104">SYNTAX</span></span>

```
Add-AzExpressRouteCrossConnectionPeering -Name <String>
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-Force] -PeeringType <String> -PeerASN <UInt32>
 -PrimaryPeerAddressPrefix <String> -SecondaryPeerAddressPrefix <String> -VlanId <Int32> [-SharedKey <String>]
 [-MicrosoftConfigAdvertisedPublicPrefix <String[]>] [-MicrosoftConfigCustomerAsn <Int32>]
 [-MicrosoftConfigRoutingRegistryName <String>] [-PeerAddressType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32601-105">설명은</span><span class="sxs-lookup"><span data-stu-id="32601-105">DESCRIPTION</span></span>
<span data-ttu-id="32601-106">**AzExpressRouteCrossConnectionPeering** cmdlet은 피어 링 구성을 express 경로 간 연결에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="32601-106">The **Add-AzExpressRouteCrossConnectionPeering** cmdlet adds a peering configuration to an ExpressRoute cross connection.</span></span> <span data-ttu-id="32601-107">**Add-AzExpressRouteCrossConnectionPeering** 을 실행 한 후에는 Set-AzExpressRouteCrossConnection cmdlet을 호출 하 여 구성을 활성화 해야 한다는 점에 주의 하세요.</span><span class="sxs-lookup"><span data-stu-id="32601-107">Note that, after running **Add-AzExpressRouteCrossConnectionPeering** , you must call the Set-AzExpressRouteCrossConnection cmdlet to activate the configuration.</span></span>

## <span data-ttu-id="32601-108">예제의</span><span class="sxs-lookup"><span data-stu-id="32601-108">EXAMPLES</span></span>

### <span data-ttu-id="32601-109">예제 1: 기존 Express 경로 상호 연결에 피어 추가</span><span class="sxs-lookup"><span data-stu-id="32601-109">Example 1: Add a peer to an existing ExpressRoute cross connection</span></span>
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

## <span data-ttu-id="32601-110">변수</span><span class="sxs-lookup"><span data-stu-id="32601-110">PARAMETERS</span></span>

### <span data-ttu-id="32601-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32601-111">-DefaultProfile</span></span>
<span data-ttu-id="32601-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32601-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32601-113">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="32601-113">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="32601-114">수정 중인 Express 경로 교차 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="32601-114">The ExpressRoute cross connection being modified.</span></span> <span data-ttu-id="32601-115">**AzExpressRouteCrossConnection** cmdlet에서 반환 된 Azure 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="32601-115">This is Azure object returned by the **Get-AzExpressRouteCrossConnection** cmdlet.</span></span>

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

### <span data-ttu-id="32601-116">-Force</span><span class="sxs-lookup"><span data-stu-id="32601-116">-Force</span></span>
<span data-ttu-id="32601-117">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="32601-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="32601-118">-MicrosoftConfigAdvertisedPublicPrefix</span><span class="sxs-lookup"><span data-stu-id="32601-118">-MicrosoftConfigAdvertisedPublicPrefix</span></span>
<span data-ttu-id="32601-119">MicrosoftPeering의 PeeringType 경우 BGP 세션을 통해 알릴 모든 접두 번호 목록을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32601-119">For a PeeringType of MicrosoftPeering, you must provide a list of all prefixes you plan to advertise over the BGP session.</span></span> <span data-ttu-id="32601-120">공용 IP 주소 접두사만 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32601-120">Only public IP address prefixes are accepted.</span></span> <span data-ttu-id="32601-121">접두 번호 집합을 보낼 계획 이라면 쉼표로 구분 된 목록을 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32601-121">You can send a comma separated list if you plan to send a set of prefixes.</span></span> <span data-ttu-id="32601-122">이러한 접두사는 RIR/IRR (라우팅 레지스트리 이름)에 등록 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32601-122">These prefixes must be registered to you in a Routing Registry Name (RIR / IRR).</span></span>

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

### <span data-ttu-id="32601-123">-MicrosoftConfigCustomerAsn</span><span class="sxs-lookup"><span data-stu-id="32601-123">-MicrosoftConfigCustomerAsn</span></span>
<span data-ttu-id="32601-124">피어 링에 번호로 등록 되지 않은 접두사를 광고 하는 경우 AS 번호를 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32601-124">If you are advertising prefixes that are not registered to the peering AS number, you can specify the AS number to which they are registered.</span></span>

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

### <span data-ttu-id="32601-125">-MicrosoftConfigRoutingRegistryName</span><span class="sxs-lookup"><span data-stu-id="32601-125">-MicrosoftConfigRoutingRegistryName</span></span>
<span data-ttu-id="32601-126">AS number 및 접두사가 등록 되는 라우팅 레지스트리 이름 (RIR/IRR)입니다.</span><span class="sxs-lookup"><span data-stu-id="32601-126">The Routing Registry Name (RIR / IRR) to which the AS number and prefixes are registered.</span></span>

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

### <span data-ttu-id="32601-127">-이름</span><span class="sxs-lookup"><span data-stu-id="32601-127">-Name</span></span>
<span data-ttu-id="32601-128">추가할 피어 링 관계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32601-128">The name of the peering relationship to be added.</span></span>

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

### <span data-ttu-id="32601-129">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="32601-129">-PeerAddressType</span></span>
<span data-ttu-id="32601-130">PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="32601-130">PeerAddressType</span></span>

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

### <span data-ttu-id="32601-131">-PeerASN</span><span class="sxs-lookup"><span data-stu-id="32601-131">-PeerASN</span></span>
<span data-ttu-id="32601-132">사용자의 Express 교차 연결의 AS 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="32601-132">The AS number of your ExpressRoute cross connection.</span></span> <span data-ttu-id="32601-133">PeeringType가 AzurePublicPeering 링 인 경우이는 공용 ASN 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32601-133">This must be a Public ASN when the PeeringType is AzurePublicPeering.</span></span>

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

### <span data-ttu-id="32601-134">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="32601-134">-PeeringType</span></span>
<span data-ttu-id="32601-135">이 매개 변수에 허용 되는 값은 `AzurePrivatePeering` , 및 등입니다. `AzurePublicPeering``MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="32601-135">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="32601-136">-PrimaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="32601-136">-PrimaryPeerAddressPrefix</span></span>
<span data-ttu-id="32601-137">이 피어 링 관계의 기본 라우팅 경로에 대 한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="32601-137">This is the IP Address range for the primary routing path of this peering relationship.</span></span> <span data-ttu-id="32601-138">이는/30 CIDR 서브넷 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32601-138">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="32601-139">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32601-139">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="32601-140">Azure는 다음 짝수 번호 주소를 Azure 라우터 인터페이스로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="32601-140">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="32601-141">-SecondaryPeerAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="32601-141">-SecondaryPeerAddressPrefix</span></span>
<span data-ttu-id="32601-142">이 피어 링 관계의 보조 라우팅 경로에 대 한 IP 주소 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="32601-142">This is the IP Address range for the secondary routing path of this peering relationship.</span></span> <span data-ttu-id="32601-143">이는/30 CIDR 서브넷 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32601-143">This must be a /30 CIDR subnet.</span></span> <span data-ttu-id="32601-144">이 서브넷의 첫 번째 홀수 번호 주소는 라우터 인터페이스에 할당 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32601-144">The first odd-numbered address in this subnet should be assigned to your router interface.</span></span> <span data-ttu-id="32601-145">Azure는 다음 짝수 번호 주소를 Azure 라우터 인터페이스로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="32601-145">Azure will configure the next even-numbered address to the Azure router interface.</span></span>

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

### <span data-ttu-id="32601-146">-SharedKey</span><span class="sxs-lookup"><span data-stu-id="32601-146">-SharedKey</span></span>
<span data-ttu-id="32601-147">이는 피어 링 구성에 미리 공유한 키로 사용 되는 선택적 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="32601-147">This is an optional MD5 hash used as a pre-shared key for the peering configuration.</span></span>

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

### <span data-ttu-id="32601-148">-VlanId</span><span class="sxs-lookup"><span data-stu-id="32601-148">-VlanId</span></span>
<span data-ttu-id="32601-149">이 피어 링에 할당 된 VLAN Id 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="32601-149">This is the Id number of the VLAN assigned for this peering.</span></span>

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

### <span data-ttu-id="32601-150">-확인</span><span class="sxs-lookup"><span data-stu-id="32601-150">-Confirm</span></span>
<span data-ttu-id="32601-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="32601-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32601-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32601-152">-WhatIf</span></span>
<span data-ttu-id="32601-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="32601-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32601-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32601-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32601-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32601-155">CommonParameters</span></span>
<span data-ttu-id="32601-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32601-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32601-157">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32601-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32601-158">입력</span><span class="sxs-lookup"><span data-stu-id="32601-158">INPUTS</span></span>

### <span data-ttu-id="32601-159">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="32601-159">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="32601-160">' ExpressRouteCrossConnection ' 매개 변수는 파이프라인에서 ' PSExpressRouteCrossConnection ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="32601-160">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="32601-161">출력</span><span class="sxs-lookup"><span data-stu-id="32601-161">OUTPUTS</span></span>

### <span data-ttu-id="32601-162">PSExpressRouteCrossConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="32601-162">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="32601-163">상속자</span><span class="sxs-lookup"><span data-stu-id="32601-163">NOTES</span></span>

## <span data-ttu-id="32601-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32601-164">RELATED LINKS</span></span>

[<span data-ttu-id="32601-165">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="32601-165">Get-AzExpressRouteCrossConnectionPeering</span></span>](Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="32601-166">제거-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="32601-166">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="32601-167">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="32601-167">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="32601-168">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="32601-168">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
