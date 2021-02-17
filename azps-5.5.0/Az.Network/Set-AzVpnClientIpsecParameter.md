---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 658a242b724c57092bd155be69743f2080c07732
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202416"
---
# <span data-ttu-id="478f1-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="478f1-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="478f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="478f1-102">SYNOPSIS</span></span>
<span data-ttu-id="478f1-103">기존 가상 네트워크 게이트웨이에 대한 vpn ipsec 매개 변수를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="478f1-104">구문</span><span class="sxs-lookup"><span data-stu-id="478f1-104">SYNTAX</span></span>

### <span data-ttu-id="478f1-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="478f1-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="478f1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="478f1-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="478f1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="478f1-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="478f1-108">설명</span><span class="sxs-lookup"><span data-stu-id="478f1-108">DESCRIPTION</span></span>
<span data-ttu-id="478f1-109">**Set-AzVpnClientIpsecParameter** cmdlet은 기존 가상 네트워크 게이트웨이에 대한 vpn ipsec 매개 변수를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="478f1-110">가상 네트워크 게이트웨이가 만들어질 때 게이트웨이에서 기본 vpn ipsec 정책 집합을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="478f1-111">지점 및 사이트간 사용자가 특정 사용자 지정 ipsec 정책을 사용하여 VPN Gateway에 연결하려는 경우 사용자는 먼저 VPN Gateway에서 해당 ipsec 정책을 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="478f1-112">**Set-AzVpnClientIpsecParameter는** 이를 위해 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="478f1-113">예제</span><span class="sxs-lookup"><span data-stu-id="478f1-113">EXAMPLES</span></span>

### <span data-ttu-id="478f1-114">예제 1: 사용자 지정 vpn ipsec 정책을 기존 가상 네트워크 게이트웨이로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-114">Example 1: Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="478f1-115">이 예제에서는 ContosoResourceGroup이라는 리소스 그룹에서 ContosoVirtualGateway라는 기존 가상 네트워크 게이트웨이에 사용자 지정 vpn ipsec 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="478f1-116">New-AzVpnClientIpsecParameter cmdlet은 사용자가 ResourceGroup의 기존 가상 네트워크 게이트웨이에 대해 설정할 수 있는 전달된 하나 또는 모든 매개 변수 값을 사용하는 vpn ipsec 매개 변수 개체를 만드는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="478f1-117">이 생성한 VpnClientIPsecParameters 개체는 Set-AzVpnClientIpsecParameter 예제와 같이 가상 네트워크 게이트웨이에서 지정된 Vpn ipsec 사용자 지정 정책을 설정하는 Set-AzVpnClientIpsecParameter 명령으로 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="478f1-118">이 명령은 설정된 매개 변수를 표시하는 VpnClientIPsecParameters의 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="478f1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="478f1-119">PARAMETERS</span></span>

### <span data-ttu-id="478f1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="478f1-120">-DefaultProfile</span></span>
<span data-ttu-id="478f1-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="478f1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="478f1-122">-InputObject</span></span>
<span data-ttu-id="478f1-123">가상 네트워크 게이트웨이 개체</span><span class="sxs-lookup"><span data-stu-id="478f1-123">The virtual network gateway object</span></span>

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

### <span data-ttu-id="478f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="478f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="478f1-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-125">The resource group name.</span></span>

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

### <span data-ttu-id="478f1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="478f1-126">-ResourceId</span></span>
<span data-ttu-id="478f1-127">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="478f1-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="478f1-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="478f1-129">가상 네트워크 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="478f1-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="478f1-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="478f1-131">Vpn 클라이언트 ipsec 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="478f1-132">이 매개 변수 값은 PS 명령 let:New-AzVpnClientIpsecParameter를 사용하여 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

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

### <span data-ttu-id="478f1-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="478f1-133">-Confirm</span></span>
<span data-ttu-id="478f1-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="478f1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="478f1-135">-WhatIf</span></span>
<span data-ttu-id="478f1-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="478f1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="478f1-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="478f1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="478f1-138">CommonParameters</span></span>
<span data-ttu-id="478f1-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="478f1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="478f1-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="478f1-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="478f1-141">입력</span><span class="sxs-lookup"><span data-stu-id="478f1-141">INPUTS</span></span>

### <span data-ttu-id="478f1-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="478f1-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="478f1-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="478f1-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="478f1-144">System.String</span><span class="sxs-lookup"><span data-stu-id="478f1-144">System.String</span></span>

## <span data-ttu-id="478f1-145">출력</span><span class="sxs-lookup"><span data-stu-id="478f1-145">OUTPUTS</span></span>

### <span data-ttu-id="478f1-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="478f1-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="478f1-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="478f1-147">NOTES</span></span>

## <span data-ttu-id="478f1-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="478f1-148">RELATED LINKS</span></span>

[<span data-ttu-id="478f1-149">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="478f1-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="478f1-150">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="478f1-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="478f1-151">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="478f1-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)
