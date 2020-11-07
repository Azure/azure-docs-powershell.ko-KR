---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 975826c459111e900e733b751c15d854c54ee2a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871330"
---
# <span data-ttu-id="8eb6e-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8eb6e-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="8eb6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eb6e-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb6e-103">이 명령을 사용 하면 사용자가 IkeEncryption 암호화, Ipsec Integrity,, IkeIntegrity, DhGroup, PfsGroup 등 기존 VPN 게이트웨이에서 설정할 값을 하나 또는 모두 지정 하 여 Vpn ipsec 매개 변수 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="8eb6e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8eb6e-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8eb6e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8eb6e-105">DESCRIPTION</span></span>
<span data-ttu-id="8eb6e-106">이 명령을 사용 하면 사용자가 IkeEncryption 암호화, Ipsec Integrity,, IkeIntegrity, DhGroup, PfsGroup 등 기존 VPN 게이트웨이에서 설정할 값을 하나 또는 모두 지정 하 여 Vpn ipsec 매개 변수 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="8eb6e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8eb6e-107">EXAMPLES</span></span>

### <span data-ttu-id="8eb6e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8eb6e-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="8eb6e-109">New-AzVpnClientIpsecParameter cmdlet은 전달 된 하나 또는 모든 매개 변수를 사용 하는 vpn ipsec 매개 변수 개체를 만드는 데 사용 됩니다. 사용자는 ResourceGroup의 기존 가상 네트워크 게이트웨이에 대해 설정할 수 있는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="8eb6e-110">이 생성 된 VpnClientIPsecParameters 개체는 위의 예제와 같이 가상 네트워크 게이트웨이에서 지정 된 Vpn ipsec 사용자 지정 정책을 설정 하기 위해 Set-AzVpnClientIpsecParameter 명령에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="8eb6e-111">이 명령은 set 매개 변수를 표시 하는 VpnClientIPsecParameters의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="8eb6e-112">변수</span><span class="sxs-lookup"><span data-stu-id="8eb6e-112">PARAMETERS</span></span>

### <span data-ttu-id="8eb6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eb6e-113">-DefaultProfile</span></span>
<span data-ttu-id="8eb6e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eb6e-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="8eb6e-115">-DhGroup</span></span>
<span data-ttu-id="8eb6e-116">초기 SA에 대 한 IKE 단계 1에 사용 되는 VpnClient DH 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-116">The VpnClient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="8eb6e-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="8eb6e-117">-IkeEncryption</span></span>
<span data-ttu-id="8eb6e-118">VpnClient IKE 암호화 알고리즘 (IKE 단계 2)</span><span class="sxs-lookup"><span data-stu-id="8eb6e-118">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="8eb6e-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="8eb6e-119">-IkeIntegrity</span></span>
<span data-ttu-id="8eb6e-120">VpnClient IKE 무결성 알고리즘 (IKE 단계 2)</span><span class="sxs-lookup"><span data-stu-id="8eb6e-120">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="8eb6e-121">-암호 암호화</span><span class="sxs-lookup"><span data-stu-id="8eb6e-121">-IpsecEncryption</span></span>
<span data-ttu-id="8eb6e-122">VpnClient IPSec 암호화 알고리즘 (IKE 단계 1)</span><span class="sxs-lookup"><span data-stu-id="8eb6e-122">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="8eb6e-123">-계층 무결성</span><span class="sxs-lookup"><span data-stu-id="8eb6e-123">-IpsecIntegrity</span></span>
<span data-ttu-id="8eb6e-124">VpnClient IPSec 무결성 알고리즘 (IKE 단계 1)</span><span class="sxs-lookup"><span data-stu-id="8eb6e-124">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="8eb6e-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="8eb6e-125">-PfsGroup</span></span>
<span data-ttu-id="8eb6e-126">새 자식 SA에 대 한 IKE 단계 2에 사용 되는 VpnClient PFS 그룹</span><span class="sxs-lookup"><span data-stu-id="8eb6e-126">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="8eb6e-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="8eb6e-127">-SADataSize</span></span>
<span data-ttu-id="8eb6e-128">VpnClient IPSec 보안 연결 (빠른 모드 또는 2 단계 SA 라고도 함) 페이로드 크기 (KB)</span><span class="sxs-lookup"><span data-stu-id="8eb6e-128">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="8eb6e-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="8eb6e-129">-SALifeTime</span></span>
<span data-ttu-id="8eb6e-130">VpnClient IPSec 보안 연결 (빠른 모드 또는 2 단계 SA 라고도 함) 수명이 초 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-130">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="8eb6e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eb6e-131">CommonParameters</span></span>
<span data-ttu-id="8eb6e-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eb6e-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eb6e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eb6e-134">입력</span><span class="sxs-lookup"><span data-stu-id="8eb6e-134">INPUTS</span></span>

### <span data-ttu-id="8eb6e-135">않아야</span><span class="sxs-lookup"><span data-stu-id="8eb6e-135">None</span></span>

## <span data-ttu-id="8eb6e-136">출력</span><span class="sxs-lookup"><span data-stu-id="8eb6e-136">OUTPUTS</span></span>

### <span data-ttu-id="8eb6e-137">PSVpnClientIPsecParameters에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="8eb6e-138">상속자</span><span class="sxs-lookup"><span data-stu-id="8eb6e-138">NOTES</span></span>

## <span data-ttu-id="8eb6e-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8eb6e-139">RELATED LINKS</span></span>

[<span data-ttu-id="8eb6e-140">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8eb6e-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="8eb6e-141">제거-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8eb6e-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="8eb6e-142">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8eb6e-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
