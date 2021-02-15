---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 028c33db36df5debb6f951f11e27f0586e7a21dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193545"
---
# <span data-ttu-id="eb2f7-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="eb2f7-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="eb2f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb2f7-102">SYNOPSIS</span></span>
<span data-ttu-id="eb2f7-103">이 명령을 사용하면 사용자가 VPN 게이트웨이에 설정할 IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup과 같은 하나 또는 모든 값을 지정하는 Vpn ipsec 정책 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb2f7-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="eb2f7-104">이 명령 let output 개체는 새 게이트웨이/기존 게이트웨이 모두에 대한 vpn ipsec 정책을 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="eb2f7-104">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="eb2f7-105">구문</span><span class="sxs-lookup"><span data-stu-id="eb2f7-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb2f7-106">설명</span><span class="sxs-lookup"><span data-stu-id="eb2f7-106">DESCRIPTION</span></span>
<span data-ttu-id="eb2f7-107">이 명령을 사용하면 사용자가 VPN 게이트웨이에 설정할 IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup과 같은 하나 또는 모든 값을 지정하는 Vpn ipsec 정책 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb2f7-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="eb2f7-108">이 명령 let output 개체는 새 게이트웨이/기존 게이트웨이 모두에 대한 vpn ipsec 정책을 설정하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="eb2f7-108">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="eb2f7-109">예제</span><span class="sxs-lookup"><span data-stu-id="eb2f7-109">EXAMPLES</span></span>

### <span data-ttu-id="eb2f7-110">예제 1: vpn ipsec 정책 개체 정의:</span><span class="sxs-lookup"><span data-stu-id="eb2f7-110">Example 1: Define vpn ipsec policy object:</span></span>
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="eb2f7-111">이 cmdlet은 사용자가 PARAM:VpnClientIpsecPolicy에 전달할 수 있는 하나 또는 모든 매개 변수 값을 사용하여 ResourceGroup에서 New-AzVirtualNetworkGateway(새 VPN Gateway 만들기) /Set-AzVirtualNetworkGateway(기존 VPN Gateway 업데이트)를 사용하여 vpn ipsec 정책 개체를 만드는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="eb2f7-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="eb2f7-112">예제 2: VPN 사용자 지정 ipsec 정책을 설정하여 새 가상 네트워크 게이트웨이 만들기:</span><span class="sxs-lookup"><span data-stu-id="eb2f7-112">Example 2: Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="eb2f7-113">이 cmdlet은 생성 후 가상 네트워크 게이트웨이 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2f7-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="eb2f7-114">예제 3: 기존 가상 네트워크 게이트웨이에서 VPN 사용자 지정 ipsec 정책 설정:</span><span class="sxs-lookup"><span data-stu-id="eb2f7-114">Example 3: Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="eb2f7-115">이 cmdlet은 vpn 사용자 지정 ipsec 정책을 설정한 후 가상 네트워크 게이트웨이 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2f7-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="eb2f7-116">예제 4: 가상 네트워크 게이트웨이를 사용하여 VPN 사용자 지정 정책이 올바르게 설정되어 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2f7-116">Example 4: Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="eb2f7-117">이 cmdlet은 가상 네트워크 게이트웨이 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2f7-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="eb2f7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb2f7-118">PARAMETERS</span></span>

### <span data-ttu-id="eb2f7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb2f7-119">-DefaultProfile</span></span>
<span data-ttu-id="eb2f7-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb2f7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb2f7-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="eb2f7-121">-DhGroup</span></span>
<span data-ttu-id="eb2f7-122">IKE 1단계에서 초기 SA에 사용되는 VpnClient DH 그룹</span><span class="sxs-lookup"><span data-stu-id="eb2f7-122">The VpnClient DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb2f7-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="eb2f7-123">-IkeEncryption</span></span>
<span data-ttu-id="eb2f7-124">VpnClient IKE 암호화 알고리즘(IKE 2단계)</span><span class="sxs-lookup"><span data-stu-id="eb2f7-124">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb2f7-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="eb2f7-125">-IkeIntegrity</span></span>
<span data-ttu-id="eb2f7-126">VpnClient IKE 무결성 알고리즘(IKE 2단계)</span><span class="sxs-lookup"><span data-stu-id="eb2f7-126">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb2f7-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="eb2f7-127">-IpsecEncryption</span></span>
<span data-ttu-id="eb2f7-128">VpnClient IPSec 암호화 알고리즘(IKE 1단계)</span><span class="sxs-lookup"><span data-stu-id="eb2f7-128">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb2f7-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="eb2f7-129">-IpsecIntegrity</span></span>
<span data-ttu-id="eb2f7-130">VpnClient IPSec 무결성 알고리즘(IKE 1단계)</span><span class="sxs-lookup"><span data-stu-id="eb2f7-130">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb2f7-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="eb2f7-131">-PfsGroup</span></span>
<span data-ttu-id="eb2f7-132">새 자식 SA에 대한 IKE 2단계에서 사용되는 VpnClient PFS 그룹</span><span class="sxs-lookup"><span data-stu-id="eb2f7-132">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb2f7-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="eb2f7-133">-SADataSize</span></span>
<span data-ttu-id="eb2f7-134">VpnClient IPSec 보안 연결(빠른 모드 또는 2단계 SA라고도 하는) 페이로드 크기(KB)</span><span class="sxs-lookup"><span data-stu-id="eb2f7-134">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="eb2f7-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="eb2f7-135">-SALifeTime</span></span>
<span data-ttu-id="eb2f7-136">VpnClient IPSec 보안 연결(빠른 모드 또는 2단계 SA라고도 하는) 수명(초)</span><span class="sxs-lookup"><span data-stu-id="eb2f7-136">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="eb2f7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb2f7-137">CommonParameters</span></span>
<span data-ttu-id="eb2f7-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eb2f7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb2f7-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eb2f7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb2f7-140">입력</span><span class="sxs-lookup"><span data-stu-id="eb2f7-140">INPUTS</span></span>

### <span data-ttu-id="eb2f7-141">없음</span><span class="sxs-lookup"><span data-stu-id="eb2f7-141">None</span></span>

## <span data-ttu-id="eb2f7-142">출력</span><span class="sxs-lookup"><span data-stu-id="eb2f7-142">OUTPUTS</span></span>

### <span data-ttu-id="eb2f7-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="eb2f7-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="eb2f7-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eb2f7-144">NOTES</span></span>

## <span data-ttu-id="eb2f7-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb2f7-145">RELATED LINKS</span></span>
