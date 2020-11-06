---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 9ec81a9cf82851905d308fa0e0dd1fa45aeb7af9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528905"
---
# <span data-ttu-id="db558-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="db558-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="db558-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db558-102">SYNOPSIS</span></span>
<span data-ttu-id="db558-103">가상 네트워크 게이트웨이의 VPN 클라이언트 주소 풀을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db558-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db558-104">구문과</span><span class="sxs-lookup"><span data-stu-id="db558-104">SYNTAX</span></span>

### <span data-ttu-id="db558-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="db558-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db558-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="db558-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db558-107">설명은</span><span class="sxs-lookup"><span data-stu-id="db558-107">DESCRIPTION</span></span>
<span data-ttu-id="db558-108">**AzureRmVirtualNetworkVpnClientConfig** cmdlet은 가상 네트워크 게이트웨이의 클라이언트 주소 풀을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="db558-108">The **Set-AzureRmVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="db558-109">이 게이트웨이에 연결 하는 VPN (가상 사설망) 클라이언트에이 주소 풀의 IP 주소가 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db558-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="db558-110">예제의</span><span class="sxs-lookup"><span data-stu-id="db558-110">EXAMPLES</span></span>

### <span data-ttu-id="db558-111">예제 1: 가상 네트워크 게이트웨이에 VPN 클라이언트 주소 풀 할당</span><span class="sxs-lookup"><span data-stu-id="db558-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="db558-112">이 예제에서는 VPN 클라이언트 주소 풀을 ContosoVirtualGateway 이라는 가상 네트워크 게이트웨이에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="db558-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="db558-113">첫 번째 명령은 gateway에 대 한 개체 참조를 만들고 개체는 $Gateway 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db558-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="db558-114">그런 다음이 예제의 두 번째 명령은 **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet을 사용 하 여 주소 풀 10.0.0.0/16을 ContosoVirtualGateway에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="db558-114">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="db558-115">예제 2: 기존 게이트웨이에서 외부 radius 기반 인증 구성</span><span class="sxs-lookup"><span data-stu-id="db558-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="db558-116">이 예제에서는 VPN 클라이언트 주소 풀을 ContosoVirtualGateway 이라는 가상 네트워크 게이트웨이에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="db558-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="db558-117">첫 번째 명령은 gateway에 대 한 개체 참조를 만들고 개체는 $Gateway 라는 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="db558-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="db558-118">그런 다음이 예제의 두 번째 명령은 **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet을 사용 하 여 주소 풀 10.0.0.0/16을 ContosoVirtualGateway에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="db558-118">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="db558-119">또한 vpn 클라이언트에 대 한 인증에 사용할 외부 radius 서버 "TestRadiusServer"를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="db558-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="db558-120">변수</span><span class="sxs-lookup"><span data-stu-id="db558-120">PARAMETERS</span></span>

### <span data-ttu-id="db558-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db558-121">-DefaultProfile</span></span>
<span data-ttu-id="db558-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db558-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db558-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="db558-123">-RadiusServerAddress</span></span>
<span data-ttu-id="db558-124">P2S 외부 Radius 서버 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="db558-124">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db558-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="db558-125">-RadiusServerSecret</span></span>
<span data-ttu-id="db558-126">P2S 외부 Radius 서버 비밀.</span><span class="sxs-lookup"><span data-stu-id="db558-126">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db558-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="db558-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="db558-128">이 cmdlet이 수정 하는 VPN 클라이언트 구성 설정이 포함 된 가상 네트워크 게이트웨이에 대 한 개체 참조를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db558-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="db558-129">Get-AzureRmVirtualNetworkGateway를 사용 하 고 게이트웨이의 이름을 지정 하 여 가상 네트워크 게이트웨이에 대 한 개체 참조를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db558-129">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db558-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="db558-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="db558-131">이 게이트웨이에 연결 하는 클라이언트에 할당할 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db558-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db558-132">-확인</span><span class="sxs-lookup"><span data-stu-id="db558-132">-Confirm</span></span>
<span data-ttu-id="db558-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="db558-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db558-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db558-134">-WhatIf</span></span>
<span data-ttu-id="db558-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="db558-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db558-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db558-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db558-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db558-137">CommonParameters</span></span>
<span data-ttu-id="db558-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db558-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db558-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db558-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db558-140">입력</span><span class="sxs-lookup"><span data-stu-id="db558-140">INPUTS</span></span>

###  
<span data-ttu-id="db558-141">이 cmdlet은 **PSVirtualNetworkGateway** 개체의 파이프라인 인스턴스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="db558-141">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="db558-142">출력</span><span class="sxs-lookup"><span data-stu-id="db558-142">OUTPUTS</span></span>

###  
<span data-ttu-id="db558-143">이 cmdlet은 **PSVirtualNetworkGateway** 개체의 기존 인스턴스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="db558-143">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="db558-144">상속자</span><span class="sxs-lookup"><span data-stu-id="db558-144">NOTES</span></span>

## <span data-ttu-id="db558-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db558-145">RELATED LINKS</span></span>

[<span data-ttu-id="db558-146">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="db558-146">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="db558-147">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="db558-147">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="db558-148">크기 조정-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="db558-148">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


