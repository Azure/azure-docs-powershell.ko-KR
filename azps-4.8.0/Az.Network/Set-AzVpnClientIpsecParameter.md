---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 658a242b724c57092bd155be69743f2080c07732
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048819"
---
# <span data-ttu-id="75337-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="75337-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="75337-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75337-102">SYNOPSIS</span></span>
<span data-ttu-id="75337-103">기존 가상 네트워크 게이트웨이의 vpn ipsec 매개 변수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75337-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="75337-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75337-104">SYNTAX</span></span>

### <span data-ttu-id="75337-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="75337-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75337-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="75337-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75337-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="75337-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75337-108">설명은</span><span class="sxs-lookup"><span data-stu-id="75337-108">DESCRIPTION</span></span>
<span data-ttu-id="75337-109">**AzVpnClientIpsecParameter** cmdlet은 기존 가상 네트워크 게이트웨이에 대 한 vpn ipsec 매개 변수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75337-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="75337-110">가상 네트워크 게이트웨이를 만들면 게이트웨이에서 기본 vpn ipsec 정책 집합을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75337-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="75337-111">예를 들어 사이트 사용자가 특정 사용자 지정 ipsec 정책을 사용 하 여 VPN 게이트웨이에 연결 하려는 경우 먼저 VPN 게이트웨이에서 ipsec 정책을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="75337-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="75337-112">**Set-AzVpnClientIpsecParameter** 는이 작업을 수행 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="75337-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="75337-113">예제의</span><span class="sxs-lookup"><span data-stu-id="75337-113">EXAMPLES</span></span>

### <span data-ttu-id="75337-114">예제 1: 사용자 지정 vpn ipsec 정책을 기존 가상 네트워크 게이트웨이로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75337-114">Example 1: Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="75337-115">이 예제에서는 사용자 지정 vpn ipsec 정책을 ContosoResourceGroup 이라는 리소스 그룹에서 ContosoVirtualGateway 이라는 기존 가상 네트워크 게이트웨이로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75337-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="75337-116">New-AzVpnClientIpsecParameter cmdlet은 전달 된 하나 또는 모든 매개 변수를 사용 하는 vpn ipsec 매개 변수 개체를 만드는 데 사용 됩니다. 사용자는 ResourceGroup의 기존 가상 네트워크 게이트웨이에 대해 설정할 수 있는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="75337-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="75337-117">이 생성 된 VpnClientIPsecParameters 개체는 위의 예제와 같이 가상 네트워크 게이트웨이에서 지정 된 Vpn ipsec 사용자 지정 정책을 설정 하기 위해 Set-AzVpnClientIpsecParameter 명령에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75337-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="75337-118">이 명령은 set 매개 변수를 표시 하는 VpnClientIPsecParameters의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75337-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="75337-119">변수</span><span class="sxs-lookup"><span data-stu-id="75337-119">PARAMETERS</span></span>

### <span data-ttu-id="75337-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75337-120">-DefaultProfile</span></span>
<span data-ttu-id="75337-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75337-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75337-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75337-122">-InputObject</span></span>
<span data-ttu-id="75337-123">가상 네트워크 게이트웨이 개체</span><span class="sxs-lookup"><span data-stu-id="75337-123">The virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75337-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75337-124">-ResourceGroupName</span></span>
<span data-ttu-id="75337-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75337-125">The resource group name.</span></span>

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

### <span data-ttu-id="75337-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75337-126">-ResourceId</span></span>
<span data-ttu-id="75337-127">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="75337-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75337-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="75337-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="75337-129">가상 네트워크 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75337-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="75337-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="75337-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="75337-131">Vpn 클라이언트 ipsec 매개 변수</span><span class="sxs-lookup"><span data-stu-id="75337-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="75337-132">이 매개 변수 값은 PS command를 사용 하 여 생성할 수 있습니다. New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="75337-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75337-133">-확인</span><span class="sxs-lookup"><span data-stu-id="75337-133">-Confirm</span></span>
<span data-ttu-id="75337-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="75337-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75337-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75337-135">-WhatIf</span></span>
<span data-ttu-id="75337-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="75337-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75337-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75337-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75337-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75337-138">CommonParameters</span></span>
<span data-ttu-id="75337-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75337-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75337-140">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75337-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75337-141">입력</span><span class="sxs-lookup"><span data-stu-id="75337-141">INPUTS</span></span>

### <span data-ttu-id="75337-142">PSVpnClientIPsecParameters에 대 한.</span><span class="sxs-lookup"><span data-stu-id="75337-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="75337-143">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="75337-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="75337-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="75337-144">System.String</span></span>

## <span data-ttu-id="75337-145">출력</span><span class="sxs-lookup"><span data-stu-id="75337-145">OUTPUTS</span></span>

### <span data-ttu-id="75337-146">PSVpnClientIPsecParameters에 대 한.</span><span class="sxs-lookup"><span data-stu-id="75337-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="75337-147">상속자</span><span class="sxs-lookup"><span data-stu-id="75337-147">NOTES</span></span>

## <span data-ttu-id="75337-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75337-148">RELATED LINKS</span></span>

[<span data-ttu-id="75337-149">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="75337-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="75337-150">새로운 AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="75337-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="75337-151">제거-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="75337-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)
