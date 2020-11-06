---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 38dcfdb1188a810b0f154dfed31f8a1ef3206247
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531384"
---
# <span data-ttu-id="5c768-101">Set-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="5c768-101">Set-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="5c768-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c768-102">SYNOPSIS</span></span>
<span data-ttu-id="5c768-103">기존 가상 네트워크 게이트웨이의 vpn ipsec 매개 변수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c768-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5c768-104">SYNTAX</span></span>

### <span data-ttu-id="5c768-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="5c768-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c768-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5c768-106">ByFactoryObject</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c768-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5c768-107">ByResourceId</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c768-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5c768-108">DESCRIPTION</span></span>
<span data-ttu-id="5c768-109">**AzureRmVpnClientIpsecParameter** cmdlet은 기존 가상 네트워크 게이트웨이에 대 한 vpn ipsec 매개 변수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-109">The **Set-AzureRmVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="5c768-110">가상 네트워크 게이트웨이를 만들면 게이트웨이에서 기본 vpn ipsec 정책 집합을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="5c768-111">예를 들어 사이트 사용자가 특정 사용자 지정 ipsec 정책을 사용 하 여 VPN 게이트웨이에 연결 하려는 경우 먼저 VPN 게이트웨이에서 ipsec 정책을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="5c768-112">**Set-AzureRmVpnClientIpsecParameter** 는이 작업을 수행 하는 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-112">**Set-AzureRmVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="5c768-113">예제의</span><span class="sxs-lookup"><span data-stu-id="5c768-113">EXAMPLES</span></span>

### <span data-ttu-id="5c768-114">예제 1: 사용자 지정 vpn ipsec 정책을 기존 가상 네트워크 게이트웨이로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-114">Example 1 : Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="5c768-115">이 예제에서는 사용자 지정 vpn ipsec 정책을 ContosoResourceGroup 이라는 리소스 그룹에서 ContosoVirtualGateway 이라는 기존 가상 네트워크 게이트웨이로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="5c768-116">New-AzureRmVpnClientIpsecParameter cmdlet은 전달 된 하나 또는 모든 매개 변수를 사용 하는 vpn ipsec 매개 변수 개체를 만드는 데 사용 됩니다. 사용자는 ResourceGroup의 기존 가상 네트워크 게이트웨이에 대해 설정할 수 있는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-116">New-AzureRmVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="5c768-117">이 생성 된 VpnClientIPsecParameters 개체는 위의 예제와 같이 가상 네트워크 게이트웨이에서 지정 된 Vpn ipsec 사용자 지정 정책을 설정 하기 위해 Set-AzureRmVpnClientIpsecParameter 명령에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-117">This created VpnClientIPsecParameters object is passed to Set-AzureRmVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="5c768-118">이 명령은 set 매개 변수를 표시 하는 VpnClientIPsecParameters의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="5c768-119">변수</span><span class="sxs-lookup"><span data-stu-id="5c768-119">PARAMETERS</span></span>

### <span data-ttu-id="5c768-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c768-120">-DefaultProfile</span></span>
<span data-ttu-id="5c768-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c768-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c768-122">-InputObject</span></span>
<span data-ttu-id="5c768-123">가상 네트워크 gateaway 개체</span><span class="sxs-lookup"><span data-stu-id="5c768-123">The virtual network gateaway object</span></span>

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

### <span data-ttu-id="5c768-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c768-124">-ResourceGroupName</span></span>
<span data-ttu-id="5c768-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-125">The resource group name.</span></span>

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

### <span data-ttu-id="5c768-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c768-126">-ResourceId</span></span>
<span data-ttu-id="5c768-127">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5c768-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="5c768-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="5c768-129">가상 네트워크 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="5c768-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="5c768-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="5c768-131">Vpn 클라이언트 ipsec 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5c768-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="5c768-132">이 매개 변수 값은 PS command를 사용 하 여 생성할 수 있습니다. New-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="5c768-132">This parameter value can be constructed using PS command let:New-AzureRmVpnClientIpsecParameter</span></span>

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

### <span data-ttu-id="5c768-133">-확인</span><span class="sxs-lookup"><span data-stu-id="5c768-133">-Confirm</span></span>
<span data-ttu-id="5c768-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c768-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c768-135">-WhatIf</span></span>
<span data-ttu-id="5c768-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c768-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c768-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c768-138">CommonParameters</span></span>
<span data-ttu-id="5c768-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c768-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c768-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c768-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c768-141">입력</span><span class="sxs-lookup"><span data-stu-id="5c768-141">INPUTS</span></span>

### <span data-ttu-id="5c768-142">PSVpnClientIPsecParameters에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5c768-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>
<span data-ttu-id="5c768-143">매개 변수: VpnClientIPsecParameter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5c768-143">Parameters: VpnClientIPsecParameter (ByValue)</span></span>

### <span data-ttu-id="5c768-144">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5c768-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="5c768-145">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5c768-145">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5c768-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5c768-146">System.String</span></span>

## <span data-ttu-id="5c768-147">출력</span><span class="sxs-lookup"><span data-stu-id="5c768-147">OUTPUTS</span></span>

### <span data-ttu-id="5c768-148">PSVpnClientIPsecParameters에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5c768-148">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="5c768-149">상속자</span><span class="sxs-lookup"><span data-stu-id="5c768-149">NOTES</span></span>

## <span data-ttu-id="5c768-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c768-150">RELATED LINKS</span></span>

[<span data-ttu-id="5c768-151">새로운 AzureRmVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="5c768-151">New-AzureRmVpnClientIpsecParameters</span></span>](./New-AzureRmVpnClientIpsecParameters.md)
