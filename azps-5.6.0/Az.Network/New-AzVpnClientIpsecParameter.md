---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 3b34fb1de6b661a622690f93808eaf0660da461b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995325"
---
# <span data-ttu-id="6ce40-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="6ce40-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="6ce40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ce40-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce40-103">이 명령을 사용하면 사용자가 IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup과 같은 하나 또는 모든 값을 지정하는 VPN ipsec 매개 변수 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ce40-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="6ce40-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ce40-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ce40-105">설명</span><span class="sxs-lookup"><span data-stu-id="6ce40-105">DESCRIPTION</span></span>
<span data-ttu-id="6ce40-106">이 명령을 사용하면 사용자가 IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup과 같은 하나 또는 모든 값을 지정하는 VPN ipsec 매개 변수 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ce40-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="6ce40-107">예제</span><span class="sxs-lookup"><span data-stu-id="6ce40-107">EXAMPLES</span></span>

### <span data-ttu-id="6ce40-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6ce40-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="6ce40-109">New-AzVpnClientIpsecParameter cmdlet은 사용자가 ResourceGroup의 기존 가상 네트워크 게이트웨이에 대해 설정할 수 있는 전달된 하나 또는 모든 매개 변수 값을 사용하는 vpn ipsec 매개 변수 개체를 만드는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ce40-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="6ce40-110">이 만든 VpnClientIPsecParameters 개체는 위의 예제와 Set-AzVpnClientIpsecParameter 가상 네트워크 게이트웨이에서 지정된 Vpn ipsec 사용자 지정 정책을 설정하는 명령으로 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ce40-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="6ce40-111">이 명령은 설정된 매개 변수를 보여주는 VpnClientIPsecParameters의 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce40-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="6ce40-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6ce40-112">PARAMETERS</span></span>

### <span data-ttu-id="6ce40-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ce40-113">-DefaultProfile</span></span>
<span data-ttu-id="6ce40-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ce40-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ce40-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="6ce40-115">-DhGroup</span></span>
<span data-ttu-id="6ce40-116">초기 SA에 IKE 1단계에서 사용되는 VpnClient DH 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="6ce40-116">The VpnClient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="6ce40-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="6ce40-117">-IkeEncryption</span></span>
<span data-ttu-id="6ce40-118">VpnClient IKE 암호화 알고리즘(IKE 2단계)</span><span class="sxs-lookup"><span data-stu-id="6ce40-118">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="6ce40-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="6ce40-119">-IkeIntegrity</span></span>
<span data-ttu-id="6ce40-120">VpnClient IKE 무결성 알고리즘(IKE 2단계)</span><span class="sxs-lookup"><span data-stu-id="6ce40-120">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="6ce40-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="6ce40-121">-IpsecEncryption</span></span>
<span data-ttu-id="6ce40-122">VpnClient IPSec 암호화 알고리즘(IKE 1단계)</span><span class="sxs-lookup"><span data-stu-id="6ce40-122">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="6ce40-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="6ce40-123">-IpsecIntegrity</span></span>
<span data-ttu-id="6ce40-124">VpnClient IPSec 무결성 알고리즘(IKE 1단계)</span><span class="sxs-lookup"><span data-stu-id="6ce40-124">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="6ce40-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="6ce40-125">-PfsGroup</span></span>
<span data-ttu-id="6ce40-126">새 자식 SA에 대한 IKE 2단계에서 사용되는 VpnClient PFS 그룹</span><span class="sxs-lookup"><span data-stu-id="6ce40-126">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="6ce40-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="6ce40-127">-SADataSize</span></span>
<span data-ttu-id="6ce40-128">KB의 VpnClient IPSec 보안 협회(빠른 모드 또는 2단계 SA라고도 하는) 페이로드 크기</span><span class="sxs-lookup"><span data-stu-id="6ce40-128">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="6ce40-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="6ce40-129">-SALifeTime</span></span>
<span data-ttu-id="6ce40-130">VpnClient IPSec 보안 협회(빠른 모드 또는 2단계 SA라고도 하는) 수명이 몇 초 만에</span><span class="sxs-lookup"><span data-stu-id="6ce40-130">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="6ce40-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce40-131">CommonParameters</span></span>
<span data-ttu-id="6ce40-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce40-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce40-133">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6ce40-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce40-134">입력</span><span class="sxs-lookup"><span data-stu-id="6ce40-134">INPUTS</span></span>

### <span data-ttu-id="6ce40-135">없음</span><span class="sxs-lookup"><span data-stu-id="6ce40-135">None</span></span>

## <span data-ttu-id="6ce40-136">출력</span><span class="sxs-lookup"><span data-stu-id="6ce40-136">OUTPUTS</span></span>

### <span data-ttu-id="6ce40-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="6ce40-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="6ce40-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6ce40-138">NOTES</span></span>

## <span data-ttu-id="6ce40-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ce40-139">RELATED LINKS</span></span>

[<span data-ttu-id="6ce40-140">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="6ce40-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="6ce40-141">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="6ce40-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="6ce40-142">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="6ce40-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
