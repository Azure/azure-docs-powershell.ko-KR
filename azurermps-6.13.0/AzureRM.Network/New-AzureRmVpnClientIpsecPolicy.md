---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecPolicy.md
ms.openlocfilehash: 98ea39141614c800b7b71d2f0c75519762bb87b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536560"
---
# <span data-ttu-id="f8f8b-101">New-AzureRmVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="f8f8b-101">New-AzureRmVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="f8f8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f8b-103">사용자는이 명령을 사용 하 여 VPN 게이트웨이에서 설정 되는 Ipsec ipsec 정책 개체를 만들어 (IkeEncryption Encryption, Ipsec Integrity,, IkeIntegrity, DhGroup, PfsGroup 등의 값을 하나 또는 모두 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8f8b-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="f8f8b-104">이 명령은 output 개체를 사용 하 여 new/exisitng gateway에 대 한 vpn ipsec 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8f8b-104">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8f8b-105">구문과</span><span class="sxs-lookup"><span data-stu-id="f8f8b-105">SYNTAX</span></span>

```
New-AzureRmVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8f8b-106">설명은</span><span class="sxs-lookup"><span data-stu-id="f8f8b-106">DESCRIPTION</span></span>
<span data-ttu-id="f8f8b-107">사용자는이 명령을 사용 하 여 VPN 게이트웨이에서 설정 되는 Ipsec ipsec 정책 개체를 만들어 (IkeEncryption Encryption, Ipsec Integrity,, IkeIntegrity, DhGroup, PfsGroup 등의 값을 하나 또는 모두 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8f8b-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="f8f8b-108">이 명령은 output 개체를 사용 하 여 new/exisitng gateway에 대 한 vpn ipsec 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8f8b-108">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

## <span data-ttu-id="f8f8b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f8f8b-109">EXAMPLES</span></span>

### <span data-ttu-id="f8f8b-110">Vpn ipsec 정책 개체 정의:</span><span class="sxs-lookup"><span data-stu-id="f8f8b-110">Define vpn ipsec policy object:</span></span>
```
PS C:\>$vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="f8f8b-111">이 cmdlet은 전달 된 하나 또는 모든 매개 변수를 사용 하 여 vpn ipsec 정책 개체를 생성 하는 데 사용 됩니다. VpnClientIpsecPolicy 명령: p r o m a t:에 New-AzureRmVirtualNetworkGateway (새 VPN 게이트웨이 만들기)/Set-AzureRmVirtualNetworkGateway (기존 VPN 게이트웨이 업데이트) ResourceGroup의 리소스 수:</span><span class="sxs-lookup"><span data-stu-id="f8f8b-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzureRmVirtualNetworkGateway (New VPN Gateway creation) / Set-AzureRmVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="f8f8b-112">Vpn 사용자 지정 ipsec 정책 설정을 사용 하 여 새 가상 네트워크 게이트웨이 만들기:</span><span class="sxs-lookup"><span data-stu-id="f8f8b-112">Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```
PS C:\> $vnetGateway = New-AzureRmVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="f8f8b-113">이 cmdlet은 생성 후 가상 네트워크 게이트웨이 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8f8b-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="f8f8b-114">기존 가상 네트워크 게이트웨이에서 vpn 사용자 지정 ipsec 정책 설정:</span><span class="sxs-lookup"><span data-stu-id="f8f8b-114">Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```
PS C:\> $vnetGateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="f8f8b-115">이 cmdlet은 vpn 사용자 지정 ipsec 정책을 설정한 후 가상 네트워크 게이트웨이 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8f8b-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="f8f8b-116">Vpn 사용자 지정 정책이 올바르게 설정 되어 있는지 확인 하려면 가상 네트워크 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8f8b-116">Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```
PS C:\> $gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="f8f8b-117">이 cmdlet은 가상 네트워크 게이트웨이 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8f8b-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="f8f8b-118">변수</span><span class="sxs-lookup"><span data-stu-id="f8f8b-118">PARAMETERS</span></span>

### <span data-ttu-id="f8f8b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8f8b-119">-DefaultProfile</span></span>
<span data-ttu-id="f8f8b-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8f8b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f8b-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="f8f8b-121">-DhGroup</span></span>
<span data-ttu-id="f8f8b-122">초기 SA에 대 한 IKE 단계 1에 사용 되는 Vpnclient DH 그룹</span><span class="sxs-lookup"><span data-stu-id="f8f8b-122">The Vpnclient DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="f8f8b-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="f8f8b-123">-IkeEncryption</span></span>
<span data-ttu-id="f8f8b-124">Vpnclient IKE 암호화 알고리즘 (IKE 단계 2)</span><span class="sxs-lookup"><span data-stu-id="f8f8b-124">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="f8f8b-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="f8f8b-125">-IkeIntegrity</span></span>
<span data-ttu-id="f8f8b-126">Vpnclient IKE 무결성 알고리즘 (IKE 단계 2)</span><span class="sxs-lookup"><span data-stu-id="f8f8b-126">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="f8f8b-127">-암호 암호화</span><span class="sxs-lookup"><span data-stu-id="f8f8b-127">-IpsecEncryption</span></span>
<span data-ttu-id="f8f8b-128">Vpnclient IPSec 암호화 알고리즘 (IKE 단계 1)</span><span class="sxs-lookup"><span data-stu-id="f8f8b-128">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="f8f8b-129">-계층 무결성</span><span class="sxs-lookup"><span data-stu-id="f8f8b-129">-IpsecIntegrity</span></span>
<span data-ttu-id="f8f8b-130">Vpnclient IPSec 무결성 알고리즘 (IKE 단계 1)</span><span class="sxs-lookup"><span data-stu-id="f8f8b-130">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="f8f8b-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="f8f8b-131">-PfsGroup</span></span>
<span data-ttu-id="f8f8b-132">새 자식 SA에 대 한 IKE 단계 2에 사용 되는 Vpnclient PFS 그룹</span><span class="sxs-lookup"><span data-stu-id="f8f8b-132">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="f8f8b-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="f8f8b-133">-SADataSize</span></span>
<span data-ttu-id="f8f8b-134">Vpnclient IPSec 보안 연결 (빠른 모드 또는 2 단계 SA 라고도 함) 페이로드 크기 (KB)</span><span class="sxs-lookup"><span data-stu-id="f8f8b-134">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="f8f8b-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="f8f8b-135">-SALifeTime</span></span>
<span data-ttu-id="f8f8b-136">Vpnclient IPSec 보안 연결 (빠른 모드 또는 2 단계 SA 라고도 함) 수명이 초 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="f8f8b-136">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="f8f8b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f8b-137">CommonParameters</span></span>
<span data-ttu-id="f8f8b-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8f8b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f8b-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8f8b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f8b-140">입력</span><span class="sxs-lookup"><span data-stu-id="f8f8b-140">INPUTS</span></span>

### <span data-ttu-id="f8f8b-141">않아야</span><span class="sxs-lookup"><span data-stu-id="f8f8b-141">None</span></span>

## <span data-ttu-id="f8f8b-142">출력</span><span class="sxs-lookup"><span data-stu-id="f8f8b-142">OUTPUTS</span></span>

### <span data-ttu-id="f8f8b-143">PSIpsecPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f8f8b-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="f8f8b-144">상속자</span><span class="sxs-lookup"><span data-stu-id="f8f8b-144">NOTES</span></span>

## <span data-ttu-id="f8f8b-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8f8b-145">RELATED LINKS</span></span>
